---
name: photo-zine-social
description: Create finished editorial, zine, poster and collectible images from real scene or portrait photos. Use for photo redesign or as B in the ABC user package. Default to strong page design with preserved source identity, independently of photographic transformability; explicit light-design requests override the default.
metadata:
  version: "5.4.0"
---

# Photo Zine Social Skill

## Strength and photographic-restraint scope

Read `references/delivery-contract.md` first. Default strong B is independent of photographic T/PRESERVE. Quiet/photo-led means less repainting/clutter, not weaker page design; historical taste cannot lower the current contract.

For E/analog, use an authored diary/editorial grid plus a meaningful source-story or reading hierarchy. For G, make asymmetric photo/negative-space construction plus a source-derived graphic/space rhythm; no text or extra crop is required. For H/K, use a designed story/study page with a second scene/detail relation or clear hierarchy, not a grade or monochrome conversion alone. J/F/Clean Editorial must create an actual page hierarchy; plain uniform border+caption is insufficient. These examples are options, not fixed templates; all families must meet the selected strength's observable gate.

## Delivery contract — read before selection

Default to **strong B** for B design requests and combined-user A+B/C+B. Read `references/delivery-contract.md` first; preserve the caller's route, normal base grade, design_required and design_strength. Do not require magazine/collage keywords for combined-user requests. Explicit light/standard/no-design instructions override the matching default. Analysis/feedback does not generate.

Strong B needs visible **page composition transformation + a second functional storytelling/reading hierarchy**. A grade, frame and tiny caption fail. Quiet, text-free, single-photo design can pass; stickers/collage are not mandatory. Plan concrete positions/scale/alignment and inspect their presence after generation. Photographic T0–T3 is independent of design_strength: **PRESERVE + T0 + strong B is valid**. Weak source fit lowers repainting/clutter risk, not the required design strength.

Compile this contract into every prompt. A/C no-layout constraints protect the photographic master, not B's final page. Do not mark done until base and design work are complete and both source and design gates pass. If a tool fails, report blocked/unfinished B, never claim a base-only image is the finished B result.

Use this skill when the user wants real photographs redesigned into polished social-media images, travel editorials, collectible cards, quiet posters, magazine pages, or conceptual photo-art pieces.

The governing idea is **photo-first design**:

> Preserve what is strong in the photograph, and build a source-led **strong page design** around it. Photographic restraint and design strength are independent decisions.

The goal is not to make every photo look "AI-designed". The goal is to make the finished set feel authored, varied, collectible, and still unmistakably based on the user's own photography.

---


# 0. Feedback mode

When the user is clearly evaluating prior outputs, do **not** automatically make a new image. Follow `references/feedback-loop.md`, translate the critique into specific design rules, and consult `references/feedback-ledger.md` before the next generation.

A positive response should promote the decisions that made the image work, not freeze the whole page into a reusable template. A neutral response should stay secondary. A hard negative should become a concrete anti-pattern.

Feedback must also catch self-contradictions: if B’s graphic treatment causes unnecessary source repainting (for example manufacturing sunset to make a magazine layout prettier), treat that as source-fidelity drift even if the layout itself is attractive.

---

## Lightweight reference-memory policy

The distributable B skill keeps a **positive image library plus, at most, a tiny archetypal cautionary set**. Do not build separate image libraries for “还行”, “一般”, tutorial screenshots, or broad research. Convert those evaluations into text rules in `references/feedback-ledger.md`.

- Strong explicit positives may enter `reference-library/positive/`.
- “还行” contributes selective textual lessons only.
- “一般” contributes diagnosis/avoidance text only.
- Negative images are retained only when a visual failure cannot be explained adequately in text; otherwise keep the warning textual.
- Research images should be deleted once their transferable principles are captured in `references/research-notes.md`, style recipes, or the feedback ledger.
- A liked layout is a **principle source**, not a template contract. Never let the positive library collapse B into one repeated serif/paper/torn-edge look.


## Lightweight image-memory policy
See `references/image-memory-policy.md`. Keep only strong positives and a tiny set of archetypal visual failures; store “还行/一般/research/tutorial” learning as text.

# 1. Non-negotiable rules

1. **One source photo -> one finished image.** A chosen recipe may use multiple meaningful crops from that same source. Mixing different originals requires explicit user authorization.
2. **No duplicates, no omissions.** Build a source ledger before generation.
3. **Near-identical angles may be culled.** If several originals show essentially the same view, keep the strongest representative and mark the others `skipped-near-duplicate`; do not generate all of them unless the user asks.
4. **Never substitute one source for another.** Similar lake, bridge, city, or mountain photos remain separate originals unless explicitly deduplicated by angle.
5. **Photo identity comes first.** Preserve the key subject, landmark, spatial logic, dominant palette, direction of light, and scene story.
6. **Do not force a uniform look.** A set should feel related, not repetitive.
7. **Do not invent unrelated subjects.** Any new graphic, illustrated, or surreal element must derive from the source image or the user's explicit request.
8. **Typography must serve the source and page hierarchy.** Keep copy short and placement source-aware; strong B may use a clear headline/subtitle hierarchy without obscuring the photographic subject. Text is optional.
9. **No generic sticker-book clutter.** Avoid decorative stars, tape, leaves, fake stamps, icons, and paper scraps unless a chosen recipe calls for a small number of them.
10. **Never generate a multi-photo moodboard by accident.** Multi-panel output is only allowed when the chosen recipe explicitly uses multiple crops from the same source image.
11. If a style has been rejected, do not drift back toward it in later outputs.
12. Prefer **clean, restrained, tactile, editorial** design over loud illustration, glossy mockups, or commercial poster aesthetics.
13. Do not turn an accepted treatment into a universal template. Vary layout signature, text amount, paper treatment, title scale, and transformation intensity according to the source.
14. **Locked design-strength floor.** B/A+B/C+B default to strong B: require page composition transformation and a second functional storytelling/reading relation. Explicit light/standard B uses the major+supporting floor instead. “Plain photo + border + caption” fails either floor. See `references/delivery-contract.md`.
15. A major design relationship can be: a deliberate editorial page structure, source-derived inset/crop system, meaningful paper/print hierarchy, magazine composition, poster hierarchy, or another source-led layout transformation. A supporting relationship can be: restrained title/subtitle, metadata, rule/line system, border, film mark, handwritten note, or small material accent.
16. The activation floor does **not** require collage. For visually dense or already-strong photographs, satisfy B through disciplined editorial structure rather than decorative clutter.

---

# 2. Source fidelity modes

Classify every image before styling.

## PRESERVE
Keep 80-100% of the retained source material photographic. This is not an untouched-pixel quota for the final canvas; strong page construction remains required.

Best for:
- already-strong photos;
- city scenes;
- documentary images;
- portraits;
- cinematic frames;
- minimal editorial treatment.

## HYBRID
Keep truthful photographic material visible while another area becomes illustrated, printed, cut, abstracted, or typographically designed.

Best default for:
- travel;
- architecture;
- water;
- landscape;
- zine/editorial work;
- Second World transformations.

## DISTILL
Do not reuse source pixels as the main image; reinterpret the scene semantically as illustration, printmaking, simplified geometry, or collectible graphic art.

Use only when:
- the user asks for stronger transformation;
- the photo is a detail/pattern that benefits from full reinterpretation;
- a poster or card style needs a distilled representation.

Default to `PRESERVE` or `HYBRID`.

---

# 3. Required workflow

## Step 1 - Inventory, select, and deduplicate

Build an internal ledger in upload order. Use `references/source-selection-engine.md` to remove both near-duplicate angles and redundant visual stories before styling. The best series may intentionally use fewer images than the upload count when the user allows culling.

Build an internal ledger in upload order.

| index | source id / filename | subject | angle group | orientation | source mode | style family | status |
|---|---|---|---|---|---|---|---|
| 01 | ... | ... | A | portrait | HYBRID | D | pending |

Allowed statuses:
- `pending`
- `done`
- `redo`
- `skipped-near-duplicate`
- `skipped-low-value`

### Near-duplicate culling rule
If 2+ photos have nearly the same:
- camera position;
- subject arrangement;
- focal length / crop;
- light;
- visual purpose;

then choose the strongest one by:
1. cleaner composition;
2. stronger light;
3. fewer reflections / obstructions;
4. better subject scale;
5. more useful negative space.

Keep one representative. Do not silently delete the others; mark them as `skipped-near-duplicate`.

## Step 2 - Read the photo before choosing a style

For each source, identify:
- narrative focal point;
- strongest geometry or path;
- dominant depth layers;
- negative space;
- visual rhythm / repetition;
- palette;
- source-derived motifs;
- emotional mode: calm, monumental, intimate, documentary, graphic, playful, cinematic, nostalgic, souvenir-like, archival, or conceptual.

Ask:

> What is the strongest thing this photo is already doing?

Do not start from a style name.

## Step 3 - Choose one primary style family

Use the 12 high-level families below. One primary family per finished image. A secondary influence may be used lightly, but do not blend 3-4 styles into a vague average.

### A. TRAVEL TICKET / SOUVENIR PASS
Travel memory as a collectible ticket or destination card.

### B. WATERCOLOR TRAVEL EDITORIAL
Soft, literary travel-magazine reinterpretation.

### C. MINIMAL COLLAGE POSTER
Graphic cropping, whitespace, modern zine/poster discipline.

### D. SECOND WORLD PHOTO EDITORIAL
A source-derived conceptual second world grows from the photo's own structure.

### E. SOFT ANALOG DIARY
35mm-like travel memory, natural imperfection, quiet annotation.

### F. MUSEUM CATALOGUE
The photo treated as an artwork or object worthy of archival display.

### G. LIGHT & NEGATIVE-SPACE POETRY
Sky, water, shadow, reflection, mist, branches, and silence become the design.

### H. CINEMATIC TRAVEL STILL
Narrative film-frame atmosphere without becoming a movie poster.

### I. MODERN CHINESE MINIMAL
Contemporary East Asian restraint for Chinese architecture, gardens, walls, roofs, bridges, stone, water, and pattern.

### J. EDITORIAL MAGAZINE FEATURE
Clean feature-page / cover logic with disciplined typography.

### K. MONOCHROME DOCUMENTARY
Structure, time, people, surface, and place over decorative color.

### L. DETAIL COLLECTIBLE CARD
A small, refined visual specimen built around one meaningful detail.

Full recipes live in `references/style-recipes.md`.

## Step 4 - Run the Style Decision Engine

Do **not** route mainly by subject. Subject type is only a weak prior. For every image, run the decision system in `references/decision-engine.md`:

1. build a `VISUAL_PROFILE`;
2. assign one primary and optionally one secondary `VISUAL_BEHAVIOR_ARCHETYPE`;
3. assign `T0-T3 TRANSFORMABILITY`;
4. build a 3-5 style candidate pool using archetype fit and the affinity matrix;
5. score candidates by structure, subject, light/color, mood, fidelity, and batch-diversity value;
6. subtract penalties for template risk, source damage, text overload, repetition, and forced concepts;
7. pass the `CONFIDENCE_GATE`;
8. choose one primary family and at most one secondary influence;
9. assign one layout signature and one optional batch role.

Always answer internally:

> **What is the strongest thing this photo is already doing?**

The chosen style must amplify that behavior. If no style is a strong match, lower photographic reinterpretation, preserve more of the source, and choose a safer layout that still satisfies the locked design strength.

## Step 5 - Batch rebalancing and style rhythm

For a varied travel series, a useful default is:
- 25-35% photo-led / analog / cinematic (`E`, `H`, `J`, `K`)
- 20-30% tactile / painterly (`B`, `I`)
- 15-25% collectible / archival (`A`, `F`, `L`)
- 15-25% conceptual / graphic (`C`, `D`, `G`)

Avoid using the same family more than twice in a row unless the user requests consistency.

## Step 6 - Compose text with the Copy Engine

Use `references/copy-engine.md`. Choose C0-C4 based on text tolerance, style family, and available visual space. Text is optional and subordinate.

## Step 6A - Compose text after image analysis

Text should be generated from the actual image, not from a generic quote bank.

### Casual/editorial title
- 1-3 words;
- easy to render;
- scene-specific;
- not overly poetic.

### Handwritten line
- 6-14 words;
- observational;
- quiet;
- slightly personal;
- no motivational slogans;
- no repeated formula such as `Same..., different...`.

### Structured styles
For museum/grid/editorial recipes, use:
- a short title;
- optionally one small subtitle or metadata line;
- no fake official facts unless the user provides them.

## Step 7 - Compile the source-led generation prompt

Use `references/prompt-compiler.md` to assemble source lock, strongest visual behavior, fidelity / transformability, primary style, optional secondary influence, layout signature, copy mode, and relevant negative constraints.

## Step 7A - Generate one finished image

Generation constraints:
- bind only the current source image;
- do not introduce content from previous photos;
- generate one output at a time;
- preserve key geometry and recognizable landmarks;
- if reframing for social media, prefer safe expansion over destructive cropping;
- source-derived motifs only unless the user asks otherwise.

## Step 8 - Quality gate

Reject and regenerate if any occur:
- wrong source;
- repeated source;
- multiple originals merged;
- source identity lost;
- major landmark changed;
- style feels generic or template-driven;
- typography dominates;
- too many stickers / scraps / doodles;
- source palette replaced by an unrelated trendy palette;
- same layout signature used repeatedly without reason;
- output violates the selected source mode;
- conceptual elements do not arise from the photo itself;
- explicit `B` / `A+B` / `C+B` output is visually indistinguishable from an A/C-only edit;
- explicit B output contains only border + caption / tiny type without a major design relationship.

Before acceptance, apply `references/evaluation-protocol.md` hard source and design gates. Mark `done` only after base_done, design_done, both gates and final_contract_check pass; a graded master alone stays pending B. On failure, use `references/retry-policy.md` to distinguish execution failure, decision failure, and source-selection failure before retrying.

---

# 4. Decision engine summary

The selector is based on **visual behavior**, not merely subject category.

## Visual Profile
Record focal strength, geometry, negative space, light, color, texture, narrative, detail value, Second World potential, text tolerance, depth, motion, mood, and one sentence describing the strongest visual behavior.

## Visual Behavior Archetype
Assign one primary and optionally one secondary behavior archetype from `references/visual-archetypes.md`. This intermediate layer describes **how the image behaves** — for example expansive negative space, directional depth, axial monumentality, reflective duality, ornamental radial structure, quiet snapshot, or motion network.

## Transformability
- `T0` — preserve the photographic master intact; compatible with strong B page construction.
- `T1` — limited photographic stylization/print finish; page-design strength is specified separately.
- `T2` — moderate reinterpretation; visible but source-faithful styling.
- `T3` — strong concept; only when the image clearly supports it.

When uncertain, lower photographic T and source-damage risk while keeping the locked route and design_strength. Choose clean strong editorial construction rather than a light-design fallback.

## Candidate scoring
Use `references/style-affinity-matrix.md` to form a deterministic prior, then refine with archetype fit, subject compatibility, transformability, contraindications, source-damage risk, and batch context.

Final candidate scores use:
- structure fit: 30
- subject fit: 20
- light/color fit: 15
- mood fit: 15
- fidelity fit: 10
- series diversity value: 10

Subtract penalties for template risk, source damage, text overload, style repetition, and forced concepts.

## Confidence gate
- `90+`: exceptional fit
- `80-89`: strong primary
- `70-79`: viable / secondary
- `60-69`: weak
- `<60`: reject

If the field is weak, choose safer PRESERVE photographic material within a qualifying strong page layout; this cannot reduce design_strength.

## Preference and global optimization
Historical/general taste is a **soft modifier after source fit**. Current explicit deliverable instructions, including B strength, are contract constraints rather than score bonuses. A favorite style may receive a modest bonus but may not override a poor match. Hard rejects are respected.

Optimize for **local fit + global rhythm**. Do not force a worse style purely for variety. Track style family, layout signature, visual intensity, and sequence role.

Full logic: `references/decision-engine.md`.
Behavior archetypes: `references/visual-archetypes.md`.
Deterministic priors: `references/style-affinity-matrix.md`.
Contraindications: `references/style-fit-matrix.md`.
Counterexamples: `references/decision-counterexamples.md`.

---

# 5. The 12 style families

## A. Travel Ticket / Souvenir Pass
A real trip moment becomes a refined collectible travel object.

Best for:
- landmarks;
- destinations;
- lakes;
- mountains;
- heritage sites;
- iconic travel moments.

Core logic:
- photo preserved strongly;
- ticket/card structure uses source-derived motifs;
- cream / ivory / warm-gray paper;
- elegant serif or refined uppercase type;
- optional route / season / journey / memory microcopy;
- no fake official ticket realism.

## B. Watercolor Travel Editorial
A literary travel-magazine page with soft watercolor reinterpretation.

Best for:
- gardens;
- lakes;
- willow;
- bridges;
- historic streets;
- distant architecture;
- mountains.

Core logic:
- retain scene recognition;
- soft watercolor or colored-pencil edges;
- low-saturation source-derived palette;
- generous breathing room;
- short editorial title;
- no children's-book rendering.

## C. Minimal Collage Poster
Modern zine/poster composition built from crop, whitespace, and one strong graphic gesture.

Best for:
- architecture;
- skyline;
- road perspective;
- strong geometry;
- simple landscape silhouettes.

Core logic:
- 1 hero image or crop;
- 1-2 secondary graphic planes maximum;
- bold but sparse composition;
- strong whitespace;
- no scrapbook clutter.

## D. Second World Photo Editorial
A conceptual "second world" grows out of the photo's own structure.

Best for:
- roads;
- walls;
- rails;
- paths;
- water;
- shadows;
- cloud layers;
- mountain ridges;
- bridges;
- cable lines;
- stairs;
- architecture boundaries.

Core logic:
1. identify the most distinctive structure;
2. ask what it would become if it could be touched, entered, pulled, measured, carried, opened, repaired, connected, climbed, or used;
3. build the lower / adjacent paper-space concept from that answer;
4. optionally add 0-3 black line figures as genuine users of the second world;
5. add one natural handwritten English aside.

Important:
- do not default to `torn paper + tiny people`;
- the photographic cut shape must itself explain the source;
- figures are optional;
- if no convincing second-world interaction exists, choose another family.

## E. Soft Analog Diary
A quiet 35mm-like travel memory.

Best for:
- streets;
- transit;
- friends;
- casual landscape;
- everyday travel moments;
- dusk and soft light.

Core logic:
- preserve photography;
- fine grain;
- gentle highlight rolloff;
- subtle film cast;
- build an authored diary/editorial grid with a meaningful story/reading hierarchy;
- one tiny note/date/underline/circle maximum as a finishing annotation;
- keep snapshot imperfection.

## F. Museum Catalogue
The photo becomes a displayed work, study plate, or archival object.

Best for:
- architecture;
- ornament;
- carvings;
- gates;
- stone;
- trees;
- roof details;
- restrained landscape studies.

Core logic:
- white / cream / neutral field;
- one carefully framed image;
- refined caption hierarchy;
- exhibition-plate restraint;
- no fake museum branding.

## G. Light & Negative-Space Poetry
The image breathes. Light, air, distance, shadow, and emptiness carry the design.

Best for:
- vast sky;
- mountain ridges;
- water;
- reflections;
- mist;
- clouds;
- branches;
- quiet distant architecture.

Core logic:
- preserve negative space;
- almost no decoration;
- light copy or no copy;
- asymmetric photo/space page composition plus source-derived spatial rhythm;
- calm scale relationships;
- soft paper or clean photographic field.

## H. Cinematic Travel Still
A narrative still-frame treatment, not a movie poster.

Best for:
- paths;
- cable cars;
- mountain travel;
- city dusk;
- traffic;
- people moving through architecture;
- dramatic cloud / light.

Core logic:
- photo remains central;
- designed story-page hierarchy plus a meaningful second source/reading relation;
- cinematic crop / tonal shaping belongs to the photo, not the whole B deliverable;
- restrained contrast;
- optional tiny title or subtitle;
- no fake film logos, billing blocks, or blockbuster grading.

## I. Modern Chinese Minimal
Contemporary Chinese visual restraint, not nostalgic tourism or commercial guochao.

Best for:
- Forbidden City;
- Beihai;
- White Pagoda;
- hutong;
- stone bridge;
- willow;
- dragon ornament;
- roofline;
- red wall;
- courtyard.

Core logic:
- source-derived vermilion, ink green, stone gray, cream, muted gold;
- modern spacing;
- refined Chinese / English pairing when useful;
- quiet geometry and cultural materiality;
- no red-gold overload.

## J. Editorial Magazine Feature
Professional travel / lifestyle editorial page or cover logic.

Best for:
- strong destination images;
- city skyline;
- architecture;
- street feature;
- representative scenic views.

Core logic:
- one dominant photo;
- clear hierarchy;
- headline + short subtitle + small supporting line at most;
- type aligns with image geometry;
- no brochure clutter.

## K. Monochrome Documentary
Structure and place become the subject.

Best for:
- hutong;
- people;
- stone;
- stairs;
- wall texture;
- streets;
- forests;
- bridges;
- documentary scenes.

Core logic:
- monochrome or near-monochrome;
- preserve real texture;
- filmic tonal range;
- documentary study-page structure plus a second functional narrative/reading relation;
- minimal caption as finishing copy;
- no fake grit for its own sake.

## L. Detail Collectible Card
A meaningful detail becomes a small visual specimen or collectible print.

Best for:
- dragon carving;
- ceiling medallion;
- tile;
- lantern;
- plaque;
- gate detail;
- roof ornament;
- stone pattern;
- ripple;
- bridge arch.

Core logic:
- tightly chosen detail;
- clean card proportion;
- one title / specimen label;
- refined border or paper field;
- no arbitrary crop that destroys meaning.

---

# 6. Second World chapter - special method rules

Because `D. SECOND WORLD PHOTO EDITORIAL` is a method rather than merely a visual skin, follow these extra rules.

## Find the source's actionable structure
Look for:
- waterline;
- wall edge;
- cable;
- path;
- cloud bank;
- window;
- roofline;
- shadow;
- mountain ridge;
- bridge;
- stair;
- reflection;
- human gesture.

Then ask:

> If this structure were a real object in another world, what would a person naturally do with it?

Possible actions:
- pull;
- push;
- unfold;
- climb;
- enter;
- carry;
- measure;
- stitch;
- connect;
- repair;
- collect;
- reveal;
- sweep;
- pour;
- borrow;
- open.

Do not repeat actions mechanically. The answer must belong to the specific photo.

## Figure rule
- 0-3 figures maximum;
- monochrome line drawing;
- no cute mascot behavior;
- no idle posing;
- every figure must perform a functional interaction.

## Text rule
Write one short English aside based on the scene's actual behavior.

Good tone:
- natural;
- observant;
- slightly dry / playful / poetic;
- never inspirational.

## Final test
The work should create this reaction:

> "Of course — that photo could have been understood that way."

If the concept feels pasted on, reject it.

---

# 7. Series coherence without monotony

A coherent series may vary in style if it shares 3-5 recurring anchors, such as:
- similar paper temperature;
- restrained typography;
- consistent margins;
- source-derived color discipline;
- quiet copy tone;
- consistent grain / tactile finish.

Do not force identical layouts.

For a 9-image set, one useful rhythm is:
1. A or J - destination opener
2. E - quiet diary
3. B - painterly breath
4. D - conceptual surprise
5. F - archival pause
6. H - cinematic movement
7. G - visual silence
8. I or K - cultural/documentary grounding
9. L or C - collectible closer

---

# 8. Supporting files

- `references/style-recipes.md` - expanded construction rules and sub-recipes.
- `references/prompt-library.md` - ready-to-copy prompts for all 12 families plus batch prompts.
- `references/batch-control.md` - source ledger, near-duplicate culling, next-batch logic, and redo rules.
- `references/research-notes.md` - design research notes and external inspiration references.
- `references/decision-engine.md` - visual profiling, archetypes, transformability, scoring, confidence gates, and batch rebalancing.
- `references/visual-archetypes.md` - intermediate behavior classes between profile and style.
- `references/style-affinity-matrix.md` - numeric priors for candidate generation.
- `references/style-fit-matrix.md` - positive signals and contraindications for all 12 style families.
- `references/decision-counterexamples.md` - anti-pattern examples that prevent subject-to-style shortcuts.
- `references/layout-signatures.md` - layout taxonomy and repetition control.
- `references/evaluation-protocol.md` - QA scoring, diversity checks, and redo diagnosis codes.
- `examples/great-wall-stress-test.md` - stress test showing one destination routed to varied styles.
- `examples/sample-decision-ledger.md` - compact planning-table example.
- `references/source-selection-engine.md` - quality, near-duplicate, visual-story redundancy, and coverage selection.
- `references/preference-adaptation.md` - explicit likes/dislikes as bounded decision modifiers.
- `references/series-planner.md` - sequencing, visual intensity, color rhythm, and text rhythm.
- `references/copy-engine.md` - scene-derived titles, handwritten asides, archival labels, and no-text decisions.
- `references/prompt-compiler.md` - structured source-led prompt assembly.
- `references/retry-policy.md` - diagnose and recover from execution, decision, or source-selection failures.
- `examples/compiled-prompt-example.md` - complete decision-to-prompt example.
