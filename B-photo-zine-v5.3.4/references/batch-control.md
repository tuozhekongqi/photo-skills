# Batch Control v5.3

## Lightweight source ledger
Use the minimum internal bookkeeping needed to preserve upload order and source identity. Do not expose or let a large per-image scoring sheet become the main workflow unless the user asks for curation.

Suggested minimal statuses:
- pending
- done
- redo
- skipped-near-duplicate (only for truly near-identical allowed duplicates)

Do not use `skipped-visual-redundancy` merely because different viewpoints tell a similar story. Do not use `skipped-low-value` as a convenience to reduce batch workload.

## Direct batch behavior
When the user gives a batch and asks to process it, proceed as one batch. Source-fit reasoning may remain internal and lightweight; do not stop to explicitly审视/打分 each photo before work.

Near-identical deduplication is a narrow exception, not a general curation license.

## Local fit before global rhythm
Global rhythm is a soft tie-breaker only. No fixed style counts, no required number of layout signatures, no mandatory experimental pieces, and no mandatory multi-image output.

If multiple sources genuinely support the same family, keep the locally superior treatment rather than forcing variety.

## "Next batch" behavior
When the user says `下一批`, `继续`, or equivalent:
- resume pending sources in upload order;
- do not rerun completed items unless asked;
- preserve source identity;
- do not invent new batch quotas.

## Redo behavior
If the user rejects a result:
- mark that source `redo`;
- retain the original source identity;
- record the **specific failure signature and scope**;
- change only what the feedback actually requires;
- do not automatically jump to a totally different family if the underlying idea was sound but the execution/intensity was wrong.

## Collage behavior
Collage is optional and source-driven. It may combine complementary same-subject frames when the composition becomes stronger, but it must not:
- save effort by swallowing many photos into one output;
- satisfy a diversity quota;
- cover/cut the key subject;
- become a nine-grid/grid-mosaic/contact-sheet dump.

## Final check
Run one compact end-of-batch check, not a dominant pre-generation filter. If an unintended nine-grid/grid-mosaic layout appears, invalidate the batch and rebuild.
