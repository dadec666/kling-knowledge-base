# CHANGELOG — KLING 3.0 KNOWLEDGE BASE

---

## v8.3 (2026-03-27)

### Исправлено
~ `Kling-Technical-Specs.md` — III. Dual-Frame Pipeline полностью переписан:
  - Платформа уточнена: RunwayML (app.runwayml.com)
  - Убрана недоступная настройка Image Guidance (0.8-1.0)
  - Заменена на Consistency Anchors (текстовые якоря)
  - Добавлены три сценария генерации End Frame (A / B / C)
~ `Prompt-Engineering-Standard.md` — VII. Negative Prompting:
  - Добавлено платформенное ограничение RunwayML
  - Добавлена таблица сцено-специфичных inline-негативов

---

## v8.2 (2026-03-27)

### Добавлено
+ `Visual-Effects-Library.md` — VII. FLUID-SOLID INTERACTION PHYSICS
  - A. Wetting & Adhesion: Contact Angle Dynamics, Hydrophobic Repulsion, Capillary Creep
  - B. Impact Dynamics: Crown Splash Dynamics, Worthington Jet, Rebound Droplet Satellites
  - C. Thermal Contact Physics: Vapour Flash Boundary, Thermal Expansion Cracking, Ablation Trail
  - D. Residue & Surface Memory: Viscous Stringing, Meniscus Tear, Tide Mark / Residue Ring
+ `Visual-Effects-Library.md` — VIII. COMBUSTION & FIRE PHYSICS
  - Flame Turbulence, Combustion Color Gradient, Flame Transparency Layering
  - Ember Drift Trajectory, Pyrolysis Smoke Layer, Soot Deposition
  - Burn Propagation Front, Char & Ash Residue
+ `Visual-Effects-Library.md` — IX. HUMAN BODY PHYSICS
  - Micro-expressions, Subsurface Skin Flush
  - Secondary Motion Lag, Fabric Tension Lines
  - Weight Shift, Ground Contact Deformation
+ `Cinematography-VFX-Lexicon.md` — новые Camera Directives
  - Whip Pan, Dutch Tilt, Crash Zoom, Snorricam
+ `Quick-Reference-Card.md` — создан (78 токенов, 11 разделов)
+ `Prompt-Templates-Library.md` — создан (7 шаблонов)

### Изменено
~ `Visual-Effects-Library.md` — Structural Latency получил backtick-токен
~ `Cinematography-VFX-Lexicon.md` — все атмосферные токены (Lens Breathing,
  Micro-dust, Anamorphic Blue Flare и др.) получили готовые backtick-фразы на EN
~ `Prompt-Engineering-Standard.md` — Mandatory Technical Replacements расширен:
  добавлены замены для воды, брызг, лавы, мёда
~ `Prompt-Engineering-Standard.md` — Clean Prompt Rule получил живой пример промпта

---

## v8.1 (дата неизвестна — до начала сессии)

### Добавлено
+ Clean Prompt Rule — цифры секунд запрещены в финальном промпте
+ Audio tags: [Dialogue], [Sound], [Ambient], [Voice]
+ Timeline Scripting (только для внутреннего анализа)
+ Токены: Micro-dust Illumination, Lens Breathing, Structural Latency

### База знаний на момент получения
- Kling-Technical-Specs.md ✅
- Visual-Effects-Library.md ✅
- Prompt-Engineering-Standard.md ✅
- Cinematography-VFX-Lexicon.md ✅

---

## v8.0 и ранее

История до v8.1 не восстанавливается.
Зафиксировано: база содержала физику Non-Newtonian, SSS, Cooke Look,
Anchor Rule, Forbidden Tokens, Dual-Frame Pipeline.

---

*Следующая версия: v8.3 — System Prompt интеграция*