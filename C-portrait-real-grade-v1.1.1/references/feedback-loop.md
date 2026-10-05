# C evaluation loop

When feedback arrives, classify it before editing again.

## Failure classes
- IDENTITY: face/body/hair/clothing/person mismatch.
- LIGHT: fake rim light, hard practicals, overbright subject, night atmosphere lost.
- SKIN: plastic texture, wrong hue, over-uniform tone.
- DEPTH: fake or uniform blur, subject cutout.
- COLOR: global cast, skin contamination, excessive saturation.
- ENVIRONMENT: background too bright/clean/repainted.
- DESIGN: B layer overpowers portrait or inserts a mismatched person.

## Action
1. Preserve accepted decisions.
2. Change only the diagnosed layer when possible.
3. Convert user feedback into a rule in `feedback-ledger.md`.
4. Do not add an output to a positive image library unless the user clearly treats it as a strong reference.
