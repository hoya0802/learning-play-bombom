# Math Pet Battle Design Baseline

This document is the local design contract for the math pet battle improvement pass. It records the current bright pixel-art direction from the project docs and existing asset inventory; it does not introduce a new brand direction and does not reference an unavailable concept image.

## Scope Guardrails

- Keep the app static and single-file-first for this pass. No React, Vite, or other framework migration is in scope.
- Design every screen first for iPad Pro 11-inch landscape at 1194x834 CSS pixels. This is the default layout, text, spacing, and touch-target working size.
- Keep desktop battle checks at 1366x768 and 1440x900 as expansion targets, with 1024x768 as a secondary tablet regression check.
- Do not start a mobile redesign. Only prevent obvious breakage below the iPad Pro 11-inch baseline unless a mobile pass is explicitly requested.
- Keep the first problem wave inside scalar multiple-choice. No freeform input, drag/drop, number-line placement, multi-answer, long story layout, fractions/decimals, timed failure mode, or open-ended puzzle boss UI.
- Reuse available math pet battle assets before requesting new art. New assets are only for documented gaps.

## Visual Direction

- Use a bright, friendly pixel-art RPG tone for a lower-elementary learning game.
- Prioritize clear silhouettes, readable characters, and short child-facing copy over decorative density.
- The battle should read as a trainer-supported pet battle: pets and enemies carry the action; the trainer supports from behind.
- Preserve the current local/GitHub Pages asset model by using relative paths and individual image assets.
- Keep UI surfaces consistent across battle, world map, shop, ranch, and location screens through shared frame, button, icon, and state rules.

## Viewports

- 1194x834: primary iPad Pro 11-inch landscape QA and layout target. All app screens, battle actors, side panels, command panel text, home cards, Hanja mode cards, location panels, and choice buttons must be visible, readable, and free of overlap or clipped Korean text.
- 1366x768: desktop expansion QA target. All battle actors, side panels, command panel text, and choice buttons must remain visible without overlap.
- 1440x900: spacious desktop QA target. The arena may breathe more, but actor hierarchy and command-panel proportions must remain intentional.
- 1024x768: secondary tablet regression target. This is no longer the default design baseline; it verifies that text, touch targets, and key battle controls remain usable on narrower tablets.
- Avoid viewport-width font scaling. Use stable dimensions, max-widths, wrapping rules, and fixed control regions so text changes do not resize the battle layout.

## Actor Hierarchy

- Pet: the primary player-side combat actor. The active pet should be larger and more visually central than the trainer, with clear attack, trait, shield, heal, and speed feedback.
- Enemy: the opposing combat actor. It should visually balance the pet and remain fully visible during damage, counterattack, and victory states.
- Trainer: a support character. The trainer can communicate guidance or presence, but should not compete with the pet as the combat focal point.
- Feedback effects: use existing effect assets for correct, wrong, double-hit, shield, heal, speed, enemy impact, damage, reward, and next-stage states where available.
- Motion and effect placement must clarify direction: pet action moves toward enemy; counterattack or damage feedback returns toward the pet side.

## Command Panel

- The bottom command panel is the problem and answer surface. It must stay readable before, during, and after an answer state.
- The prompt area is for the current 문제. Keep it short enough for scalar multiple-choice and allow controlled wrapping for `short-story-choice`.
- Choice buttons are for 선택지. Keep stable sizes for the three-choice layout so correct, wrong, disabled, and pending states do not shift the panel.
- Use pixel frame/button assets where available, with enough internal padding that Korean text and numbers do not touch frame edges.
- Correct answer state should combine color, icon/effect, and copy. Wrong answer state should also combine more than color alone.
- Disabled choices must remain visibly disabled and semantically inactive.

## Side Panels

- The active pet panel should show identity, level, HP/status, role, and current trait or skill in a scannable order.
- Roster slots should clearly distinguish active, available, locked, empty, and disabled states.
- Item and gear panels should distinguish usable, zero-count, equipped, locked, and disabled states without relying only on hover text.
- Essential status must be visible for tablet/touch users.
- Side-panel cards may use pixel frames, but avoid nested card-in-card styling that makes state hierarchy hard to scan.

## Problem Types

- First-wave problem families are scalar multiple-choice only: `add-basic`, `sub-basic`, `make-10`, `missing-addend`, `unknown-position`, `part-part-whole`, `compare-difference`, `three-addends`, `place-value-tens-ones`, and `short-story-choice`.
- Each generated problem must have one scalar answer and three distinct choices that include the answer.
- Preserve compatibility with legacy `{ text, answer }` questions and `state.math.choices`.
- Short story prompts may be used only when they fit the command panel without a new renderer.
- Later formats such as number lines, drag/drop models, multi-answer questions, freeform input, fractions/decimals, and long story problems require a separate renderer and are out of this pass.

## Korean Text

- Korean is the default visible UI language for math pet battle surfaces.
- Keep labels short, child-facing, and UTF-8 clean. Avoid mojibake and avoid adult curriculum jargon in visible UI.
- Required child-facing problem labels include: 더하기, 빼기, 10 만들기, 빈칸 찾기, 큰 수 / 작은 수, 이야기 문제, 자리값.
- Core battle terms should remain understandable: 문제, 선택지, 정답, 오답, 보상, 저장됨, 새로 시작, 다시 하기.
- Save/progress/reset copy must make scope clear: reset or new-start actions affect math battle state only, not unrelated app data.

## State Colors

- Correct: green family, paired with check or burst feedback and affirmative copy.
- Wrong: red family, paired with wrong or puff feedback and recovery/counterattack copy.
- Trait or bonus: yellow/gold family, paired with sparkle, speed, heal, shield, or attack iconography.
- Disabled or locked: muted gray/blue treatment with lower contrast, no active glow, and visible reason text where space allows.
- Active/current: brighter frame, stronger outline, or glow; do not rely on color alone.
- Reward/currency: gold for star coins, gem cyan/blue for answer gems, using the existing currency assets when present.

## Assets

- Prefer individual assets under `assets/math-pet-battle/` over spritesheets when both exist.
- Use `assets/math-pet-battle/ui/single/` for icons and pixel UI pieces, including button, panel, command, nameplate, pet-card, slot, and skill-slot frames where available.
- Use `assets/math-pet-battle/effects/single/` for battle feedback effects.
- Use `assets/math-pet-battle/locations/single/` for world and location landmarks.
- Preserve relative paths so the static file works locally and on GitHub Pages.
- Do not replace current assets with unrelated art or IP-like references. New art must match the bright pixel-art direction and lower-elementary readability.

## Panel, Frame, And Button Rules

- Use pixel frames to clarify functional regions: battle arena, command panel, active pet, roster, items, gear, shop cards, ranch cards, and location states.
- Keep one clear frame layer per surface. Avoid stacking framed panels inside framed panels unless the inner element is an individual repeated item.
- Buttons need stable width/height, visible focus/disabled states, and enough padding for Korean labels.
- Icon-only controls need accessible names or adjacent visible context. Text buttons are acceptable for clear commands such as 새로 시작 or 다시 하기.
- Do not let long numbers or Korean labels resize the command panel, side panels, or roster grid.

## QA Evidence

- Documentation QA for this baseline is grep/readback evidence, saved under `.omo/evidence/task-1-math-pet-battle-improvements-execution.md`.
- Required grep terms include `1194x834`, `iPad Pro 11-inch`, `1366x768`, `1440x900`, `1024x768`, `asset`, and `problem`.
- Manual readback uses:
  `C:\Users\dorab\.local\bin\omo.cmd sparkshell --shell "sed -n '1,220p' DESIGN.md"`
- Later visual tasks must add browser screenshots rather than claiming visual completion from grep alone.
- Screenshot acceptance for later UI work: target viewport named in artifact, every relevant screen captured at 1194x834, actors and primary content fully visible, prompt and choices readable, Korean labels not clipped or awkwardly detached, no text overlap, state distinctions visible, and the relevant guardrails still obeyed.
