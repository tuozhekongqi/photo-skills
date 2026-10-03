---
name: photo-real-grade
version: 1.4
summary: Preserve the user's original photograph and improve only believable exposure, tonal hierarchy, color, local contrast, and source-supported light. No redesign, no layout, no invented objects, and no synthetic relighting that contradicts the source.
description: "Preserve the user's original photograph and improve only believable exposure, tonal hierarchy, color, local contrast, and source-supported light. No redesign, no layout, no invented objects, and no synthetic relighting that contradicts the source."
license: "Proprietary (All rights reserved; 未经许可不得商用)"
---

# Photo Real Grade Skill

Use this skill when the user wants **the same photograph preserved**, with only the corrections that genuinely help. A valid A result may be almost unchanged from the source. The default is not “make it more dramatic”; it is “keep what already works and remove only what weakens it.”

## Routing rule
Use A when the request means: 调光影 / 调色 / 修得更好看但仍然真实 / 不改变原图 / 电影感但不要 AI 味.

A itself does **not** perform magazine pages, paper textures, collage, typography, souvenir cards, Second World illustration, or other graphic redesign; those belong to Skill B. Under the shared default routing, A runs **together with B** for non-portrait images, and with **B + C** when a clear portrait/person subject is present. Source quality or low correction need may reduce A to near-no-op, but must not remove B or C from the default route. Only an explicit user module override changes the combination.

## Non-negotiable constraints
1. Preserve composition, crop intent, perspective, geometry, scene content, architecture, people, signage, historical traces, water/sky structure, and object identity.
2. Do not add/remove/replace subjects unless the user explicitly asks.
3. Do not invent a sun, sunbeam, rim light, reflection, fog, rain, depth-of-field, shadow, lens flare, or golden-hour condition that the source does not plausibly support.
4. Preserve the original direction of light. Strengthen only light that can be explained by the source scene.
5. Avoid HDR flattening, fake microcontrast, over-sharpening, plastic textures, painterly surfaces, global orange/teal washes, crushed featureless blacks, and clipped white highlights.
6. Shadows may be deep, but should retain enough structure to feel photographic. Highlights may be bright, but should keep texture where the source contains it.
7. Local color separation is preferred over a single global color cast. Warm light may coexist with cooler ambient shadow when physically plausible.
8. Grain/noise is not a default. Keep clean digital texture unless the source already has texture or the user explicitly asks for film character.
9. When uncertain, preserve source identity first. **Default to the minimum useful intervention.** Stronger cinematic shaping is allowed only when the source already contains that light/contrast and the current user intent clearly benefits from it. Realism outranks drama.


## Evaluation / feedback mode
When the user is reviewing prior outputs rather than asking for a new edit, enter **evaluation mode** and do not generate automatically. Use `references/feedback-loop.md`, `references/feedback-ledger.md`, and the shared `../FEEDBACK_ABSORPTION_POLICY.md`. New feedback must be scoped and bounded; recency alone never increases its weight.

The feedback loop must distinguish:
- source-fidelity failure;
- cinematic-intensity mismatch;
- people / clutter selection error;
- color or light realism error;
- local execution error versus a bad overall direction.

Use semantic people handling rather than a distance-only rule: preserve edge/back-facing figures that add scale or quiet lived-in atmosphere, even if relatively near; remove figures mainly when they compete with the actual subject. This is a conditional composition rule, not a blanket “keep/remove people” policy.

## Lightweight memory policy
See `references/image-memory-policy.md` for the storage contract.

- **Images are expensive context.** Keep images only when they are strong positive references or exceptionally representative failure examples.
- User ratings such as “还行”, “一般”, or nuanced criticism are primarily converted into text rules, not retained as image libraries.
- A “还行” result may contribute one useful principle while its weak parts become a warning; it does not enter the positive image library unless the user later upgrades it.
- A “一般” result should normally leave **no image** in the package. Record the diagnosis in text and discard the image.
- Never create a secondary-image library. Never retain teaching/research screenshots once their useful principles are already summarized in the skill.

## Core principle
**Preserve first; improve only what needs improvement.**

A no-op / near-original result is valid when the photograph is already strong. Do not search for an edit merely because the tool can make one.

The target is a believable photograph with stronger visual direction: a clear subject, readable depth, controlled highlights, anchored blacks, and color relationships that feel intentional without looking generated.

## Required workflow
1. First ask whether the source actually needs correction. If not, keep it essentially original. If yes, identify only the few issues that materially weaken it.
2. Decide whether the scene supports a light-led grade. If not, prefer subtle exposure/color correction rather than manufactured drama.
3. Protect source identity first; adjust global exposure second; shape local light third; refine color fourth; add texture only last and only if justified.
4. Compare against the source after every major change: if architecture, faces, foliage, water, clouds, text, or object edges appear rewritten, back off.
5. Final authenticity pass: ask whether the image could plausibly be a careful Lightroom/Camera Raw grade of the same frame.

## Light logic learned from the user's preferred examples
- Backlight/side-backlight: preserve the scene, deepen surrounding values moderately, and let existing edge light or reflections carry the subject. Do not paint a new halo around everything.
- Golden-hour street light: long shadows and warm pavement can create depth; keep neutral/cool materials from turning uniformly orange.
- Overcast scenes: do not fake sunset. Use restrained local contrast, subtle temperature separation, and clearer water/sky/architecture tonality.
- Hard directional light: shadow can be a compositional shape. Do not automatically lift all shadows.
- Indoor/street night: warm practical lights may sit against cooler ambient areas, but avoid exaggerated orange/teal grading.
- Portraits: facial texture and natural asymmetry survive. No beauty-retouch flattening unless requested.

## User-validated reference policy
`reference-library/positive/` contains only a compact set of user-approved image references. Learn the **reason** each image worked; do not turn any one image into a universal preset.

`reference-library/cautionary/` is intentionally tiny. It stores only a few archetypal visual failures that are easier to understand as images than as prose. Most negative, secondary, and “general” feedback is stored as text in `references/feedback-ledger.md` and `references/negative-patterns.md`.

Do not build large secondary/research screenshot libraries inside the distributable skill. Once useful lessons have been extracted into text, the source research images should be removed from the runtime package. This keeps the skill portable and prevents historical examples from silently becoming style targets.

## Heritage architecture module
For palace / temple / traditional architecture, apply the conditional rules in `references/heritage-architecture-look.md`. The module emphasizes real weather, architectural geometry, deep-but-readable shadows, stable red/gray/gold relationships, authentic surface texture, and semantic people handling. It is not a preset and must not override source fidelity.
