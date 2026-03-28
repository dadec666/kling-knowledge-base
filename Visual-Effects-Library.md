# VFX PHYSICS & MATERIAL SCIENCE REGULATION

## I. MATERIAL SHADERS (Surface Properties)

* **Subsurface Scattering (SSS):** Mandatory for organic/translucent surfaces (skin, wax, jelly, Skittles candy).
* **Iridescence / Thin-film:** Rainbow color shifts (oil slicks, soap bubbles, pearl paint, glaze).
* **Anisotropic Highlights:** Linear light streaks on brushed metal, hair, or silk.
* **Clear Coat:** Mirror-like secondary glossy layer over a base material.
* **Ray-Traced Reflections:** Physically accurate environmental reflections.

---

## II. FLUID DYNAMICS (Transformation Physics)

* **High Viscosity:** Thick, heavy, slow-moving flow (lava, honey, Skittles glaze).
* **Marangoni Effect:** Complex flow patterns driven by surface tension (spreading glaze).
* **Viscous Drag:** Visible resistance when a liquid moves over a surface.

---

## III. KINETIC CONSTRAINTS (Anti-Artifact Rules)

* **No-Jelly Rule:** Rigid objects (metal, stone, glass) must maintain structural integrity. No rubbery warping.
* **Momentum & Inertia:** Objects must have perceived weight. Sudden stops are prohibited.
* **Particle Interactions:** Use "Embers", "Dust motes", or "Liquid droplets" to fill the space and add scale.

---

## IV. ADVANCED TRANSFORMATION PHYSICS (Секретные токены)

* **Non-Newtonian Fluid Dynamics:** Используй для морфинга твердых тел в жидкости. Позволяет объекту
  сохранять форму при ударе, но растекаться при медленном движении. Идеально для «ртутных» эффектов.
* **Leidenfrost Effect:** Визуальный эффект «парящих капель». Применяй, когда раскаленный металл или лава
  соприкасаются с холодной поверхностью. Создает слой пара и характерное «бегающее» движение.
* **Structural Latency:** Временная задержка перед деформацией. Придает объекту визуальный вес.
  Токен: `structural latency deformation delay, object resists shape change before yielding`
* **Stress Fractures & Fissures:** Генерация микротрещин на поверхности перед плавлением или взрывом.

---

## V. SURFACE MICRO-DETAILS (Для Nano Banana 2)

* **Specular Micro-geometry:** Мельчайшие неровности для реалистичных бликов. Вместо "shiny".
* **Oxidized Patina:** Для старых металлов. Указывай слой окисления, а не просто «ржавчину».
* **Anisotropic Brushed Grain:** Направленная шлифовка металла. Блики «гуляют» при движении камеры.

---

## VI. MACRO REALISM & IMPERFECTIONS

* **Micro-pores & Peach Fuzz:** Для сверхкрупных планов лиц или кожи (SSS + peach fuzz).
* **Surface Grit & Lens Grime:** Едва заметные царапины или пыль на «объективе».
* **Sub-dermal Scattering:** Глубокий вариант SSS — свет сквозь плоть или густые жидкости.

---

## VII. FLUID-SOLID INTERACTION PHYSICS (Физика контакта жидкости с твёрдым телом)

### A. Wetting & Adhesion (Смачивание и адгезия)

* **Contact Angle Dynamics:** Угол мениска в точке контакта жидкости с поверхностью.
  Токен: `hydrophilic flat meniscus on glass` или `hydrophobic convex bead on wax surface`
* **Hydrophobic Repulsion (Lotus Effect):** Жидкость собирается в шары и скатывается.
  Токен: `water beading on hydrophobic surface, lotus effect repulsion, no wetting`
* **Capillary Creep:** Жидкость «вползает» в трещины и поры под действием капиллярных сил.
  Токен: `liquid capillary creep into surface micro-fissures, slow absorption wicking`

### B. Impact Dynamics (Динамика удара)

* **Crown Splash Dynamics:** Форма «короны» при ударе капли о поверхность.
  Токен: `symmetric crown splash with 12-point corona, rim instability droplets at apex`
* **Worthington Jet:** Вертикальный выброс из центра кратера после удара капли.
  Токен: `Worthington jet rising from impact center, thin liquid column with terminal droplet`
* **Rebound Droplet Satellites:** Микрокапли-спутники, разлетающиеся по конической траектории.
  Токен: `satellite microdroplets ejected radially on impact, sub-millimeter bead scatter`

### C. Thermal Contact Physics (Тепловое взаимодействие)

* **Vapour Flash Boundary:** Облако пара по линии контакта раскалённой жидкости с холодной поверхностью.
  Токен: `vapour flash boundary at liquid-solid contact line, superheated steam burst`
* **Thermal Expansion Cracking:** Радиальные трещины от резкого перепада температур.
  Токен: `radial thermal cracking from contact point, stress lines propagating outward`
* **Ablation Trail:** Выжженный след на поверхности после контакта с горячей жидкостью.
  Токен: `ablation trail seared into surface, charred contact scar with glowing edges`

### D. Residue & Surface Memory (Остаточные следы)

* **Viscous Stringing:** Нити вязкой жидкости между поверхностью и поднимающимся объектом.
  Токен: `viscous stringing between surface and lifting object, elastic liquid filaments`
* **Meniscus Tear:** Момент разрыва поверхностной плёнки с микровибрацией.
  Токен: `meniscus tear at detachment point, surface film rupture with recoil snap`
* **Tide Mark / Residue Ring:** Высохший след жидкости — кольцо из осадка по краям зоны контакта.
  Токен: `dried tide mark residue ring at liquid boundary, mineral deposit edge line`

---

## VIII. COMBUSTION & FIRE PHYSICS (Физика огня и горения)

### A. Flame Structure (Структура пламени)

* **Flame Turbulence:** Хаотичные вихри и завихрения в теле пламени —
  особенно на границе огонь/воздух. Без этого токена огонь выглядит «мультяшным».
  Токен: `turbulent flame vortex at combustion boundary, chaotic fire column instability`
* **Combustion Color Gradient:** Цвет пламени зависит от температуры.
  Синий (ядро, макс. температура) → белый → оранжевый → красный → чёрный дым (периферия).
  Токен: `combustion color gradient — blue core to white to orange to deep red outer edge`
* **Flame Transparency Layering:** Пламя полупрозрачно — сквозь него видны объекты за ним,
  искажённые тепловым маревом.
  Токен: `semi-transparent flame layers with heat haze distortion through fire body`

### B. Ember & Smoke Dynamics (Искры и дым)

* **Ember Drift Trajectory:** Искры поднимаются по спирали вместе с восходящим тепловым потоком,
  замедляются и гаснут — не летят хаотично в стороны.
  Токен: `ember drift on rising thermal column, spiral ascent with fade-out decay`
* **Pyrolysis Smoke Layer:** Густой белый дым от неполного сгорания у основания огня —
  отдельный слой, отличающийся от чёрного дыма продуктов горения.
  Токен: `pyrolysis white smoke at flame base, separate from black combustion exhaust`
* **Soot Deposition:** Чёрный налёт копоти на поверхностях выше зоны горения.
  Токен: `soot deposition streaks above flame source on surrounding surfaces`

### C. Fire-Surface Interaction (Огонь на поверхности)

* **Burn Propagation Front:** Линия горения распространяется по поверхности с видимым фронтом —
  не вся поверхность вспыхивает сразу, а огонь «идёт» по материалу.
  Токен: `burn propagation front spreading across surface, leading edge char line`
* **Char & Ash Residue:** После прохождения огня — чёрная обугленная поверхность с
  пепельным налётом и едва видимыми тлеющими углями.
  Токен: `char and ash residue post-combustion, glowing ember remnants in blackened surface`

  ---

## IX. HUMAN BODY PHYSICS (Физика человеческого тела)

### A. Facial Micro-dynamics (Микродинамика лица)

* **Micro-expressions:** Едва уловимые мимические движения — подёргивание уголка
  рта, прищур, напряжение скул. Делают лицо «живым» между активными движениями.
  Токен: `subtle micro-expression flicker — jaw tension, eye squint, lip corner twitch`
* **Subsurface Skin Flush:** Покраснение кожи от эмоции или нагрева — видимое
  изменение цвета через SSS-слой (не поверхностное).
  Токен: `subsurface skin flush — capillary redness visible through SSS dermis layer`

### B. Secondary Motion (Вторичное движение)

* **Secondary Motion Lag:** Волосы, одежда, украшения, жировые складки реагируют
  на движение тела с инерционной задержкой — не синхронно.
  Токен: `secondary motion lag on hair and clothing, inertial delay after primary body move`
* **Fabric Tension Lines:** Складки ткани возникают в точках натяжения при движении —
  рукав при поднятии руки, колено при шаге.
  Токен: `fabric tension fold lines at stress points during movement`

### C. Weight & Balance (Вес и баланс)

* **Weight Shift:** При ходьбе или повороте тело переносит вес — таз смещается,
  плечи компенсируют. Без этого персонаж выглядит «плавающим».
  Токен: `visible weight shift — hip displacement with shoulder counter-rotation on step`
* **Ground Contact Deformation:** Мягкие части тела (ступни, ягодицы) деформируются
  в точке контакта с поверхностью под весом тела.
  Токен: `ground contact soft tissue deformation under body weight at contact point`