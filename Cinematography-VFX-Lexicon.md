# CINEMATOGRAPHY & VFX LEXICON (MASTER)

## I. CINEMATOGRAPHY & STAGING

### 1. Spatial Layering (Mandatory)

* **Foreground (FG):** Focus on macro textures (scratches, dust motes, rain droplets on lens).
* **Midground (MG):** The Subject (Anchor) and its primary movement/transformation.
* **Background (BG):** Parallax depth, moving clouds, distant traffic, city lights, heat haze.

### 2. Camera Directives

* **Dolly Push/Pull:** Physical camera move on tracks. Creates intense depth and tension.
* **Orbit Shot:** 360-degree rotation. Ideal for showing all sides of a transformation.
* **Rack Focus:** Cinematic focus shift between FG and MG.
* **Crane / Jib Shot:** Vertical sweeping motion (high-to-low or low-to-high).
* **Handheld Organic Shake:** Subtle micro-vibrations for "found footage" realism.
* **Low-Angle Tracking:** Following the subject from below to emphasize power/scale.
* **Whip Pan:** Сверхбыстрый горизонтальный смаз кадра. Используется как переход
  между сценами или для передачи дезориентации.
  Токен: `whip pan transition — extreme horizontal motion blur wipe`
* **Dutch Tilt (Canted Angle):** Камера наклонена по оси — создаёт ощущение
  психологического напряжения, нестабильности или угрозы.
  Токен: `Dutch tilt 15-degree canted frame angle, psychological unease composition`
* **Crash Zoom:** Резкий наезд объективом (не движением камеры) — агрессивное
  внимание к деталю или шоковый акцент.
  Токен: `crash zoom punch-in to subject, rapid focal compression with barrel distortion`
* **Snorricam (Body Mount):** Камера закреплена на теле актёра — фон движется,
  лицо остаётся в центре кадра. Эффект диссоциации.
  Токен: `Snorricam body-mount perspective, subject static while world rotates around`
  
### 3. Optics & Lenses

* **35mm / 50mm:** Natural perspective, standard field of view.
* **85mm / 100mm:** Portrait compression, shallow depth of field (creamy bokeh).
* **14mm / Wide-angle:** Epic scale, slight barrel distortion at edges.
* **Anamorphic Lens:** Cinematic wide flares, oval bokeh, horizontal blue light leaks.

---

## II. VISUAL EFFECTS (VFX) & LIGHTING

### 1. Lighting Rig Design

* **Rim Lighting / Edge Light:** High-intensity light from behind. Defines silhouettes.
* **Volumetric Lighting (God Rays):** Visible shafts of light through dust, smoke, or water.
* **Global Illumination (GI):** Realistic light bouncing between surfaces.
* **Chiaroscuro:** High-contrast lighting with deep, dramatic shadows.
* **Teal & Orange Grade:** Industry-standard cinematic color contrast.

### 2. Advanced Material Shaders

* **Subsurface Scattering (SSS):** Light penetration for organic/soft surfaces.
* **Iridescence (Thin-film Interference):** Rainbow color shifts (oil slicks, soap bubbles).
* **Anisotropic Reflections:** Directional highlights on brushed metal, hair, carbon fiber.
* **Clear Coat:** Glossy mirror-like top layer over a matte base.
* **Ray-Traced Reflections:** Physically accurate mirror surfaces and environmental reflections.

### 3. Particle Systems & Environment

* **Debris & Embers:** Small floating particles for fire or destruction scenes.
* **Brownian Motion:** Natural, random movement of dust particles in light shafts.
* **Heat Haze:** Shimmering air distortion for desert or engine exhaust scenes.
* **Caustics:** Concentrated light patterns refracted through glass or water.

---

## III. ATMOSPHERIC & OPTICAL TEXTURES (Секреты «киношности»)

* **Micro-dust Illumination:** «Танцующие» пылинки в контровом свете. Физический объём кадра.
  Токен: `micro-dust illumination in backlit shaft, Brownian motion particle drift`
* **Lens Breathing:** Картинка слегка «пульсирует» при переходе фокуса с FG на BG.
  Токен: `lens breathing on rack focus shift, subtle zoom-pulse during focus transition`
* **Chromatic Aberration (Peripheral):** Расщепление цветов по краям. Убирает «цифровую чистоту».
  Токен: `subtle peripheral chromatic aberration, RGB fringe at frame edges`
* **Anamorphic Blue Flare:** Горизонтальный синий блик. Голливудский экшен.
  Токен: `anamorphic blue horizontal lens flare from key light source`
* **Heat Haze Distortion:** Дрожание воздуха над нагретыми поверхностями.
  Токен: `heat haze shimmer above hot surface, air distortion ripple`

---

## IV. MOTION DYNAMICS (Динамика движения)

* **Parallax Shift Alignment:** FG быстро, BG медленно.
  Токен: `parallax shift — foreground fast, background slow drift`
* **Organic Handheld Micro-shake:** Естественное дрожание рук оператора.
  Токен: `organic handheld micro-shake, camera operator breathing vibration`
* **Motion Blur Tail:** «Хвост» размытия при быстром движении.
  Токен: `directional motion blur tail on fast-moving subject, velocity streak`

---

## V. ULTRA-HIGH-END OPTICS (The "Cooke" Look)

* **Cooke S4 Anamorphic Rendering:** Мягкий спад резкости к краям, «тёплое» изображение.
  Токен: `Cooke S4 anamorphic rendering, warm image rendition, soft edge fall-off`
* **Negative Fill (Cinematic Shadow):** Глубокие тени на одной стороне объекта.
  Токен: `strong negative fill on the shadow side for high-contrast drama`
* **Speed Ramping (Time Remapping):** Изменение частоты кадров.
  Токен: `sudden speed ramp from 24fps real-time to 120fps extreme slow-motion`
* **Caustic Light Refraction:** Узоры света через воду или стекло.
  Токен: `caustic light refraction pattern through glass surface`

---

## VI. LIGHTING PRESETS (Готовые световые связки)

Готовые пресеты для быстрой вставки в промпт.
Выбери пресет → скопируй строку токенов → вставь в блок освещения.

---

### PRESET 01 — NOIR
> Детектив, триллер, криминальная драма. Жёсткие тени, минимум заполняющего света.

    Tokens: Chiaroscuro — hard key light from 45-degree angle, strong negative fill
    on shadow side, cold 5600K practical light, deep underexposed background,
    subtle rim light defining silhouette edge.

---

### PRESET 02 — GOLDEN HOUR
> Природа, романтика, эпические финалы. Тёплый боковой свет.

    Tokens: Warm 3200K key light from low horizontal angle, Rim Lighting — golden
    edge highlight on subject contour, Volumetric God Rays through dust or haze,
    Global Illumination — warm bounce from ground surface, Teal & Orange Grade.

---

### PRESET 03 — INDUSTRIAL / FORGE
> Металл, огонь, производство, лава. Практические источники света.

    Tokens: Sodium vapor practical light — warm 2700K dominant source, strong negative
    fill on opposite side, heat haze shimmer above hot surfaces, Volumetric God Rays
    through smoke column, underexposed background with spot illumination only.

---

### PRESET 04 — NEON NOIR (Cyberpunk)
> Ночной город, неон, дождь. Цветной отражённый свет.

    Tokens: Global Illumination — neon colour bounce on wet asphalt, teal and magenta
    practical lights as key sources, Volumetric God Rays through rain and fog,
    caustic light refraction pattern in puddles, deep shadow zones between light pools,
    subtle peripheral chromatic aberration.

---

### PRESET 05 — CLINICAL / COLD
> Лаборатория, sci-fi, хоррор. Холодный равномерный свет без теней.

    Tokens: Cold 6500K overhead fluorescent key light, minimal shadow depth,
    Global Illumination — flat even bounce, subtle Rim Lighting from below,
    no warm tones, desaturated background, occasional flicker on practical sources.

---

### PRESET 06 — MACRO STUDIO
> Крупный план продукта, капли, материалы. Контролируемый студийный свет.

    Tokens: Rim Lighting — dual edge lights left and right, soft box key light
    from above at 90 degrees, caustic light refraction pattern through subject,
    Global Illumination — clean white bounce, no coloured gels, Specular
    Micro-geometry highlights on surface details.

---

### PRESET 07 — APOCALYPTIC / OVERCAST
> Постапокалипсис, война, разрушение. Рассеянный серый свет.

    Tokens: Overcast diffused daylight — flat 7000K grey key light, no direct
    shadows, Volumetric God Rays through smoke and ash, micro-dust illumination
    in backlit shaft, Brownian motion particle drift, desaturated colour grade,
    cold rim light from distant fire source.

---

### БЫСТРАЯ ТАБЛИЦА ВЫБОРА

| Настроение | Пресет | Ключевой токен |
|---|---|---|
| Детектив / триллер | NOIR | `Chiaroscuro, strong negative fill` |
| Закат / природа | GOLDEN HOUR | `Warm 3200K, Rim Lighting golden` |
| Металл / огонь | INDUSTRIAL | `Sodium vapor 2700K, heat haze` |
| Ночной город | NEON NOIR | `GI neon bounce, caustic puddles` |
| Лаборатория / sci-fi | CLINICAL | `Cold 6500K, flat GI bounce` |
| Продукт / макро | MACRO STUDIO | `Dual Rim Light, soft box 90°` |
| Постапокалипсис | APOCALYPTIC | `Overcast 7000K, ash particles` |
