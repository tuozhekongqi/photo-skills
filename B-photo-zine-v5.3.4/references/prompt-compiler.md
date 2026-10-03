# Prompt Compiler v5.3

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
- subtle analog finish only when source/user intent supports it.

Do not describe it as a second equal style.

### BLOCK F — Layout signature
Explicitly state the chosen layout signature.

### BLOCK G — Copy
Use the chosen Copy Engine mode. If C0, explicitly request no text.

### BLOCK H — Negative constraints
Include only failure modes relevant to this source / style, plus universal rules:
- no unrequested or unjustified multi-photo collage; if a deliberate same-subject collage is chosen, preserve one clear hero image and do not cover the key subject;
- no unrelated invented object;
- no source-identity loss;
- no generic sticker clutter;
- no commercial ad look.

---

## 2. Prompt length rule

Prefer a clear 8-block instruction over a giant paragraph of decorative adjectives. Repetition lowers adherence.

The prompt should explain:
- what must remain;
- what visual behavior matters;
- what transformation is allowed;
- what exact layout / material language to use;
- what to avoid.

---

## 3. Style-specific compiler rule

Never compile from the style recipe alone. Always merge:
`source lock + strongest behavior + transformability + primary style + layout + copy + relevant negatives`.

This keeps the prompt source-led.

---

## 4. Example skeleton

```text
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
No unrelated motifs, no red-gold tourism cliché, no unjustified multi-photo collage...
```
