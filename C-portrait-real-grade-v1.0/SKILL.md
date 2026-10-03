---
name: portrait-real-grade
version: 1.0
summary: Preserve human identity and natural portrait realism while making only believable, low-strength refinements to skin, hair, clothing response, body presentation, and person-specific light. Designed to run with A and B when a clear portrait/person subject is present.
description: "Preserve human identity and natural portrait realism while making only believable, low-strength refinements to skin, hair, clothing response, body presentation, and person-specific light. Designed to run with A and B when a clear portrait/person subject is present."
license: "Proprietary (All rights reserved; 未经许可不得商用)"
---

# Portrait Real Grade Skill (C)

Use C when the image contains a **clear portrait / person-as-subject**. C is the person-specific realism layer. It does not replace A or B.

## Default combined route
- **Clear portrait/person subject present -> A + B + C by default.**
- **No portrait/person subject -> A + B by default.**
- Incidental distant passersby or tiny background figures do not automatically make the image a portrait; route by the actual subject.
- The user's explicit request always overrides the default combination.

Default activation does **not** mean strong effects. A, B, and C may all run at very low strength when the source is already good. A clear portrait keeps C in the default route even when no visible retouch is needed; in that case C acts as a realism/identity guardrail. Only an explicit user module override changes the combination.

## Module boundaries
- **A** handles the whole scene: exposure, white balance, believable tonal hierarchy, environment, background, architecture, light consistency.
- **B** handles the design/presentation layer: editorial framing, typography, paper/print language, layout, restrained source-led composition. B does not mean collage.
- **C** handles the person: identity, skin, face, hair, clothing response, person-specific light, and requested subtle body presentation.

## Non-negotiable portrait constraints
1. Preserve identity, age cues, expression, pose, gaze, face proportions, and recognizable features unless the user explicitly requests a specific change.
2. Prefer light, skin tone, local contrast, and texture adjustments over changing facial geometry.
3. Keep cheek/jaw outer contours natural and continuous. Avoid wavy, dented, pinched, collapsed, or over-sculpted face edges.
4. Preserve real skin texture. Do not create plastic skin, beauty-filter flattening, fake pore sharpening, or uniform airbrushing.
5. Keep eyes, teeth, lips, hairline, fingers, limbs, clothing edges, and jewelry anatomically/physically plausible. Do not “beautify” by inventing details.
6. Hair can be cleaned or made slightly smoother when helpful, but preserve strand direction, volume, and natural flyaways unless the user asks for stronger grooming.
7. Body-shape adjustments, when explicitly requested, must be subtle and local; protect anatomy, clothing folds, background geometry, and identity. Do not let extra requests replace A/B/C’s realism baseline.
8. Do not sexualize the person or alter clothing/body emphasis merely because a stronger stylization is possible.
9. Person lighting must agree with the scene lighting established by A. Do not add independent face glow, rim light, or beauty lighting that contradicts the environment.
10. When uncertain, preserve the person rather than “improve” them.

## A+B+C does not mean three heavy effects
A+B+C means three responsibilities are considered together:
1. A protects and lightly finishes the scene.
2. C protects and lightly finishes the person.
3. B adds only the amount of editorial/design expression that genuinely helps.

A strong portrait may therefore receive near-original A, near-original C, and an extremely restrained B treatment. The default route is about coverage, not intensity.

## Feedback absorption
Follow the shared `../FEEDBACK_ABSORPTION_POLICY.md`.
- “Face edge looks fake” should tighten face-geometry protection; it must not make all future portraits flat or untouched.
- “Hair could be smoother” is a local preference, not a license to repaint hair globally.
- A single failed portrait execution does not disable C or B.
- Positive portrait feedback becomes a compatible anchor, not a universal preset.

## Final portrait check
Before accepting an output, verify:
- same person / same expression / same pose identity;
- no warped jaw/cheek/hairline/fingers/limbs;
- skin still has believable texture;
- person and background share one coherent light field;
- B does not cover the face, body focal point, or important person/environment relationship;
- the result still feels like the user's photograph, not a generated replacement.
