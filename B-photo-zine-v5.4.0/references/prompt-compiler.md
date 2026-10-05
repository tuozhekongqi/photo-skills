# Prompt Compiler v5.3

## BLOCK 0 — Locked delivery and stage scope

Read `delivery-contract.md` first. Prepend route, base_grade_strength, design_required and design_strength to EVERY prompt, including standalone B, batch items and retries. Name the main page-composition relationship and the second functional relation with positions, relative scale, alignment and intended reading/story function. Specify normal A/C base treatment where applicable; do not amplify grading to balance strong B.

Scope A/C no-layout/no-type/no-paper negatives to the protected photographic master/person. The B canvas must be free to carry the requested design. No-text C0 requires a non-text functional hierarchy. T0/PRESERVE prohibits repainting, not page construction. A one-call prompt must include both base and design tasks and pass both hard gates.

After source selection and style decision, compile the generation instruction in blocks. This prevents long free-form prompts from losing the actual decision logic.

---

## 1. Prompt block order

### BLOCK A — Source lock
State:
- use only the current source;
- preserve landmark / subject identity;
- preserve critical geometry, light, palette, and spatial relationships;
- do not import content from other photos.

### BLOCK B — Strongest visual behavior
One sentence from the Decision Trace.

Example:
`The core of this image is the cable line pulling the eye into a deep green valley.`

### BLOCK C — Fidelity + transformability
Specify:
- PRESERVE / HYBRID / DISTILL;
- T0 / T1 / T2 / T3;
- what must remain photographic;
- what may be transformed.

### BLOCK D — Primary style construction
Use the selected family / sub-recipe only. Include its key composition, material, color, and layout behavior.

### BLOCK E — Secondary influence
Optional. Mention only one limited influence, e.g.:
- cinematic tonal shaping;
- museum-like margin discipline;
- light watercolor edge;
- analog grain.

Do not describe it as a second equal style.

### BLOCK F — Layout signature
Explicitly state the chosen layout signature.

### BLOCK G — Copy
Use the chosen Copy Engine mode. If C0, explicitly request no text.

### BLOCK H — Negative constraints
Include only failure modes relevant to this source / style, plus universal rules:
- no multi-photo collage;
- no unrelated invented object;
- no source-identity loss;
- no generic sticker clutter;
- no commercial ad look.

---

## 2. Prompt length rule

Prefer a clear delivery-contract block plus the 8 construction blocks over a giant paragraph of decorative adjectives. Repetition lowers adherence.

The prompt should explain:
- what must remain;
- what visual behavior matters;
- what transformation is allowed;
- what exact layout / material language to use;
- what to avoid.

---

## 3. Style-specific compiler rule

Never compile from the style recipe alone. Always merge:
`locked delivery contract + source lock + strongest behavior + photographic transformability + primary style + layout + copy + scoped negatives`.

This keeps the prompt source-led.

---

## 4. Example skeleton

```text
DELIVERY CONTRACT:
route=A+B; base_grade_strength=normal; design_required=true; design_strength=strong.
Create asymmetric photo/paper page structure with a source-derived visual reading hierarchy. Keep the original lighting believable; do not intensify base grading.

SOURCE LOCK:
Use only this uploaded source image...

VISUAL BEHAVIOR:
The strongest feature is...

FIDELITY:
HYBRID, T2. Keep ... photographic. Only ... may be stylized.

PRIMARY STYLE:
Use Modern Chinese Minimal...

SECONDARY INFLUENCE:
Borrow only the soft tonal restraint of Cinematic Travel Still.

LAYOUT:
Use WHITE_FIELD_PLATE...

COPY:
Use C2: short title + small observational line...

AVOID:
No unrelated motifs, no red-gold tourism cliché, no multi-photo collage...
```
