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

---

## X. GLASS & TRANSPARENCY PHYSICS (Физика стекла и прозрачности)

### A. Optical Properties (Оптические свойства)

* **Fresnel Effect:** Отражение зависит от угла зрения — под прямым углом
  стекло прозрачно, под острым становится зеркальным.
  Токен: `Fresnel reflectance shift — transparent at normal incidence,
  mirror-like at grazing angle`

* **Internal Refraction:** Объекты за стеклом искажаются — смещаются,
  раздваиваются, меняют цвет на границе материала.
  Токен: `internal refraction distortion through glass body,
  object displacement and chromatic shift at material boundary`

* **Caustic Projection:** Концентрированные узоры света на поверхности
  за стеклом — движутся при изменении угла освещения.
  Токен: `caustic light projection through glass onto receiving surface,
  dynamic focus pattern shifting with light angle`

---

### B. Surface States (Состояния поверхности)

* **Condensation Micro-droplets:** Мельчайшие капли конденсата на холодном
  стекле — неравномерные, с Contact Angle Dynamics на каждой капле.
  Токен: `condensation micro-droplets on cold glass surface,
  hydrophilic flat meniscus, irregular distribution`

* **Smear & Fingerprint Residue:** Жировые разводы и отпечатки пальцев —
  видны только под определённым углом освещения (Fresnel зависимость).
  Токен: `fingerprint smear residue on glass — visible only at
  oblique lighting angle, thin-film iridescence on grease trace`

* **Frost Crystal Growth:** Кристаллы инея растут от краёв к центру
  по дендритным паттернам — каждый кристалл с анизотропным бликом.
  Токен: `frost crystal dendritic growth across glass surface,
  anisotropic highlight on each ice facet`

---

### C. Fracture Dynamics (Динамика разрушения)

* **Spider Web Fracture:** Паутина трещин расходится радиально от точки
  удара — основные трещины с концентрическими кольцами между ними.
  Токен: `spider web fracture pattern radiating from impact point,
  concentric ring cracks between radial lines`

* **Shatter Fragment Scatter:** Осколки разлетаются конически от точки
  удара — каждый фрагмент с острыми гранями и Fresnel бликами.
  Токен: `glass shatter fragment scatter — conical ejection trajectory,
  sharp edge Fresnel highlights on each shard`

* **Laminate Delamination:** Многослойное стекло не рассыпается —
  слои расходятся, между ними появляется воздушная прослойка с иридесценцией.
  Токен: `laminate glass delamination — layers separating with
  thin-film iridescence in air gap between plies`

---

### D. Liquid-Glass Interaction (Жидкость на стекле)

* **Rain Streak Channeling:** Капли дождя сливаются в ручейки —
  путь определяется микрорельефом поверхности, не гравитацией.
  Токен: `rain streak channeling on glass — droplet merging into
  rivulets guided by surface micro-texture, not gravity alone`

* **Wiper Arc Residue:** После удара дворника остаётся тонкая плёнка
  с радужными разводами — граница чистого и грязного стекла.
  Токен: `wiper arc residue boundary — thin film iridescence
  at clean-dirty glass transition line`

---

## XI. FABRIC & CLOTH PHYSICS (Физика ткани и одежды)

### A. Drape & Weight (Драпировка и вес)

* **Cloth Drape Simulation:** Ткань падает под весом — форма складок
  зависит от плотности материала. Шёлк течёт плавно, деним держит форму.
  Токен: `cloth drape simulation — fabric weight defines fold radius,
  silk fluid cascade vs denim rigid crease geometry`

* **Bias Cut Distortion:** Ткань скроенная по диагонали тянется
  иначе — складки идут под 45 градусов, силуэт живёт при движении.
  Токен: `bias cut fabric distortion — 45-degree grain fold lines,
  silhouette breathing with body movement`

* **Hem Oscillation:** Нижний край ткани колышется с запаздыванием
  после основного движения — амплитуда зависит от длины и веса.
  Токен: `hem oscillation trailing behind primary body motion,
  amplitude decay proportional to fabric length and weight`

---

### B. Wind & Air Interaction (Ветер и воздух)

* **Wind Billow:** Ткань наполняется воздухом — выпуклые паруса
  с чёткой границей натяжения по краям.
  Токен: `wind billow inflation — convex fabric sail with tension
  line at leading edge, trailing hem flutter`

* **Turbulent Flutter:** Хаотичное дрожание лёгкой ткани в турбулентном
  потоке — не периодическое, а случайное по частоте и амплитуде.
  Токен: `turbulent fabric flutter — aperiodic frequency variation,
  random amplitude micro-oscillation on lightweight material`

* **Vortex Wrap:** Ткань закручивается вокруг тела при резком повороте —
  инерция тянет её по касательной к траектории движения.
  Токен: `vortex wrap — fabric inertia tangential lag on rapid
  body rotation, wrap-around trailing edge`

---

### C. Tension & Stress (Натяжение и нагрузка)

* **Fabric Tension Lines:** Складки концентрируются в точках натяжения —
  рукав при поднятии руки, колено при шаге, плечо при повороте.
  Токен: `fabric tension fold convergence at stress points —
  sleeve pull on arm raise, knee gather on stride`

* **Seam Stress Deformation:** Швы стягивают ткань при нагрузке —
  видна деформация по линии шва, нитки натянуты.
  Токен: `seam stress deformation under load — fabric distortion
  along stitch line, thread tension visible at joint`

* **Stretch Recovery:** Эластичная ткань возвращается в форму после
  растяжения — с лёгкой вибрацией и остаточными складками.
  Токен: `elastic fabric stretch recovery — rebound oscillation
  with residual crease memory after deformation`

---

### D. Wet & Soiled States (Мокрая и загрязнённая ткань)

* **Wet Fabric Adhesion:** Мокрая ткань прилипает к телу — повторяет
  контуры под ней, темнеет, теряет воздушность складок.
  Токен: `wet fabric adhesion to body surface — form-revealing
  drape, darkened saturation, collapsed fold volume`

* **Mud Splash Absorption:** Грязь впитывается в ткань неравномерно —
  пятно расплывается по волокнам через Capillary Creep.
  Токен: `mud splash absorption into fabric weave — irregular
  stain boundary spreading via capillary creep through fibres`

* **Drying Tide Mark:** После высыхания остаётся светлый контур
  по границе пятна — минеральный осадок по краю.
  Токен: `drying tide mark on fabric — pale mineral residue ring
  at former wet boundary after evaporation`
