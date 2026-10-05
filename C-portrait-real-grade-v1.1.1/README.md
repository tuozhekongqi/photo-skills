# Portrait Real Grade v1.1.1 — C

## User-package revision

This revision preserves normal photographic grading and adds combined-user integration: A+B for scene-led edits, C+B for portrait-led edits, with strong B by default. Standalone use remains photographic only. Current explicit grading-only/light-design instructions override the relevant combined default. SKILL.md uses valid name/description metadata. Reference images are unchanged.

C is the portrait-first sibling of A.

- **A**: scene-first realistic photographic finishing.
- **C**: person-first realistic photographic finishing.
- **B**: design/editorial layer.

C may be used alone (`C`) or followed by B (`C+B`). In C+B, C resolves the person and environment first; B must treat that portrait master as the truth layer rather than generating a new person.

## Runtime principle
**Same person, same moment, stronger hierarchy.**

The target is a believable edited photograph: natural identity, soft local light, preserved skin texture, gradual depth, believable night atmosphere, and restrained cinematic color.

## Core files
- `SKILL.md` — complete runtime rules.
- `references/workflow.md` — operational checklist.
- `references/research-lessons.md` — external research distilled into transferable rules.
- `references/negative-patterns.md` — common AI-looking portrait failures.
- `references/integration-with-B.md` — C+B contract.
- `references/feedback-ledger.md` — user-specific learned corrections.
