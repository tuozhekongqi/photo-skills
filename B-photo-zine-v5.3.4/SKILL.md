---
name: photo-zine-social
version: 5.3.4
summary: Turn real photos into source-led social/editorial outputs while preserving source identity. Treat batches directly and lightly, use feedback without overfitting, avoid quota-driven collage/diversity, and keep multi-image work optional and compositionally justified.
---

# Photo Zine Social Skill

Within the combined package, B is active by default under the shared routing rule. This skill defines the photo-first editorial/design layer for real photographs; visible redesign into social-media images, travel editorials, collectible cards, quiet posters, magazine pages, or conceptual photo-art pieces is applied only when it helps the source or the user explicitly asks for it.

The governing idea is **photo-first design**:

> Understand the source image first. Then choose the lightest intervention that reveals what is already strong in the photo.

The goal is not to make every photo look "AI-designed". The goal is to add design only when it helps, while keeping the user's photography primary. A batch may legitimately contain repeated quiet treatments if that is what the photographs support.

## Shared default routing
- No clear portrait/person subject: **A + B** by default.
- Clear portrait/person subject: **A + B + C** by default.
- The user's explicit instruction overrides these defaults.
- B being active does not mean collage or heavy layout; it may be a very restrained or near-no-op editorial layer. Source quality, “只轻修”, “只调色/光影”, or low visible-design value do not disable B; only an explicit user module override changes the combination.

---


# 0. Feedback mode

When the user is clearly evaluating prior outputs, do **not** automatically make a new image. Follow `references/feedback-loop.md` and the shared `../FEEDBACK_ABSORPTION_POLICY.md`. Learn at the smallest valid scope; do not let one recent comment globally reweight the skill.

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

1. **Default: one source photo -> one finished image.** A multi-source collage is an optional exception only when complementary same-subject images genuinely become stronger together; never use collage to save effort or satisfy diversity.
2. **No duplicates, no omissions.** Build a source ledger before generation.
3. **Near-identical-angle culling is narrow.** It may be used only for truly same-angle duplicates under the user's existing allowance. Do not cull different viewpoints merely because they tell a similar story.
4. **Never substitute one source for another.** Similar lake, bridge, city, or mountain photos remain separate originals unless explicitly deduplicated by angle.
5. **Photo identity comes first.** Preserve the key subject, landmark, spatial logic, dominant palette, direction of light, and scene story.
6. **Do not force a uniform look.** A set should feel related, not repetitive.
7. **Do not invent unrelated subjects.** Any new graphic, illustrated, or surreal element must derive from the source image or the user's explicit request.
8. **Typography must stay subordinate to the image.** Use short copy, small scale, and style-appropriate placement.
9. **No generic sticker-book clutter.** Avoid decorative stars, tape, leaves, fake stamps, icons, and paper scraps unless a chosen recipe calls for a small number of them.
10. **Never generate a multi-photo moodboard by accident.** No nine-grid/grid-mosaic/contact-sheet dump. Diptych/triptych/asymmetric same-subject layouts are allowed only with a clear compositional reason and must not cover the primary subject.
11. A rejected **execution** suppresses only its concrete failure signature. Remove an entire family only when the user explicitly establishes a durable family-level hard reject or repeated cross-context evidence justifies it.
12. Prefer **clean, restrained, tactile, editorial** design over loud illustration, glossy mockups, or commercial poster aesthetics.
13. Do not turn an accepted treatment into a universal template. Vary layout signature, text amount, paper treatment, title scale, and transformation intensity according to the source.

---

# 2. Source fidelity modes

Classify every image before styling.

## PRESERVE
Keep the source essentially photographic; design changes should not alter the scene itself.

Best for:
- already-strong photos;
- city scenes;
- documentary images;
- portraits;
- cinematic frames;
- minimal editorial treatment.

## HYBRID
Keep truthful photographic material dominant while a limited area becomes printed, cut, abstracted, or typographically designed.

Use conditionally when a specific transition or design layer clearly improves the source. HYBRID is **not** the automatic default for travel, architecture, water, landscape, or editorial work.

## DISTILL
Strongly reinterpret the scene as illustration, printmaking, simplified geometry, or collectible graphic art.

Use only when the user explicitly wants stronger transformation or when a clearly validated reference/source concept makes the transformation unmistakably appropriate. Never use DISTILL merely to create variety or to make an already-strong photograph look more designed.

**Default to `PRESERVE`.** Use `HYBRID` only when the source clearly benefits.

---

# 3. Required workflow

## Step 1 - Lightweight batch intake

When the user submits a batch, treat it as a batch and proceed in upload order. Do not let an exhaustive per-image audition/scoring pass become the dominant workflow. Keep only enough internal bookkeeping to preserve source identity and avoid accidental omissions/substitutions.

Do not discard different viewpoints for visual-story redundancy. Only truly near-identical same-angle frames may be collapsed under the user's existing allowance.

Consult `references/source-selection-engine.md` and `references/batch-control.md`.

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
Photo-led travel editorial with restrained watercolor/ink accents or partial transitions. Do not default to repainting the whole photograph.

### C. MINIMAL COLLAGE POSTER
Graphic cropping, whitespace, modern zine/poster discipline.

### D. SECOND WORLD PHOTO EDITORIAL
A source-derived conceptual second world grows from the photo's own structure.

### E. SOFT ANALOG DIARY
Quiet photo-led travel memory. Analog character is optional and subtle; grain, cast, and “film look” are never mandatory.

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

Do **not** route mainly by subject. Use `references/decision-engine.md` as a lightweight internal aid, not as a quota-producing or exhaustive pre-generation gate. The main question is still what the source is already doing well. If two treatments are genuinely equally suitable, batch context may break the tie. Do not use numeric scoring or diversity pressure.

Always answer internally:

> **What is the strongest thing this photo is already doing?**

The chosen style must amplify that behavior. If no style is a strong match, downgrade intervention and preserve more of the photograph.

## Step 5 - Batch coherence without quotas

There are no target percentages for A/B families, no required family count, and no mandatory experimental/multi-image slot. Repetition is acceptable when several photographs genuinely call for the same treatment.

Use batch context only as a secondary tie-breaker. Never make a worse local decision just to diversify the set.

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
- conceptual elements do not arise from the photo itself.
- unintended nine-grid / grid-mosaic / contact-sheet batch dump;
- collage covers or cuts through the key subject without a source-led reason.

After acceptance, mark the source `done`. On failure, use `references/retry-policy.md` to distinguish execution failure, decision failure, and source-selection failure before retrying.

---

# 4. Decision engine summary

The selector is based on **visual behavior**, not merely subject category.

## Visual Profile
Record focal strength, geometry, negative space, light, color, texture, narrative, detail value, Second World potential, text tolerance, depth, motion, mood, and one sentence describing the strongest visual behavior.

## Visual Behavior Archetype
Assign one primary and optionally one secondary behavior archetype from `references/visual-archetypes.md`. This intermediate layer describes **how the image behaves** — for example expansive negative space, directional depth, axial monumentality, reflective duality, ornamental radial structure, quiet snapshot, or motion network.

## Transformability
- `T0` — minimal intervention; preserve the photo.
- `T1` — light design; layout / framing / small type.
- `T2` — moderate reinterpretation; visible but source-faithful styling.
- `T3` — strong concept; only when the image clearly supports it.

When uncertain, downgrade.

## Qualitative candidate choice
Use `references/decision-engine.md`. Do not use numeric scores, fixed thresholds, family quotas, or confidence percentages. Normally compare only the most plausible treatment(s) against the option to preserve/do less.

Source fidelity, current explicit intent, and compatible approved anchors dominate. Batch variety can only break a genuine tie.

## Preference and global optimization
Apply explicit user taste as a **scoped, bounded modifier after source fit**. A new comment does not gain weight because it is recent. Execution-specific rejects do not ban the parent family; global hard rejects require explicit durable scope or repeated cross-context evidence.

Optimize for **local fit first**. Batch rhythm is optional and should usually be achieved by sequencing, not by changing a correct local treatment. Do not force a worse style for variety.

Full logic: `references/decision-engine.md`.
Behavior archetypes: `references/visual-archetypes.md`.
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
A photo-led travel-magazine page with restrained watercolor/ink accents or partial transitions. The photograph remains dominant by default.

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
A quiet photo-led travel memory with optional analog character.

Best for:
- streets;
- transit;
- friends;
- casual landscape;
- everyday travel moments;
- dusk and soft light.

Core logic:
- preserve photography;
- gentle highlight rolloff;
- grain and film cast are optional, minimal, and only used when source/user intent supports them;
- one tiny note/date/underline/circle maximum;
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
- cinematic crop / tonal shaping;
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
- minimal caption;
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

If a set needs coherence, it may share a few optional anchors such as:
- similar paper temperature;
- restrained typography;
- consistent margins;
- source-derived color discipline;
- quiet copy tone;
- a consistent tactile finish where appropriate; grain is not required.

Do not force identical layouts.

---

# 8. Supporting files

- `references/style-recipes.md` - expanded construction rules and sub-recipes.
- `references/prompt-library.md` - ready-to-copy prompts for all 12 families plus batch prompts.
- `references/batch-control.md` - source ledger, near-duplicate culling, next-batch logic, and redo rules.
- `references/research-notes.md` - design research notes and external inspiration references.
- `references/decision-engine.md` - lightweight qualitative source-led routing; no numeric scoring or style quotas.
- `references/visual-archetypes.md` - intermediate behavior classes between profile and style.
- `references/style-fit-matrix.md` - positive signals and contraindications for all 12 style families.
- `references/decision-counterexamples.md` - anti-pattern examples that prevent subject-to-style shortcuts.
- `references/layout-signatures.md` - layout taxonomy and repetition control.
- `references/evaluation-protocol.md` - lightweight final QC and redo diagnosis codes; no diversity quotas.
- `references/source-selection-engine.md` - conservative source preservation with narrow same-angle duplicate handling.
- `references/preference-adaptation.md` - explicit likes/dislikes as bounded decision modifiers.
- `references/series-planner.md` - sequencing, visual intensity, color rhythm, and text rhythm.
- `references/copy-engine.md` - scene-derived titles, handwritten asides, archival labels, and no-text decisions.
- `references/prompt-compiler.md` - structured source-led prompt assembly.
- `references/retry-policy.md` - diagnose and recover from execution, decision, or source-selection failures.
- `examples/compiled-prompt-example.md` - complete decision-to-prompt example.


## Heritage architecture foundation
For traditional architecture, first consult `references/heritage-photo-foundation.md`. Keep the default A -> B responsibility order: finish/protect the photograph realistically in A, then let B range from near-no-op to a visible zine layer according to real design value, without changing the scene's weather, architecture, or historical detail.

## Same-source batch handling
For related photographs, consult `references/batch-diversity.md`. Treat the upload as one batch for coherence, but keep routing source-led and lightweight. There are no required roles, style counts, multi-image pieces, or experimental slots. Collage remains an optional same-subject exception only when it genuinely improves composition.
