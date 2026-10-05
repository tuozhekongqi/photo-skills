# Great Wall Batch Stress Test — Decision Engine Example

## User-version interpretation

This is a planning example, not evidence of newly generated images. Assume the user permits batch culling. Every retained source uses normal A + strong B. T0/T1 describes photographic restraint only; all final layouts require both strong-design relations. A–L are B family labels, not the ABC route. Quiet frames remain strongly designed pages.

Purpose: verify that ten photos from one destination do **not** collapse into one style merely because the subject is the Great Wall.

This test intentionally uses visual behavior, near-duplicate culling, transformability, and batch rebalancing.

## Input overview

10 source photos include:
- cable cars over a forested valley;
- several through-window Great Wall / hillside views;
- broad mountain ridges and sky;
- winding Great Wall sections;
- a destination marker / heritage sign;
- a busy terrace / lookout under dramatic cloud.

## Deduplication pass

### Keep 01 — cable cars descending into the valley
Unique directional / motion image.

### Skip 02 — wall high on ridge, heavy window reflection
Reason: weaker than neighboring wall/ridge views and adds little new visual behavior.
Status: `skipped-low-value`.

### Skip 03 — similar ridge/wall view through cable-car window
Reason: near-duplicate visual purpose with stronger later wall/ridge frames.
Status: `skipped-near-duplicate`.

### Skip 04 — sweeping wall across mountain, but similar to 05
Reason: 05 presents the wall and mountain relationship more clearly with less competing cable hardware.
Status: `skipped-near-duplicate`.

### Keep 05 — wall sweeps across mountain with dramatic cloud
Strong wall rhythm + depth + sky.

### Keep 06 — mountain ridges with enormous blue sky
Different visual behavior: landscape scale and negative space, wall not dominant.

### Keep 07 — wall climbing a ridge under large open sky
Different geometry from 05; strong graphic route / silhouette.

### Keep 08 — heritage destination stone marker with visitors
Unique souvenir / arrival memory.

### Keep 09 — lookout terrace, people, mountains, radiant cloud
Unique human movement + cinematic atmosphere.

### Keep 10 — vertical view of wall threading through green mountains
Unique orientation and winding-depth behavior.

Selected: 7 / 10.

---

## Decision table

| src | strongest visual behavior | archetype | T | primary | score | secondary | score | final reason |
|---|---|---|---|---|---:|---|---:|---|
| 01 | cable lines pull the eye into a deep green valley | V2 + V10 | T3 | D Second World | 92 | H Cinematic | 85 | actionable cable geometry supports a real concept |
| 05 | wall rhythm crosses layered ridges beneath dramatic cloud | V2 + V1 | T1 | G Light Poetry | 90 | H Cinematic | 86 | atmosphere and breathing sky are stronger than graphic restyling |
| 06 | mountain silhouette sits below a huge uninterrupted sky | V1 | T0 | G Light Poetry | 95 | H Cinematic | 80 | the photo is already strong; preserve it |
| 07 | wall forms a clear route across a graphic mountain silhouette | V2 + V8 | T2 | C Minimal Collage | 87 | G Light Poetry | 84 | geometry can be clarified without overpainting the landscape |
| 08 | landmark marker functions as an arrival / souvenir memory | V7 + V11 | T1 | A Travel Ticket | 88 | J Magazine | 82 | collectible travel-memory logic is natural here |
| 09 | human movement leads into mountains beneath theatrical cloud | V10 + V1 | T0 | H Cinematic | 92 | E Analog | 83 | timing and atmosphere matter more than poster graphics |
| 10 | wall snakes through dense green ridges in a vertical frame | V2 + V9 | T2 | I Modern Chinese | 86 | B Watercolor | 82 | cultural geometry + natural material palette support a restrained heritage treatment |

---

## Batch rebalancing result

Final families:
`D, G, G, C, A, H, I`

This intentionally allows G twice because both are high-confidence local fits but their layouts should differ:
- 05 -> `ASYMMETRIC_EDITORIAL` with photo/space construction and restrained reading hierarchy;
- 06 -> text-free `GRAPHIC_FIELD` with asymmetric intact photo placement and a source-derived axis/space rhythm.

Layout signatures should be:
1. 01 — `TOP_PHOTO_BOTTOM_PAPER` (Second World)
2. 05 — `ASYMMETRIC_EDITORIAL` + clear page reading hierarchy
3. 06 — text-free `GRAPHIC_FIELD` + source-derived spatial rhythm
4. 07 — `GRAPHIC_FIELD`
5. 08 — `TICKET_DIPTYCH`
6. 09 — `HERO_PLUS_MICROCROP` story page with a meaningful environmental crop from the same source, preserving real people
7. 10 — `EDGE_TRANSITION` or `WHITE_FIELD_PLATE`

Despite one destination, the series contains 6 families and varied qualifying page structures; do not infer a layout count from optional alternatives.

---

## What this test proves

- Same place does not imply same style.
- Some Great Wall photographic masters remain nearly untouched, while every retained final page still meets strong B.
- One strong conceptual image is enough; Second World should not dominate.
- Near-duplicate culling improves the final series more than styling every source.
- Batch diversity should come from visual behavior, not random style rotation.
