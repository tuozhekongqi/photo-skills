# Style Decision Engine v5.2

This document defines the decision layer for `photo-zine-social`. It exists to prevent shallow subject-to-style routing. The engine must choose styles based on what the photo is visually doing, how much intervention it can tolerate, and how the image should function inside a set.

---

## 1. Decision pipeline

For every selected source image, run these stages in order after source selection:

0. `OUTPUT_INTENT + USER_PREFERENCE`
1. `VISUAL_PROFILE`
2. `TRANSFORMABILITY`
3. `CANDIDATE_POOL`
4. `CANDIDATE_SCORING`
5. `CONFIDENCE_GATE`
6. `PRIMARY_SECONDARY_SELECTION`
7. `BATCH_REBALANCING`
8. `DECISION_TRACE`
9. `SERIES_PLACEMENT`

Never jump directly from subject name to a style family.

---

## 1.5 Output intent and preference layer

Before profiling, record the current output intent (for example social feed, story, print, portfolio) and any explicit style likes / dislikes. Use `preference-adaptation.md`.

Historical taste is a soft modifier after source fit. Current explicit deliverable instructions and hard rejects constrain candidate eligibility; do not treat required strong B as a modest preference bonus.

### Locked delivery constraint
Read `delivery-contract.md` and lock route, base_grade_strength, design_required and design_strength before profiling. B/A+B/C+B defaults to strong B. Only current explicit instructions may reduce design strength. Before scoring, filter candidates against the locked strength: strong requires page composition transformation plus a second functional relation; explicit light/standard requires the major+supporting floor; do not compensate with grade/source-fit scores. T0 is valid at strong B because it describes photo preservation, not page construction.

Source selection happens before this engine; use `source-selection-engine.md` to remove near-duplicates and redundant visual stories.

---

## 2. Visual Profile

Create an internal profile with the following fields.

| field | values / scale | question |
|---|---|---|
| subject_type | landmark / architecture / water / garden / street / road / mountain / skyline / detail / people / mixed | What is present? |
| focal_strength | 0-3 | How clear and strong is the main subject? |
| geometry_strength | 0-3 | How important are axes, curves, silhouettes, repeated forms, or perspective? |
| negative_space | 0-3 | Does empty space materially improve the image? |
| light_value | 0-3 | Is light itself a key reason the photo works? |
| color_value | 0-3 | Are the source colors essential to the scene identity? |
| texture_value | 0-3 | Are material surfaces / grain / ornament important? |
| narrative_strength | 0-3 | Is there implied movement, timing, human action, or story? |
| detail_extraction_value | 0-3 | Would a crop or specimen treatment reveal something important? |
| second_world_potential | 0-3 | Is there a structure that can support a natural conceptual interaction? |
| text_tolerance | 0-3 | Can typography be added without weakening the image? |
| symmetry_axis | none / weak / strong | Is axial order important? |
| depth_type | flat / layered / deep perspective | How does space read? |
| motion_vector | none / horizontal / vertical / diagonal / radial / curved | Is there a dominant movement direction? |
| mood_vector | choose 1-3 | calm / monumental / intimate / documentary / graphic / cinematic / nostalgic / souvenir-like / archival / conceptual / poetic / playful |

Then write one internal sentence:

> **Strongest visual behavior:** ...

Examples:
- `A curved ridge line carrying the eye through a large quiet sky.`
- `A vanishing alley where red accents interrupt gray masonry.`
- `A centered ornamental medallion with radial repetition.`
- `Reflections create a second, calmer version of the architecture.`

The style decision must serve this sentence.

---

## 2.5 Visual Behavior Archetype

After the profile, assign one primary and optionally one secondary visual archetype from `visual-archetypes.md`. This is the preferred bridge between raw visual analysis and style candidates.

Archetypes describe **how the image behaves**, such as expansive negative space, directional depth, axial monumentality, reflective duality, ornamental radial structure, quiet snapshot, or motion network.

Use the archetype to build the candidate pool. Subject type remains only a weak prior.

---

## 3. Transformability

Assign one level before scoring styles.

### T0 — Preserve the photographic rendering

`T0` is valid with strong B. The photograph already has strong photographic quality; preserve its rendering inside the designed page.

Use when:
- composition is already resolved;
- natural light is excellent;
- the scene is documentary or cinematic;
- repainting or heavy photographic stylization would damage the photo; choose page design around the protected material.

Preferred families:
- E Soft Analog Diary
- G Light & Negative-Space Poetry
- H Cinematic Travel Still
- J Editorial Magazine Feature

Default fidelity: `PRESERVE`.

### T1 — Limited photographic stylization
The source tolerates limited print/tonal stylization but remains mostly photographic. Layout, text and design_strength are resolved separately.

Preferred families:
- E Soft Analog Diary
- F Museum Catalogue
- G Light & Negative-Space Poetry
- J Editorial Magazine Feature
- A Travel Ticket, light version

Default fidelity: `PRESERVE`.

### T2 — Moderate reinterpretation
The source can tolerate visible stylization while retaining scene identity.

Preferred families:
- A Travel Ticket / Souvenir Pass
- B Watercolor Travel Editorial
- C Minimal Collage Poster
- F Museum Catalogue
- I Modern Chinese Minimal
- L Detail Collectible Card

Default fidelity: `HYBRID`.

### T3 — Strong concept
The image has unusually clear structure or motif and can support a stronger conceptual transformation without losing identity.

Preferred families:
- D Second World Photo Editorial
- C Minimal Collage Poster, graphic variant
- L Detail Collectible Card
- restrained DISTILL sub-recipes

Default fidelity: `HYBRID`; use `DISTILL` only when clearly justified.

### Downgrade rule
When uncertain between photographic T levels, choose the lower level. Lower T does not lower page-design strength. A strong photograph can remain intact within a strongly designed page.

---

## 4. Candidate Pool

Do not score all 12 families mechanically. Build a pool of 3-5 plausible candidates based on visual behavior.

Subject type may be used only as a weak prior. It must not determine the result by itself.

Useful priors:
- strong negative space -> G, C, F, J
- strong geometry -> C, F, J, D
- strong natural light -> G, H, E, J
- strong texture / ornament -> F, L, I, K
- strong movement / implied story -> H, E, D, K
- strong conceptual structure -> D, C
- iconic destination memory -> A, J, E
- already excellent photograph -> E, G, H, J

---

## 5. Candidate Scoring

Use `style-affinity-matrix.md` to establish a deterministic prior from the Visual Profile, then refine it with archetype fit, subject compatibility, transformability, contraindications, source-damage risk, and batch context.

Score each candidate 0-100.

### Positive dimensions

| component | weight | meaning |
|---|---:|---|
| structure_fit | 30 | Does the style amplify geometry, layers, movement, or negative space? |
| subject_fit | 20 | Is the style naturally compatible with the scene without becoming thematic cliché? |
| light_color_fit | 15 | Does it preserve useful light and palette? |
| mood_fit | 15 | Does it match the image's emotional tone? |
| fidelity_fit | 10 | Does it respect the required PRESERVE / HYBRID / DISTILL level? |
| series_diversity_value | 10 | Does it improve the full set without materially lowering local fit? |

Maximum positive score: 100.

### Penalties

Subtract only when applicable:

| penalty | range | trigger |
|---|---:|---|
| template_risk | 0-10 | The treatment is becoming a repeated template rather than source-led design. |
| source_damage_risk | 0-10 | The style would erase a strong source quality. |
| text_overload_risk | 0-5 | The image has poor room for typography. |
| style_repetition_risk | 0-10 | The batch already contains too many similar treatments. |
| conceptual_force_risk | 0-10 | The concept feels imposed rather than discovered in the source. |

`final_score = positive_score - penalties`

### Interpretation
- 90-100: exceptional fit
- 80-89: strong primary
- 70-79: viable, often secondary or batch-balancing
- 60-69: weak; only use with a clear reason
- below 60: reject

### Preference adjustment
After source-fit scoring, apply only a modest user-preference bonus from `preference-adaptation.md`. Strong likes may add roughly +4 to +8 when compatible; soft likes +1 to +3. Hard rejects remove the treatment. Preference cannot rescue a fundamentally weak source fit.

---

## 6. Confidence Gate

After scoring:

### Case A — clear winner
If #1 leads #2 by >= 10 points and scores >= 80:
- choose #1 as primary;
- do not blend unnecessarily.

### Case B — two excellent candidates
If #1 and #2 are both >= 82 and separated by < 10 points:
- choose one primary;
- allow the other only as a secondary influence;
- never average them 50/50.

Example:
`Primary G + subtle H tonal influence`, not `half G / half H`.

### Case C — weak field
If no candidate reaches 75:
- step down transformability by one level if possible;
- prefer PRESERVE;
- choose E, G, H, J, or Clean Editorial with qualifying strong page construction; keep design_strength locked.

### Case D — high source-damage risk
If the best style still carries `source_damage_risk >= 7`:
- reject it even if the raw compatibility score is high;
- choose a safer candidate.

### Case E — no convincing concept
If D Second World requires explaining the concept in words to make it understandable, do not use D.

---

## 7. Primary / Secondary Selection

Every image retains its locked route/base/design contract and planned main/second functional relations, then receives:
- one `primary_family`;
- zero or one `secondary_influence`;
- one `source_fidelity_mode`;
- one `layout_signature`;
- one `batch_role`.

Secondary influence may affect only one or two dimensions such as:
- tonal treatment;
- typography;
- paper texture;
- crop discipline;
- line style.

It must not create a vague hybrid of multiple families.

---

## 8. Batch Rebalancing

After local decisions, optimize the set.

### Hard constraints
- no same family more than twice consecutively;
- no identical layout signature more than twice in a 6-image run;
- conceptual styles should not dominate the set;
- preserve at least one photo-led image in every 3-4 selected outputs when suitable.

### Diversity targets
For 6 outputs:
- >= 3 families;
- >= 3 layout signatures.

For 9 outputs:
- >= 4 families;
- >= 4 layout signatures;
- at least 2 photo-led outputs;
- at most 2 strongly conceptual outputs unless the user asks otherwise.

### Rebalancing rule
If two photos both score highly for the same family:
1. keep the stronger one in that family;
2. move the other to its secondary candidate only if the secondary score is within 8 points and >= 78;
3. otherwise keep both and vary layout / text / material rather than forcing a worse style.

Never sacrifice a clearly superior local decision merely to satisfy arbitrary variety.

---

## 9. Batch Roles

Assign one optional role to help sequence the set:
- `opener` — strongest destination / establishing image;
- `breath` — quiet visual pause;
- `movement` — action, road, cable car, crowd, travel energy;
- `concept` — one surprising reinterpretation;
- `heritage_anchor` — architecture / culture / material detail;
- `documentary_grounding` — ordinary lived reality;
- `collectible_closer` — detail card / archival end note.

Roles are sequencing aids, not mandatory style mappings.

---

## 10. Decision Trace

For every image, including single-image jobs, store the delivery-contract fields alongside this compact internal record:

```text
strongest_visual_behavior:
transformability:
source_fidelity_mode:
top_candidates:
primary_family:
secondary_influence:
layout_signature:
batch_role:
confidence:
why_primary:
why_not_runner_up:
```

The contract, stage completion and hard-gate fields are required for every job; full candidate traces are required for long batches so redo avoids the same failure.

---

## 11. Series Placement

After batch rebalancing, use `series-planner.md` to order the selected outputs by role, visual intensity, color rhythm, layout rhythm, and text rhythm. Reordering is preferred over degrading a good local style decision.

---

## 12. Tie-break hierarchy

When two styles remain equally plausible, prefer in this order:

1. the option that preserves the strongest source quality;
2. the option with lower source-damage risk;
3. the option that adds useful diversity to the batch;
4. the option requiring fewer invented elements;
5. the simpler treatment.

When in doubt, repaint less and remove clutter while meeting every locked delivery requirement. Choose coherent strong page construction, never silently lighter B.
