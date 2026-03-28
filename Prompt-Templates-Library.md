# KLING 3.0 — PROMPT TEMPLATES LIBRARY (v1.0)
> Готовые скелеты промптов под типовые сцены.
> Замени [ANCHOR], [MATERIAL], [LOCATION] на свои значения — и 80% промпта готово.
> Все шаблоны соответствуют CLEAN PROMPT RULE.

---

## КАК ИСПОЛЬЗОВАТЬ

1. Выбери нужный шаблон по типу сцены
2. Замени все [ЗАГЛУШКИ] на конкретные значения
3. Удали ненужные опциональные строки (помечены ★)
4. Проверь: нет цифр секунд в финальном блоке → готово

---

## TEMPLATE 01 — LIQUID TRANSFORMATION
> Твёрдый объект трансформируется в жидкость (плавление, морфинг, растворение)
> Режим: 10s или 15s | Интенсивность: Natural → Cinematic

### Внутренний анализ (не копировать в Kling):
- 0-3s: Anchor в статике, микровибрации, stress fractures появляются
- 3-10s: Structural Latency → деформация → Non-Newtonian flow
- 10-15s: Финальное состояние жидкости, residue, аудио-тег

### Финальный промпт:
Initial state: [ANCHOR — точное название объекта], [MATERIAL shader — напр. anisotropic
brushed grain on surface], surface grit, Zero-Motion Anchor. THEN structural latency
deformation delay — [ANCHOR] resists shape change, stress fractures and fissures spread
across surface. FOLLOWED BY Non-Newtonian fluid dynamics — object collapses into
[TARGET LIQUID — напр. molten chrome / dark honey / liquid mercury], high viscosity flow,
Marangoni Effect spreading pool, viscous stringing at separation points. FINALLY
[CAMERA MOVE — напр. Dolly Pull], Cooke S4 anamorphic rendering, lens breathing on
rack focus shift, dried tide mark residue ring at liquid boundary.
[Sound: [SOUND — напр. metallic groan, liquid hiss]] [Ambient: [ENV — напр. industrial hum]]
No jelly-like distortion, no flickering, no sudden frame jumps.

---

## TEMPLATE 02 — IMPACT MACRO
> Удар капли/снаряда о поверхность. Макросъёмка, гиперреализм.
> Режим: 5s или 10s | Интенсивность: Cinematic

### Внутренний анализ:
- 0-1s: Капля/объект в воздухе, Zero-Motion Anchor на поверхности
- 1-3s: Момент удара — Crown Splash, Worthington Jet
- 3-5s: Satellite microdroplets, residue, рапид

### Финальный промпт:
Initial state: [ANCHOR — напр. single water droplet / mercury bead] suspended above
[SURFACE — напр. still water surface / black granite slab], 85mm macro lens,
Global Illumination, Rim Lighting from behind. THEN impact — symmetric crown splash
with 12-point corona, rim instability droplets at apex, Worthington jet rising from
impact center with terminal droplet. FOLLOWED BY satellite microdroplets ejected
radially, sub-millimeter bead scatter, sudden speed ramp from 24fps real-time to
120fps extreme slow-motion. FINALLY [CAMERA MOVE — напр. Rack Focus to residue],
hydrophilic flat meniscus settling on surface, caustic light refraction pattern,
micro-dust illumination in backlit shaft.
[Sound: [SOUND — напр. sharp liquid crack, crystalline ring]] [Ambient: [ENV — напр. silence, room tone]]
No flickering, no floating debris.

---

## TEMPLATE 03 — VEHICLE REVEAL
> Кинематографичный reveal автомобиля, мотоцикла или техники.
> Режим: 10s или 15s | Интенсивность: Natural

### Внутренний анализ:
- 0-3s: Anchor в статике, детали материала, атмосфера
- 3-10s: Движение + движение камеры
- 10-15s: Финальный ракурс, optical exit

### Финальный промпт:
Initial state: [ANCHOR — напр. 1967 black Ford Mustang fastback], anisotropic brushed
grain on hood, specular micro-geometry on chrome details, surface grit and lens grime,
Zero-Motion Anchor. [LIGHTING — напр. Warm 3200K key light, strong negative fill on
shadow side, Volumetric God Rays through dust]. THEN [MOTION — напр. engine ignites,
exhaust vapour flash boundary at pipe exits, heat haze shimmer above hood].
FOLLOWED BY [CAMERA MOVE — напр. low-angle Dolly Push along driver side],
parallax shift — foreground fast, background slow drift, Cooke S4 anamorphic rendering,
anamorphic blue horizontal lens flare from headlights. FINALLY speed ramp to 120fps
slow-motion on wheel spin, lens breathing on rack focus shift to rear badge,
subtle peripheral chromatic aberration.
[Sound: [SOUND — напр. V8 idle rumble, tyre creak on asphalt]] [Ambient: [ENV — напр. desert wind, garage echo]]
No brand hallucination, no flickering.

---

## TEMPLATE 04 — CHARACTER SPEAKING (LIP-SYNC)
> Персонаж говорит в камеру. Портретный крупный план.
> Режим: 10s или 15s | Интенсивность: Static / Micro

### Внутренний анализ:
- 0-3s: Anchor лица, микроэмоции, установка освещения
- 3-10s: Речь + micro-expressions
- 10-15s: Финальная реакция, затухание

### Финальный промпт:
Initial state: [ANCHOR — напр. young woman, sharp cheekbones, dark eyes],
Subsurface Scattering (SSS), micro-pores, peach fuzz on skin, 85mm portrait lens,
[LIGHTING — напр. Chiaroscuro — warm key light right, deep negative fill left].
THEN [CHARACTER] speaks directly to lens, high-fidelity lip synchronization,
natural jaw movement, subtle micro-expression flicker — jaw tension, eye squint,
lip corner twitch. FOLLOWED BY secondary motion lag on hair, inertial delay,
subsurface skin flush — capillary redness visible through SSS dermis layer.
FINALLY Rack Focus from eyes to lips, lens breathing on focus transition,
[CAMERA MOVE — напр. slow Dolly Pull reveal].
[Dialogue: "[ТЕКСТ РЕПЛИКИ]"] [Voice: [TONE — напр. authoritative / whispering]]
[Ambient: [ENV — напр. quiet room, distant city hum]]
No limb duplication, no flickering.

---

## TEMPLATE 05 — FIRE & DESTRUCTION
> Объект горит, взрывается или разрушается огнём.
> Режим: 10s или 15s | Интенсивность: Hyper / Chaos

### Внутренний анализ:
- 0-3s: Anchor в статике, stress fractures начинаются
- 3-8s: Возгорание, burn propagation front, flame turbulence
- 8-15s: Пик огня + debris, рапид, остаточные следы

### Финальный промпт:
Initial state: [ANCHOR — напр. wooden cabin / steel bridge / abandoned car],
[MATERIAL — напр. oxidized patina on metal / aged wood grain], surface grit,
Zero-Motion Anchor. THEN stress fractures and fissures spread across surface,
burn propagation front advancing from [ORIGIN — напр. lower left corner],
turbulent flame vortex at combustion boundary, combustion color gradient —
blue core to white to orange to deep red outer edge. FOLLOWED BY pyrolysis white
smoke at flame base, ember drift on rising thermal column spiral ascent,
soot deposition streaks on surrounding surfaces, [CAMERA MOVE — напр. Orbit Shot
at mid-level], Volumetric God Rays through smoke, micro-dust illumination in
backlit shaft. FINALLY sudden speed ramp to 120fps on peak flame moment,
char and ash residue post-combustion, glowing ember remnants in blackened surface,
Chiaroscuro lighting, strong negative fill on shadow side.
[Sound: [SOUND — напр. crackling fire, structural groan, glass shattering]]
[Ambient: [ENV — напр. wind feeding the fire, distant sirens]]
No jelly-like distortion, no floating debris, no sudden frame jumps.

---

## TEMPLATE 06 — ATMOSPHERIC ENVIRONMENT
> Живая среда без главного объекта: природа, улица, интерьер.
> Режим: 10s или 15s | Интенсивность: Static / Micro

### Внутренний анализ:
- 0-5s: Установка атмосферы, spatial layering
- 5-15s: Медленное движение камеры, накопление деталей

### Финальный промпт:
Initial state: [LOCATION — напр. rain-soaked Tokyo alley at night / desert highway at dusk],
Foreground: [FG DETAIL — напр. rain droplets on lens, neon reflection in puddle].
Midground: [MG DETAIL — напр. steam rising from grate, distant figure].
Background: [BG DETAIL — напр. city lights bokeh, moving traffic streaks].
Global Illumination — [LIGHT SOURCE — напр. neon signs bouncing on wet asphalt],
Teal & Orange Grade, Volumetric God Rays through [MEDIUM — напр. rain / fog / dust].
THEN [CAMERA MOVE — напр. slow Dolly Push through alley], parallax shift —
foreground fast, background slow drift, organic handheld micro-shake,
micro-dust illumination in backlit shaft, Brownian motion particle drift.
FOLLOWED BY Rack Focus from FG droplets to MG subject, lens breathing on
focus transition, subtle peripheral chromatic aberration. FINALLY [EXIT MOVE —
напр. Crane up reveal of full skyline], heat haze shimmer above [HEAT SOURCE —
напр. neon signs / car hoods].
[Ambient: [ENV — напр. rain hitting asphalt, distant traffic, wind through alley]]
No flickering, no sudden frame jumps.

---

## TEMPLATE 07 — THERMAL CONTACT (лава / металл / кислота)
> Раскалённая жидкость встречает холодную твёрдую поверхность.
> Режим: 10s или 15s | Интенсивность: Cinematic

### Внутренний анализ:
- 0-2s: Anchor поверхности, Leidenfrost эффект уже присутствует
- 2-8s: Контакт — vapour flash, thermal cracking, ablation
- 8-15s: Растекание, residue ring, остывание

### Финальный промпт:
Initial state: [ANCHOR SURFACE — напр. cold black basalt slab / frozen steel plate],
[MATERIAL — напр. oxidized patina, surface grit], Zero-Motion Anchor,
Leidenfrost Effect micro-droplets hovering above surface. THEN [LIQUID —
напр. molten lava flow / liquid white-hot metal] makes contact — vapour flash
boundary at liquid-solid contact line, superheated steam burst, radial thermal
cracking from contact point, stress lines propagating outward. FOLLOWED BY
ablation trail seared into surface, charred contact scar with glowing edges,
Non-Newtonian high viscosity spread, Marangoni Effect at flow edge,
[CAMERA MOVE — напр. low-angle Dolly Push tracking the flow front],
heat haze shimmer above contact zone. FINALLY dried tide mark residue ring
at liquid boundary, mineral deposit edge line, Cooke S4 anamorphic rendering,
Volumetric God Rays through steam column.
[Sound: [SOUND — напр. hissing steam, deep crackling, stone fracture]]
[Ambient: [ENV — напр. volcanic rumble / industrial furnace hum]]
No jelly-like distortion, no flickering.

---

## БЫСТРЫЙ ВЫБОР ШАБЛОНА

| Сцена | Шаблон | Режим | Интенсивность |
|---|---|---|---|
| Объект плавится / морфирует | TEMPLATE 01 | 10-15s | Natural → Cinematic |
| Капля ударяет о поверхность | TEMPLATE 02 | 5-10s | Cinematic |
| Reveal автомобиля / техники | TEMPLATE 03 | 10-15s | Natural |
| Персонаж говорит в камеру | TEMPLATE 04 | 10-15s | Static / Micro |
| Огонь / взрыв / разрушение | TEMPLATE 05 | 10-15s | Hyper / Chaos |
| Живая среда / атмосфера | TEMPLATE 06 | 10-15s | Static / Micro |
| Лава / металл касается поверхности | TEMPLATE 07 | 10-15s | Cinematic |

---

*v1.0 | Обновлено: 2026-03-27 | Шаблонов: 7*
