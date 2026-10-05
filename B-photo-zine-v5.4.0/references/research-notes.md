# Research Notes — GitHub style expansion

This file records broad design lessons adapted into this skill. It is not a copy of any repository's exact prompts.

## Sources consulted

1. VigoZhao / AI-Visual-Prompt-Cookbook
   - Structured reusable style systems.
   - Useful categories: Photo + Doodle, Zine + Collage, Travel + City, Editorial + Minimal.
   - Key lesson adopted: define a style by composition logic, typography, image treatment, and negative constraints rather than only adjectives.

2. horushe93 / ai-image-prompts
   - Examples of digital editorial collage, Swiss grid, punk travel zine, vintage travelogue, and duotone/brutalist families.
   - Key lesson adopted: broaden the library across print, grid, and travelogue families while keeping each system reusable.

3. jas0nh / zine-poster-skill
   - Explicit source-fidelity channels and deterministic style contracts.
   - Key lesson adopted: distinguish PRESERVE, HYBRID, and DISTILL source-pixel policies so style does not silently destroy the original photo.

4. Shuryne / gpt-image-prompts
   - Medium-specific prompt examples such as cyanotype, linocut, gouache, collage editorial, ink, riso.
   - Key lesson adopted: medium choice should change material behavior and edge logic, not just add a style adjective.

5. boraoztunc / minimal-zine-poster
   - Strong emphasis on negative space, density control, restrained tactile poster design.
   - Key lesson adopted: guard against density creep and keep one visual anchor rather than filling the canvas.

6. Pixmind-io / awesome-midjourney-v7-example-prompts
   - Photography prompt patterns for editorial/documentary/photo realism.
   - Key lesson adopted: camera-like composition, lighting, crop, and depth should be described separately from graphic styling when preserving photography.

## Added recipe families

- `SOFT_ANALOG_EDITORIAL`
- `ANALOG_DIARY`
- `FILMSTRIP_DIARY`
- `CONTACT_SHEET_STORY`
- `VINTAGE_TRAVELOGUE`
- `GOUACHE_POSTCARD`
- `RISO_POSTCARD`
- `CYANOTYPE_MEMORY`
- `LINOCUT_HERITAGE`
- `NEWSPRINT_CITY`
- `SWISS_GRID_TRAVEL`
- `DUOTONE_BRUTALIST`
- `PAPER_APERTURE`
- `PHOTO_DOODLE_LIGHT`

## Design rule learned from the research

A robust style recipe should specify:

`source policy + composition grammar + material behavior + color logic + typography hierarchy + negative constraints`.

This makes styles meaningfully different without making the batch look random.


## Runtime archive policy
The earlier research-image archive has been removed from the distributable skill after its reusable lessons were distilled into this file, `style-recipes.md`, `decision-engine.md`, `prompt-compiler.md`, and the feedback ledger. Keep the textual principles; do not ship the original research images unless a future task specifically requires forensic re-analysis.


## Lessons extracted from the removed image-only research folder

Two research-only examples were deliberately removed from the runtime image set after their transferable ideas were written down:

- **Last Blue** — useful lesson: a photo can carry the page through a narrow dominant color field and silhouette/line rhythm; rough painted/ink-like edge masks can connect image and paper. Do not conclude that every dusk image needs brush masks or a script title.
- **Lakeside Line** — useful lesson: strong architectural framing and directional depth can support a calm editorial split, restrained botanical accent, and low-density copy. Do not conclude that every travel image needs botanical decoration or the same serif hierarchy.

These are now text lessons only; the source research images are intentionally not shipped.
