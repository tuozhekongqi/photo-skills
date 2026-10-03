# Source Selection Engine v5.3

The default goal is to preserve the user's batch, not to shrink it. Selection is conservative and exists mainly to prevent accidental duplicates/substitutions.

## 1. No heavyweight curation by default
When the user sends a batch for processing, do not turn the task into a visible or dominant per-image audition. Process in upload order with lightweight internal tracking.

## 2. Near-duplicate exception
Only collapse frames that are truly near-identical in camera position, subject arrangement, crop/focal length, light, and visual purpose. This exception reflects the user's allowance that the same angle may need only one representative.

Different viewpoints of the same place are not duplicates merely because they communicate a similar story.

If choosing between true near-duplicates, prefer the cleaner/stronger frame, but keep the rule narrow.

## 3. Do not discard by "visual-story redundancy"
Do not omit a source simply because another image already covers the same theme (for example two different lake views, two different building angles, or repeated sky/architecture motifs). Different compositions may both matter to the user.

Do not use `low-value` as a convenience filter unless the image is genuinely unusable or the user asked for curation.

## 4. Style opportunity does not decide survival
A photograph should not be removed merely because it has low B/design opportunity. A strong or ordinary non-portrait photograph remains under the default A+B route unless the user explicitly changes the module combination. It may still look lightly designed or essentially original because A and/or B may run at near-no-op strength.

## 5. Skip semantics
Use only when justified:
- `skipped-near-duplicate` — truly same-angle near-duplicate and one representative is allowed;
- `reserved-alt` — optional alternative, but not silently discarded.

Never silently discard a source.
