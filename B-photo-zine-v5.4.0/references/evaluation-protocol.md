# Evaluation Protocol v5.0

## Hard gates BEFORE weighted scores

Read `delivery-contract.md`. First inspect the actual output for correct source, scene/portrait identity and plausible lighting; source_gate_pass must be true. Then inspect the locked design requirement. Strong B requires page composition transformation AND a second functional narrative/reading relation. Standard/light requires major+supporting structure. Grade alone, filter, plain border+caption, or merely written design intentions fail R04_UNDER_DESIGNED regardless of the numerical scores below.

For strong B, name the two visible relations and compare the final page with the base master. Removing a tiny caption/border/sticker must not return essentially the unchanged original layout. Quiet/photo-led/no-text are compatible with strong construction and are not exemptions. Missing B keeps design_done=false and status=redo/pending; tool/capacity failure uses blocked. Mark done only after required base/design work, both gates and final_contract_check=pass. Weighted scores cannot offset a hard-gate failure.

Use this after planning a batch and before accepting final images.

## A. Per-image decision quality
Score 0-2 for each:
- source identity preserved;
- strongest visual behavior correctly identified;
- transformability not overestimated;
- primary style explains the image better than alternatives;
- typography fits available space;
- concept derives from source;
- layout supports rather than competes with photo.

Target: >= 11 / 14.

## B. Per-image generation quality
Score 0-2 for each:
- correct source used;
- no accidental multi-photo collage;
- major landmark / geometry preserved;
- palette remains source-related;
- text remains subordinate;
- no generic sticker clutter;
- no obvious repeated template behavior.

Target: >= 12 / 14.

## C. Batch diversity quality
For 6+ selected outputs, verify:
- >= 3 style families;
- >= 3 layout signatures;
- no family more than twice consecutively;
- at least one visually quiet image;
- at least one photo-led treatment;
- no more than one or two strong concept pieces unless requested;
- repeated copy rhythm is avoided.

## D. Batch coherence quality
The set should share 3-5 anchors:
- paper temperature;
- margin scale;
- typography family/mood;
- source-derived color discipline;
- copy tone;
- grain / tactile finish.

Do not achieve coherence by making layouts identical.

## E. Redo diagnosis codes
When rejecting an output, record one or more:
- `R01_WRONG_SOURCE`
- `R02_SOURCE_IDENTITY_LOST`
- `R03_OVER_DESIGNED`
- `R04_UNDER_DESIGNED`
- `R05_TEMPLATE_REPEAT`
- `R06_BAD_TYPE_PLACEMENT`
- `R07_COPY_GENERIC`
- `R08_CONCEPT_FORCED`
- `R09_PALETTE_DRIFT`
- `R10_LAYOUT_MISMATCH`
- `R11_UNRELATED_INVENTION`
- `R12_MULTI_SOURCE_MERGE`

On redo, change the cause, not merely the wording of the prompt.
