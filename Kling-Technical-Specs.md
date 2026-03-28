# KLING PRO - TECHNICAL ARCHITECTURE & LIMITS

## I. TEMPORAL MODES & PACING

* **5s Mode:** High-speed dynamics. Best for: Explosions, jumps, quick camera pans, rapid impacts.
* **10s Mode:** Narrative flow. Best for: Walking, talking, steady environmental reveals, character acting.
* **15s Mode:** Complex Transitions & Morphing. Best for: Texture shifts, slow cinematic reveals, material changes.

---

## II. MOTION SCALE SYSTEM (Values 1-10)

* **1-2 (Static/Micro):** Only wind, dust, or breathing. Use for high-detail macro shots.
* **3-5 (Natural):** Normal human/animal movement, steady vehicle cruise, hair blowing.
* **6-8 (Cinematic):** Fast tracking, dramatic action, sports, controlled debris.
* **9-10 (Hyper/Chaos):** Massive destruction, high-velocity transitions, camera shakes.

---

## III. MOTION SCALE REFERENCE TABLE (Таблица Motion Scale по сценам)

### Шкала значений (1-10)

| Scale | Категория | Характеристика |
|---|---|---|
| 1-2 | Static / Micro | Только дыхание, ветер, пыль. Макросъёмка |
| 3-5 | Natural | Обычное движение человека, животного, транспорта |
| 6-8 | Cinematic | Экшен, драматика, спорт, контролируемый хаос |
| 9-10 | Hyper / Chaos | Разрушение, высокоскоростные переходы, shake |

---

### Рекомендации по типам сцен

| Тип сцены | Scale | Режим | Обоснование |
|---|---|---|---|
| Макро капля / Impact | 6-7 | 5s | Быстрый удар, короткое действие |
| Портрет / Lip-sync | 2-3 | 10-15s | Минимум движения, максимум детали лица |
| Жидкая трансформация | 5-7 | 15s | Плавный морфинг, нужно время |
| Reveal автомобиля | 4-6 | 10-15s | Плавное движение камеры, детали |
| Огонь / взрыв | 8-10 | 10-15s | Хаотичная динамика, debris |
| Термальный контакт | 6-8 | 10-15s | Активная реакция материалов |
| Атмосфера / среда | 2-4 | 10-15s | Медленное накопление деталей |
| Персонаж идёт | 3-5 | 10s | Естественное движение |
| Разрушение / краш | 9-10 | 5-10s | Максимальный хаос, быстро |
| Ткань на ветру | 4-6 | 10s | Органичное колыхание |
| Стекло бьётся | 7-9 | 5s | Быстрый импульс, разлёт осколков |
| Продуктовый макро | 1-3 | 10-15s | Статика с микродеталями |

---

### Правило совмещения Scale и Duration

    Scale 1-4  → предпочтителен режим 10-15s (нужно время для накопления деталей)
    Scale 5-7  → любой режим 5-15s в зависимости от сцены
    Scale 8-10 → предпочтителен режим 5-10s (хаос не нужно растягивать)

### Критическое правило
Scale 9-10 в режиме 15s — почти всегда даёт артефакты.
Kling теряет консистентность субъекта при высоком Scale на длинных клипах.

---

## IV. DUAL-FRAME PIPELINE (Start/End Frame) & PLATFORM WORKFLOW

### Pipeline Platform
Вся генерация происходит на одной платформе: **RunwayML (app.runwayml.com)**

Внутри платформы два режима:
* **Image (Nano Banana 2):** Генерация статичных кадров. Используется для
  создания Start Frame и End Frame перед видеогенерацией.
* **Video (Kling 3.0 Pro):** Генерация видео. Принимает Start/End Frame
  и текстовый промпт.

### Рабочий порядок (всегда):
1. Вкладка **Image** → Nano Banana 2 → референс в слот (если есть) →
   генерируем Start Frame → скачиваем результат
2. Вкладка **Image** → Nano Banana 2 → скачанный Start Frame в слот →
   генерируем End Frame
3. Вкладка **Video** → Kling 3.0 Pro → загружаем оба кадра + промпт → Generate

**Ключевые правила:**
* Референс → используется ТОЛЬКО на Шаге 1
* End Frame → всегда генерируется из Start Frame, не из оригинального референса
* Один субъект проходит сквозь весь пайплайн без разрывов консистентности

### Frame Slot Logic
* **Start Frame:** Defines the Source Anchor (Geometry, Lighting Key, Initial State).
  Всегда Zero-Motion Anchor — без размытия, максимальная детализация.
* **End Frame:** Defines the Target State (Final Texture, Material, or Position).
* **Image Guidance:** Настройка guidance недоступна в интерфейсе RunwayML.
  Консистентность субъекта между кадрами обеспечивается исключительно
  через текстовые якоря в промпте (см. Consistency Anchors ниже).

### Consistency Anchors (замена guidance)
Три обязательных якоря в промпте для End Frame — без них субъект изменится:

* `Subject from reference image` — явная привязка к референсу
* `Maintain identical [angle / lighting / composition]` — фиксация параметров
* `ONLY change: [X]` — явное ограничение что разрешено меняться

### Промпты для генерации кадров

---

**Промпт для Start Frame — с референсом:**
Subject from reference. [Описание сцены / окружения].
Zero-Motion Anchor.
[Материал — SSS / Anisotropic / etc.].
[Освещение — Rim Light / Chiaroscuro / Warm 3200K key light].
[Камера — 85mm portrait / 35mm wide / Low-angle].

**Промпт для Start Frame — без референса:**
[Полное описание субъекта — внешность, одежда, поза].
[Описание сцены / окружения]. Zero-Motion Anchor.
[Материал — SSS / Anisotropic / etc.].
[Освещение — Rim Light / Chiaroscuro / Warm 3200K key light].
[Камера — 85mm portrait / 35mm wide / Low-angle].

---

**Промпт для End Frame (всегда из Start Frame):**
Subject from reference image. Maintain identical facial geometry,
lighting direction, camera angle, and composition.
ONLY change: [что меняется — материал / состояние / выражение].
Zero-Motion Anchor. No expression drift. No angle shift.
[Финальный материал — SSS / Anisotropic / etc.].

> End Frame всегда генерируется из скачанного Start Frame —
> независимо от того был референс на Шаге 1 или нет.

### Negative Prompt
Отдельного поля Negative Prompt в интерфейсе RunwayML нет ни в Image ни в Video.
Негативные директивы вшиваются inline в конец основного промпта:
`No jelly-like distortion, no flickering, no [scene-relevant artifact]`

---

## V. NATIVE AUDIO ENGINE

* **Sync Protocol:** Audio must trigger at the visual "Peak" of the movement.
* **Format:** [Ambient: context], [Sound: specific action], [Music: mood/genre].
* **Example:** `[Sound: liquid squelching, metallic hiss] [Ambient: heavy desert wind]`

---

## VI. NATIVE AUDIO & LIP-SYNC PROTOCOL (v2.0)

* **High-Fidelity Lip-Sync:** При использовании видео с говорящим персонажем обязательно добавляй:
  `[Character] speaks directly to lens, high-fidelity lip synchronization, natural jaw movement`
* **Layered Soundscape:** Всегда разделяй аудио на три слоя в конце промпта:
  * `[Dialogue: "Текст реплики"]` — если есть речь.
  * `[Sound: specific mechanical/organic actions]` — например, `metallic clinking`, `liquid splashing`.
  * `[Ambient: environment mood]` — например, `deep space hum`, `wind howling`.
* **Emotional Tonality:** Маркеры для голоса: `[Voice: raspy, whispering, authoritative, trembling with fear]`
