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

## IV. GENERATION MODES (Режимы генерации Kling 3.0 Pro)

---

### РЕЖИМ 1 — FRAMES
Доступно: Start Frame + End Frame + текстовый промпт
Длительность: 5s / 10s / 15s

Когда использовать:
- Трансформация материала (твёрдое → жидкое)
- Морфинг объекта
- Смена состояния (сухое → мокрое, холодное → раскалённое)
- Любой эффект где важно финальное состояние

Пайплайн:
    Nano Banana 2 → Start Frame → скачать
    Nano Banana 2 → End Frame (из Start Frame как референс) → скачать
    Kling FRAMES → загрузить оба кадра + промпт → Generate

Выбор длительности:
    5s  — быстрый удар, импульс, взрыв (Scale 7-10)
    10s — стандартная трансформация (Scale 4-7)
    15s — медленный морфинг, детализированные изменения (Scale 2-6)

Референсное фото (если есть):
    Используется ТОЛЬКО на шаге генерации Start Frame в Nano Banana 2.
    End Frame всегда генерируется из скачанного Start Frame — не из оригинала.

Промпт для Start Frame:
    [Субъект из референса / описание субъекта]. Zero-Motion Anchor.
    [Материал — SSS / Anisotropic / etc.].
    [Освещение — Rim Light / Chiaroscuro / Warm 3200K key light].
    [Камера — 85mm portrait / 35mm wide / Low-angle].
    [Сцена / окружение].

Промпт для End Frame:
    Subject from reference image. Maintain identical facial geometry,
    lighting direction, camera angle, and composition.
    ONLY change: [что меняется — материал / состояние / выражение].
    Zero-Motion Anchor. No expression drift. No angle shift.
    [Финальный материал — SSS / Anisotropic / etc.].

Consistency Anchors (обязательны в End Frame промпте):
    `Subject from reference image` — явная привязка к Start Frame
    `Maintain identical [angle / lighting / composition]` — фиксация параметров
    `ONLY change: [X]` — явное ограничение что разрешено меняться

---

### РЕЖИМ 2 — MULTISHOT
Доступно: Start Frame (общий) + промпт для каждого шота
Длительность каждого шота: 3-12s
Суммарная длительность: не более 15s

Когда использовать:
- Нарративная последовательность (несколько действий подряд)
- Смена ракурсов камеры внутри одной сцены
- Несколько эмоций или состояний подряд
- Shot list из 2-4 шотов

Пайплайн:
    Nano Banana 2 → Start Frame → скачать
    Kling MULTISHOT → загрузить Start Frame
    → Shot 1: промпт + длительность
    → Shot 2: промпт + длительность
    → Shot 3: промпт + длительность (если нужен)
    → Generate

Типовые конфигурации шотов:
    2 шота: 7s + 8s = 15s
    3 шота: 5s + 5s + 5s = 15s
    3 шота: 4s + 5s + 6s = 15s
    4 шота: 3s + 4s + 4s + 4s = 15s

Важные ограничения:
- Start Frame один для всей последовательности
- End Frame недоступен — финал описывается только текстом последнего шота
- Каждый шот получает отдельный промпт
- Anchor субъекта должен быть идентичен в каждом шот-промпте
- Clean Prompt Rule действует для каждого шот-промпта отдельно

---

### ВЫБОР РЕЖИМА — БЫСТРАЯ ТАБЛИЦА

| Задача | Режим | Почему |
|---|---|---|
| Объект плавится / морфирует | FRAMES | Нужен точный End Frame |
| Персонаж делает 3 действия | MULTISHOT | Нарратив из нескольких шотов |
| Reveal материала | FRAMES | Финальное состояние критично |
| Диалог + реакция + уход | MULTISHOT | Три разных момента |
| Удар капли (макро) | FRAMES | Точный начальный и конечный кадр |
| Смена ракурсов камеры | MULTISHOT | Несколько углов одной сцены |
| Термальный контакт | FRAMES | Нужен финальный след |
| Атмосферная сцена | MULTISHOT | Накопление деталей по шотам |
| Портрет / Lip-sync | FRAMES | Точный контроль финального состояния |
| Экшен сцена (3+ действия) | MULTISHOT | Динамика нескольких шотов |
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
