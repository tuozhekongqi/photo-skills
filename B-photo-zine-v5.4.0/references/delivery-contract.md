# Delivery Contract v1.0 — 用户版正常底片 + 重 B

## Scope and precedence

This contract governs an image-generation/edit request invoking the combined ABC user package, and design requests invoking B directly. It does not convert analysis, feedback, diagnostics, or a bare upload into a generation request. Standalone A/C retain their standalone grading behavior. Current explicit user instructions override defaults. Source identity and plausible lighting constrain implementation; resolve conflict with a safer qualifying design, never silently omit required B.

Resolve this contract BEFORE photographic analysis and style scoring. Child workflows may choose techniques but must not reset route or design strength.

## Fields locked before style selection

```text
entry_context: combined-user | standalone-a | standalone-b | standalone-c
task_mode: generate | analyze | feedback
route: A+B | C+B | A | C | B | analysis-only
base_grade_strength: normal | none
design_required: true | false
design_strength: strong | standard | light | off
source_id:
main_design_relationship:
second_functional_relationship:
base_done: false
design_done: false
source_gate_pass: false
design_gate_pass: false
final_contract_check: pending
status: pending
```

For combined-user + generate: scene subject → A+B; portrait subject → C+B; normal base and strong B. B-only has base_grade_strength=none, base_done=true (not applicable). Analysis/feedback has no generation and no completion claim for an image.

Explicit only-photographic/no-design → A or C, design_required=false, off. Explicit light B → light; explicit normal/standard B → standard. Explicit design-only/no-grading → B. A request to keep the photo natural or edit hair/body is not an instruction to omit B. Do not add A before C.

## Independent axes

- A/C normal = existing realistic base workflow at ordinary priority, source-dependent corrections, no automatic cinematic intensification.
- Photographic transformability T0–T3 = tolerance for changing the photographic rendering/content. T0 leaves a strong photographic master intact; T1 permits limited photographic finish; T2/T3 allow increasing source-supported reinterpretation. It is not a page-design scale.
- PRESERVE/HYBRID/DISTILL = how photographic material is treated. PRESERVE proportions describe the retained photographic character of that material, not the percentage of the final page that must remain untouched pixels.
- design_strength = amount and consequence of page construction. PRESERVE + T0 + strong B is explicitly valid. Strong design does not authorize DISTILL, different faces, body reshaping, fabricated light, or invented facts.

## Observable strong-B minimum

Pass BOTH requirements in the final visible image:

1. **Page composition transformation**: deliberately reorganize the final canvas through an authored editorial grid, asymmetric photograph/space distribution, a source-derived spatial/graphic construction, a study/contact-sheet system, or comparable structure. A filter, plain frame, uniform border or one small caption alone fails.
2. **Second functional relation** integrated into that construction: meaningful source-detail/context storytelling; clear title/subtitle reading hierarchy; a paper/print or source-derived graphic hierarchy that guides the eye; or a deliberate non-text photographic/graphic contrast. It must explain something or organize reading, not merely add a decorative mark.

Identify both relationships concretely before generation: positions, scale, alignment and what they communicate. After generation, inspect the image for their actual presence. Removing a tiny caption, frame or sticker must not leave essentially the original photo layout.

Strong B can be quiet, text-free and use one intact photo. Do not require a fixed collage, insert, torn edge, extra person, decorative density, or number of elements. If a second crop adds no information, choose typography or a non-text graphic/space relationship instead. Crops must come from the current source or its A/C master. Portrait insets must preserve the same person; if risky, use environment/detail crops or a single-photo layout.

Standard/light B: require one major designed layout relation and one supporting relation; lighter scale/complexity is permitted. Plain grade + border + caption still fails. Off skips B and its design gate only when explicitly permitted by the resolved route.

## Compiler and stage boundary

Carry route, base_grade_strength, design_required and design_strength into EVERY final generation prompt, including a one-call implementation. Name the two planned relations and protect the source/portrait identity. A/C prohibitions on layout/type/material apply to the photographic master, not the B page. Prefer separate base and design stages when tools support them; a single tool call must still apply normal base treatment and strong design, and pass both gates.

Do not require visible text: C0/no-text is compatible with strong B via non-text hierarchy. Do not manufacture names, dates, destinations, logos or metadata. A–L in B are style-family labels; they do not refer to the ABC module route.

## Recovery and completion

Weak confidence → choose safer PRESERVE and lower photographic T if needed; retain locked design strength. Remove clutter and unstable concepts, then build a clean qualifying editorial layout. Under-designed output → R04_UNDER_DESIGNED; repair page construction, not just color or caption.

Follow retry-policy.md. Never silently lower strong to light, mark an A/C-only image as B-complete, or loop indefinitely. If tooling/capacity/source constraints prevent completion, status=blocked; report completed base and unfinished B separately. A permitted recovery ceiling is a stop condition, not permission to claim success.

For design_required=true, done requires base_done AND design_done AND source_gate_pass AND design_gate_pass AND final_contract_check=pass. For A/C-only, design_done=true means not applicable; source_gate_pass and final_contract_check must still pass. For blocked/redo/pending no done claim is allowed. One image may be done only after its actual final artifact has been inspected.
