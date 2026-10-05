# Batch Control v5.2

## Completion ledger and immutable contract

For every selected source, add entry_context, task_mode, route, base_grade_strength, design_required, design_strength, main_design_relationship, second_functional_relationship, base_done, design_done, source_gate_pass, design_gate_pass and final_contract_check to the ledger. These are required for single-image jobs too. Add status=blocked for tool/capacity failure. A/C completion only changes base_done; B remains pending until its actual artifact passes the design gate. Done requires the full delivery contract, not a successful image-tool call.

Batch breath/photo-led roles change visual density, not strong-B requirements. Resume incomplete B from the accepted master. Culling or swapping a reserved source requires the user's permission to curate the batch; a request to process every photo prohibits omissions.

## Source ledger

Maintain this internal schema:

| index | file | subject | angle_group | strongest_behavior | archetype | transformability | source_mode | primary_candidate | secondary_candidate | chosen_family | confidence | layout_signature | batch_role | status | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

Statuses:
- pending
- done
- redo
- skipped-near-duplicate
- skipped-low-value
- skipped-visual-redundancy
- reserved-alt

## Near-duplicate policy

Near-duplicate means the images communicate essentially the same visual idea from nearly the same camera position.

Keep the strongest representative based on:
1. composition;
2. light;
3. subject scale;
4. clarity;
5. fewer window reflections / obstructions;
6. useful negative space;
7. best fit for an available style family.

Do not confuse "same place" with "same angle". Different viewpoints of the same place may both be valuable.

After angle deduplication, run a **visual-story redundancy** pass using `source-selection-engine.md`. Two different viewpoints may still communicate the same story and need not both be styled.

## Decision-aware batch planning

Before generation, each selected source must have:
- one sentence for `strongest_behavior`;
- one primary and optional secondary visual archetype;
- T0-T3 `transformability`;
- a primary and secondary candidate with scores;
- one final chosen family;
- one `confidence` value;
- one `layout_signature`;
- an optional `batch_role`.

Do not begin generation for a large batch until the first planning pass is complete.

## Local fit + global rhythm

Rebalance only when the alternative remains genuinely strong.

A source may move from primary to secondary candidate when:
- secondary score is >= 78; and
- secondary is within 8 points of primary; and
- the change materially improves batch diversity.

Otherwise keep the locally superior style and vary layout, typography, or material instead.

## "Next batch" behavior

When the user says `下一批`, `继续`, or equivalent:
- resume from the first pending source;
- do not rerun done items;
- do not promote skipped-near-duplicate images unless the user asks;
- do not silently change source order;
- avoid the previous output's exact layout signature when possible.

## Redo behavior

If the user rejects a result:
- mark that source `redo`;
- retain the original source id;
- record the rejected style / failure mode;
- choose a materially different treatment on regeneration;
- if transformability was overestimated, downgrade it;
- do not count the failed output as a new source.

Use a diagnosis code from `evaluation-protocol.md`.

## Style diversity

For 6 selected outputs:
- >= 3 style families;
- >= 3 layout signatures;
- no family more than twice consecutively.

For 9 selected outputs:
- >= 4 style families;
- >= 4 layout signatures;
- at least 2 photo-led treatments when the sources support them;
- no more than 2 strongly conceptual outputs unless requested.

Use conceptual styles such as Second World only when the source truly supports them.

## Layout diversity

Track layout signatures from `layout-signatures.md` separately from style families. Two images may share a family while using different layouts.

Do not use `TOP_PHOTO_BOTTOM_PAPER` or `TICKET_DIPTYCH` so often that the set starts to look templated.

## Text diversity

Do not reuse the same:
- title;
- handwritten sentence structure;
- location line;
- alignment;
- font mood;
- corner placement;

across several outputs unless the user asks for a strict series system.

## Series sequencing

After style and layout decisions are final, use `series-planner.md` to order outputs. Prefer reordering over weakening a high-confidence style decision merely for variety. Track visual intensity (`Q/M/S`), color rhythm, text rhythm, and sequence role.
