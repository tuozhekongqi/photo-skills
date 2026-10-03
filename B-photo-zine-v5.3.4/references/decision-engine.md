# Style Decision Engine v5.3.4 — qualitative, source-led

This is a **lightweight internal aid**, not a scoring system and not a mandatory per-image audition. Its job is to stop shallow “subject -> preset” routing while keeping the batch workflow direct.

## 1. One compact question
For the current source, ask:

> What is already working, and what is the lightest design intervention that would add real value without weakening it?

If the answer is “the photograph already works,” choose PRESERVE / A-lite / minimal B rather than inventing a stronger treatment.

## 2. Read only what matters
Use a compact visual read, not a full numeric profile. Notice only the relevant factors:
- main subject / visual anchor;
- important geometry or depth;
- real light and color relationships;
- useful negative space;
- texture/detail that must remain literal;
- human/story moment;
- tolerance for typography or paper/layout intervention.

Subject category is only context, never a style command.

## 3. Transformation ceiling
Use the lowest level that achieves the goal:
- `T0` — near-original / no visible design needed;
- `T1` — light layout, margin, framing, tiny type, or A+B editorial finish;
- `T2` — visible but photo-led stylization when it clearly adds value;
- `T3` — strong conceptual transformation only when the user explicitly wants it or the source/reference makes the concept unmistakably appropriate.

When uncertain, step down.

## 4. Fidelity default
`PRESERVE` is the default for strong photographs and for any source the user already likes.

`HYBRID` is conditional: use it only when a specific design transition/print treatment improves the work while the source identity remains clear.

`DISTILL` is not a default route. Use it only for explicit strong-stylization intent or a clearly justified experimental output. Do not let DISTILL replace a strong source photo simply to make the result feel more designed.

## 5. Candidate choice without numbers
Do not score 12 families, assign confidence percentages, or create a large candidate pool.

Normally consider at most 1–2 plausible treatments plus the “do less / preserve” option. Prefer, in order:
1. current explicit user intent;
2. source fidelity and subject integrity;
3. nearest compatible user-approved positive anchor;
4. the treatment that adds the clearest value with the least source damage;
5. simplicity.

Batch variety may break a true tie, but never rescue a worse local choice.

## 6. Family vs intensity
Keep separate:
- family/module choice;
- design intensity;
- photo-grade intensity;
- typography amount;
- material/paper amount;
- collage behavior.

A family can be correct while its intensity is wrong. “Too much” normally means reduce the relevant dimension before changing the entire family.

## 7. A+B is not collage
A+B can be a single source photo:
- A/A-lite protects and lightly finishes the photograph;
- B adds a restrained editorial design layer.

Do not require extra source images or collage for A+B.

## 8. Batch context
Treat the upload as one batch for coherence, but do not create:
- style quotas;
- layout quotas;
- experimental slots;
- multi-image requirements;
- mandatory sequence roles.

If several photos genuinely benefit from the same treatment, repetition is acceptable.

## 9. Collage gate
Collage is considered only when 2–4 complementary same-subject/same-event frames genuinely become stronger together. It must have a clear hero image and cannot hide/cut the key subject.

Never collage to save work, consume uploads, show “variety,” or reduce output count.

## 10. Optional trace for debugging only
Only when a result fails or a redo is needed, record a short trace:
```text
source_anchor:
what_already_works:
chosen_mode: PRESERVE / HYBRID / DISTILL
chosen_family_or_A+B:
intensity_issue_if_any:
why_this_is_lighter/better_than_alternatives:
```
Do not run this as a heavy gate for ordinary batch processing.
