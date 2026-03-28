# MASTER PROMPT ENGINEERING PROTOCOL

## I. THREE-PHASE SCRIPTING (0-15s)

1. **Initial Phase (0-20%):** Establish the Anchor State (from Start Frame). Static intro.
2. **Action Phase (20-80%):** The core transformation, camera vector, or movement.
3. **Resolution Phase (80-100%):** Settling into the Final State (from End Frame).

---

## II. THE "ANCHOR" RULE (Consistency)

* The Subject description (e.g., "1967 Black Mustang") must be 100% identical in all prompt blocks.
* Do not change lighting or camera angle between Start and End prompts unless a "Camera Move" is requested.

---

## III. OPTIMIZATION & FORBIDDEN TOKENS

* **Forbidden:** "masterpiece", "beautiful", "high quality", "realistic", "4k/8k"
* **Mandatory:** "35mm anamorphic", "global illumination", "momentum", "85mm lens", "volumetric light"
* **Separation:** Always describe Subject Motion and Camera Motion in separate sentences.

---

## IV. FORBIDDEN & MANDATORY TOKENS (The "Anti-Clutter" List)

### 1. Forbidden Tokens

* **Оценочные:** beautiful, masterpiece, high quality, amazing, stunning, breathtaking, incredible
* **Технический спам:** 4k, 8k, ultra-realistic, photorealistic, cinematic, real-life
* **Абстракции:** perfect, ideal, best, cool, style
* **Пустые фразы:** highly detailed background, many details

### 2. Mandatory Technical Replacements

* Вместо "Beautiful light" → `Rim Lighting, Volumetric God Rays, Global Illumination`
* Вместо "High quality skin" → `Subsurface Scattering (SSS), micro-pores, peach fuzz`
* Вместо "Realistic metal" → `Anisotropic reflections, ray-traced reflections, surface imperfections`
* Вместо "Moving camera" → `Dolly Push, Orbit Shot, Pan, Tilt`
* Вместо "Water looks real" → `Contact Angle Dynamics, hydrophilic flat meniscus, capillary creep`
* Вместо "Splash effect" → `Crown Splash Dynamics, Worthington Jet, satellite microdroplets`
* Вместо "Lava touches rock" → `Vapour Flash Boundary, ablation trail, radial thermal cracking`
* Вместо "Honey dripping" → `Viscous Stringing, elastic liquid filaments, meniscus tear`

### 3. Syntax Hygiene

* **No "@" tags:** Символ @ запрещён.
* **Short Sentences:** `[Subject] + [Action] + [Context]`
* **Material First:** Сначала материал объекта, затем его движение.

---

## V. MULTI-SHOT & CONSISTENCY LOGIC

* **Scene Transition Anchoring:** Anchor переносится из предыдущего промпта без изменений.
* **Match Cut Protocol:** End Frame = Start Frame следующего ролика по композиции и освещению.
* **Lighting Key Consistency:** Указывай конкретный тип света (`Warm 3200K key light`) везде.
* **Motion Continuity:** Движение камеры должно логично продолжаться или затухать между роликами.

---

## VI. ADVANCED SYNTAX HACKS (Power Tokens)

* **Zero-Motion Anchor (Nano Banana 2):** В Start Frame. Максимальная детализация без Motion Blur.
* **Temporal Texture Persistence:** Удерживает микро-рельеф в начале. Убирает мерцание текстур.
* **3rd Person:** `3rd Person cinematic close-up` | **1st Person:** `1st person POV hand-tracking`
* **Sequential Physics Trigger:** `[Subject] starts to glow, THEN melts into [Liquid]`
  **THEN** / **FOLLOWED BY** — критический триггер для Kling 3.0.

---

## VII. NEGATIVE PROMPTING & HYGIENE

### ВАЖНО — Платформенное ограничение RunwayML
RunwayML не имеет отдельного поля Negative Prompt ни в режиме Image (Nano Banana 2)
ни в режиме Video (Kling 3.0 Pro). Единственный рабочий метод — inline-запрет
в конце промпта через явные отрицания:

**Обязательная закрывающая строка каждого промпта:**
`No jelly-like distortion, no flickering, no limb duplication,
no floating debris, no sudden frame jumps, no brand hallucination`

**Сцено-специфичные дополнения (добавлять к базовой строке):**

| Тип сцены | Дополнительный inline-негатив |
|---|---|
| Жидкости / морфинг | `no surface tension violation, no physics reversal` |
| Лицо / персонаж | `no teeth distortion, no eye asymmetry, no skin flickering` |
| Огонь / взрыв | `no static flame, no uniform color burn, no floating embers` |
| Техника / авто | `no wheel deformation, no logo distortion` |
| Макро / капли | `no droplet merging artifacts, no gravity reversal` |
| Термальный контакт | `no instant material phase skip, no colour banding` |

---

## VIII. TIMESTAMP SCRIPTING (Метод Таймлайна)

Только для внутреннего анализа — НЕ в финальном промпте:

* **0-3s:** Initial state, micro-vibrations, establish anchor.
* **3-10s:** Core kinetic action, primary transformation, camera orbit.
* **10-15s:** Final settlement, lens flare exit, micro-debris floating.

---

## ⚠️ CLEAN PROMPT RULE (CRITICAL)

Цифры секунд и двоеточия в финальном `<Kling Video Prompt>` **ЗАПРЕЩЕНЫ**.

**Шаблон:**
Initial state: [anchor + micro-details]. THEN [core action + physics token].
FOLLOWED BY [camera move + optical effect]. FINALLY [resolution + audio tags].

**Пример:**
Initial state: 1967 black Mustang fastback, anisotropic brushed grain on hood,
surface grit and lens grime. THEN engine ignites, structural latency deformation delay
on chassis panels, vapour flash boundary at exhaust ports. FOLLOWED BY Dolly Push,
Cooke S4 anamorphic rendering, lens breathing on focus shift. FINALLY speed ramp to
120fps slow-motion, anamorphic blue flare exit.
[Sound: V8 roar, metallic hiss] [Ambient: desert wind]