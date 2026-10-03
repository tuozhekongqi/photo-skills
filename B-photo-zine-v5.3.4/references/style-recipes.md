# Style Recipes v4.0

The skill now routes through 12 high-level style families defined in `../SKILL.md`. The detailed recipes below remain valid as sub-recipes. Map them as follows:

- A Travel Ticket / Souvenir Pass -> `TRAVEL_TICKET_DIPTYCH`, `VINTAGE_TRAVELOGUE`
- B Watercolor Travel Editorial -> `QUIET_WATERCOLOR`, `GOUACHE_POSTCARD`
- C Minimal Collage Poster -> `CLEAN_EDITORIAL`, `SWISS_GRID_TRAVEL`, `PAPER_APERTURE`
- D Second World Photo Editorial -> use the dedicated method in `../SKILL.md` and `prompt-library.md`
- E Soft Analog Diary -> `SOFT_ANALOG_EDITORIAL`, `ANALOG_DIARY` (filmstrip/contact-sheet recipes are disabled by current project preference and grid-failure policy unless the user explicitly reopens them)
- F Museum Catalogue -> `ARCH_STUDY`, `DETAIL_GRAPHIC` with archival layout
- G Light & Negative-Space Poetry -> `CLEAN_EDITORIAL`, `CYANOTYPE_MEMORY` when appropriate
- H Cinematic Travel Still -> photo-led cinematic treatment; preserve source realism
- I Modern Chinese Minimal -> `ARCH_STUDY`, `LINOCUT_HERITAGE`, restrained heritage treatments
- J Editorial Magazine Feature -> `EDITORIAL_CITY`, `SWISS_GRID_TRAVEL`, `CLEAN_EDITORIAL`
- K Monochrome Documentary -> `NEWSPRINT_CITY`, documentary monochrome logic
- L Detail Collectible Card -> `DETAIL_GRAPHIC`, `RISO_POSTCARD` for selected details

Important: the high-level family decides intent; the sub-recipe decides construction details. Do not let a sub-recipe override the source image.

---

# Style Recipes v3.0

Every recipe defines six dimensions:

1. **Source policy** — PRESERVE / HYBRID / DISTILL.
2. **Composition** — where the photo, negative space, text, and graphic elements live.
3. **Material** — film, paper, ink, watercolor, gouache, halftone, etc.
4. **Color** — source-derived palette behavior.
5. **Typography** — what kind of text belongs in the piece.
6. **Failure modes** — what to avoid.

Use recipes as systems, not rigid templates.

---

## ZINE_TEAR

**Source policy:** HYBRID.

Use for travel, water, garden, hutong, street, and many general scenes.

- Keep the main photographic region realistic.
- Create one irregular tear or transition that follows source geometry: shoreline, roofline, bridge, road, tree canopy, wall, shadow edge, or subject silhouette.
- Let the stylized region use restrained screenprint, dry-brush, watercolor, halftone, or paper texture.
- Maintain color or motion continuity across the transition.
- Prefer one dominant tear event, not many small scraps.
- Typography: lower-left casual English title + one short handwritten line.
- Avoid fixed 50/50 horizontal splits, heavy white borders, sticker clutter, or moodboard layouts.

## QUIET_WATERCOLOR

**Source policy:** PRESERVE or light HYBRID.

Use only when the source naturally benefits from a soft watercolor/ink accent. The photograph remains the main image.

- Preserve the real photographic subject, geometry, weather, and most source texture.
- Confine watercolor/pencil treatment to margins, transitions, selected secondary areas, or subtle edge behavior unless the user explicitly asks for a full illustration.
- Use source-derived muted colors.
- Keep generous negative space.
- Never repaint the whole frame by default.
- Typography: small serif or handwritten title, minimal line.
- Avoid children's-book watercolor, dense outlines, and oversaturated greens.

## GOUACHE_POSTCARD

**Source policy:** experimental HYBRID/DISTILL, opt-in only.

Use only when the user explicitly asks for a painterly/gouache result or a validated reference clearly calls for it. Do not select this merely for batch variety.

- Reinterpret the source in opaque-but-soft gouache shapes with visible brush edges.
- Simplify forms more than watercolor but preserve silhouette and spatial rhythm.
- Use 4-7 source-derived colors, slightly warmed and muted.
- Keep one or two crisp anchors (roof, boat, bridge, sign, tree trunk) amid softer shapes.
- Typography: small postcard title; optional one-line note.
- Avoid glossy digital painting, hyperreal brushwork, and children's illustration.

## RISO_POSTCARD

**Source policy:** experimental HYBRID/DISTILL, opt-in or clearly reference-led.

Use for selected decorative details, architecture, boats, urban geometry, market scenes, or photos with 2-4 strong colors when printmaking is genuinely the point.

- Reduce the image to 2-4 ink layers with slight misregistration.
- Use coarse grain, flat ink, halftone, and paper absorption.
- Keep the subject silhouette and key geometry unmistakable.
- Allow one bright source-derived spot color to do structural work.
- Typography: small bold grotesk, mono, or loose handwritten annotation.
- Avoid rainbow palettes, perfect vector edges, and dense commercial poster layouts.

## CYANOTYPE_MEMORY

**Source policy:** experimental HYBRID/DISTILL, opt-in or clearly reference-led.

Use for botanical scenes, old architecture, silhouettes, lake edges, branches, railings, and quiet memories only when the cyanotype treatment is explicitly desired or clearly supported by a validated reference.

- Use a deep cyan / Prussian blue print field with pale paper/white exposed forms.
- Preserve source silhouette and negative-space relationships.
- Optional second warm paper tone may appear as a small accent only.
- Excellent for willow branches, railings, roofs, carved details, and leaves.
- Typography: tiny serif or handwritten note, preferably in the margin.
- Avoid turning every object into equal-detail blue line art; prioritize silhouette and atmosphere.

## LINOCUT_HERITAGE

**Source policy:** experimental DISTILL, opt-in or clearly reference-led.

Use only when the user wants a printmaking interpretation or a validated reference strongly supports it. Do not replace a strong heritage photograph simply because linocut is available.

- Translate the source into carved black / dark-ink shapes and strong negative space.
- Preserve architectural axis, roof rhythm, stone texture, or motif silhouette.
- Use one restrained secondary ink color only if useful (vermilion, moss green, muted blue, ochre).
- Let carved line direction reinforce form.
- Typography: small serif / wood-type inspired title; no ornate faux-historical lettering.
- Avoid fantasy illustration and excessive micro-detail.

## NEWSPRINT_CITY

**Source policy:** HYBRID.

Use for city roads, hutongs, crowds, transit, architectural reportage, and documentary scenes.

- Keep the source photo readable but translate large regions into black/gray newsprint halftone.
- Add one restrained accent color from the source (red lantern, amber streetlight, blue sign, green tree).
- Use paper grain, ink spread, and slightly imperfect registration.
- Typography: compact headline + tiny date/location-like poetic microcopy if desired.
- Avoid fake newspapers, long articles, political headlines, or dense faux journalism.

## CLEAN_EDITORIAL

**Source policy:** PRESERVE.

Use when the source is already visually strong.

- Preserve 80-95% photographic character.
- Use subtle matte paper / film texture, gentle tonal unification, and restrained typography.
- One small text block or no text if the image is stronger without it.
- Do not decorate for decoration's sake.

## EDITORIAL_CITY

**Source policy:** PRESERVE or HYBRID.

Use for towers, roads, flyovers, vehicles, blue hour, and modern city geometry.

- Keep architecture and roads photographically recognizable.
- Use clean geometric accents, subtle halftone, directional lines, or light print texture.
- Prefer cool gray-blue with source-derived warm lights.
- Typography: modern grotesk or narrow sans, small and left-aligned.
- Avoid cyberpunk, neon overload, sci-fi additions, and heavy commercial poster styling.

## SOFT_ANALOG_EDITORIAL

**Source policy:** PRESERVE.

Use for travel, architecture, street, landscape, portraits, and dusk.

- Preserve the whole photograph.
- Keep tonal shaping subtle. Grain and color cast are optional; do not add them unless the source already supports analog character or the user wants it.
- Add one deliberate layout gesture only: thin rule, tiny caption, quiet margin, or minimal type block.
- Think magazine opener, not filter preset.
- Typography: refined sans/serif, low contrast to the image.
- Avoid fake dust, heavy light leaks, excessive faded-vintage effects.

## ANALOG_DIARY

**Source policy:** PRESERVE.

Use for candid travel memories, streets, friends, walks, food, transit, and everyday scenes.

- Keep photo realism and casual framing.
- Add subtle date-like notation, handwritten side note, grease-pencil circle, underline, or one small doodle derived from the scene.
- The diary marks should occupy less than 10-15% of the frame.
- Preserve imperfect snapshot energy rather than "fixing" everything.
- Avoid sticker overload, cartoon mascots, and scrapbook maximalism.

## FILMSTRIP_DIARY — disabled by current project preference

Do not select this recipe by default. The user explicitly disliked the filmstrip-style treatment. Re-enable only if the user later asks for it. This is a scoped project preference, not a reason to suppress all photo-led or analog treatments.

## CONTACT_SHEET_STORY — disabled

Do not use this recipe in the current skill. Contact-sheet/grid-mosaic photo layouts conflict with the final batch hard-failure rule.

## VINTAGE_TRAVELOGUE

**Source policy:** PRESERVE or HYBRID.

Use for heritage sites, lakes, old streets, stations, bridges, and destination memories.

- Keep the photo or a large faithful region.
- Add restrained aged-paper tone, softened inks, small caption blocks, and archival travel-book composition.
- Use subtle border or inset image only if source geometry allows.
- Color stays source-derived, slightly muted and warm.
- Avoid sepia overload, fake postal stamps everywhere, distressed edges, or theme-park nostalgia.

## ARCH_STUDY

**Source policy:** HYBRID.

Use for palaces, temples, towers, bridges, strong symmetry, roof sequences, and urban architectural geometry.

- Preserve the key photo architecture.
- Simplify secondary areas into architectural study drawings, ink wash, or flat color blocks.
- Keep axis, roofline, wall, bridge, skyline, and layer relationships correct.
- Use restrained ivory, gray, muted green, blue-gray, vermilion, or earthy yellow.
- Typography: refined serif or modern architectural sans.
- Avoid turning the whole image into traditional ink painting or technical CAD.

## SWISS_GRID_TRAVEL

**Source policy:** PRESERVE or HYBRID.

Use for architecture, city geometry, strong negative space, modern buildings, museums, stations, and minimal landscapes.

- Build a strict but quiet grid around the source photo.
- Use flush-left typography, small scale hierarchy, strong alignment, and generous margins.
- One photographic hero area + one or two small analytical crops/blocks maximum.
- Use black/charcoal type with one source-derived accent color.
- Typography: neutral grotesk / neo-grotesk, clean spacing.
- Avoid turning the result into corporate presentation design or overwhelming the photo with giant type.

## DUOTONE_BRUTALIST

**Source policy:** HYBRID.

Use for towers, flyovers, roads, concrete structures, strong shadow geometry, and bold architectural scenes.

- Convert one region or the whole image into a controlled two-color print system.
- Use large blocks, cropped geometry, thick rules, and strong but sparse type.
- Palette must come from the source or a close tonal interpretation.
- Keep enough photographic texture to avoid flat vector sameness.
- Avoid red-black cliche unless source colors justify it; avoid maximal brutalist clutter.

## PAPER_APERTURE

**Source policy:** PRESERVE.

Use for a single strong landmark, tower, gate, roofline, bridge, or road perspective.

- Keep the source photo visible through one clean paper aperture: circle, arch, diamond, vertical slit, or source-inspired contour.
- The surrounding paper planes should be quiet, matte, and lightly dimensional.
- Add very small perspective-aligned typography or one short title.
- The aperture shape should reinforce the subject geometry.
- Avoid glossy 3D mockups, heavy shadows, or decorative folded-paper spectacle.

## DETAIL_GRAPHIC

**Source policy:** light HYBRID by default; DISTILL only when explicitly requested.

Use for carved dragons, reliefs, ornamental ceilings, tiles, patterns, and strong centered details. Keep the core photographic detail dominant unless the user asks for stronger abstraction.

- Keep the central detail highly recognizable.
- Abstract surrounding repetition or geometry more than the core motif.
- Use source-derived ornament and color logic.
- Typography should be tiny or absent.
- Avoid turning historical detail into unrelated fantasy art.

## PHOTO_DOODLE_LIGHT

**Source policy:** PRESERVE.

Use for candid streets, transit, friends, markets, cafés, casual travel, and playful moments.

- Preserve the photograph almost entirely.
- Add only 2-5 small doodle gestures: arrow, underline, orbit line, tiny star, rough frame, map-like line, or simple source-derived icon.
- Doodles should feel like pen marks made after printing the photo.
- Use one or two colors maximum, preferably sampled from the source.
- Typography: one handwritten title or margin note.
- Avoid mascots, cartoon faces, sticker bombing, manga bubbles, or neon scribble overload unless explicitly requested.

## SURREAL_POP

**Source policy:** HYBRID.

Use sparingly for a single strong source-derived motif such as a lantern, boat, dragon, road, or architectural fragment.

- Keep the subject recognizable.
- One impossible scale shift or spatial intervention is enough.
- Use 2-3 flat matte color families from the source.
- Add only a few hand-drawn lines or repeated source-derived elements.
- No gradients, fake 3D plastic, random props, or unrelated surreal objects.

## TRAVEL_TICKET_DIPTYCH

**Source policy:** PRESERVE + DISTILL within one composition.

### Intent

Create a **vertical top/bottom contrast composition** that feels like:

**real travel/life moment above + collectible illustrated travel ticket below**.

This recipe should feel like a quiet travel magazine spread or a refined souvenir card, not a gimmicky ticket mockup.

### Structure

- Overall composition: vertical.
- Top region: about 50% of the page.
- Bottom region: about 50% of the page.
- Top uses the uploaded original photo itself as the main visual. Preserve its composition, subject, color, light, scale relationships, and photographic realism as much as possible.
- Do not cartoonize, redraw, flatten, or heavily restyle the top half.
- Bottom background: warm off-white, light beige, ivory, or pale warm gray with subtle paper texture and generous breathing room.

### Ticket object

Place one horizontal collectible travel-ticket / souvenir-ticket card in the central area of the bottom half.

- Ticket size: roughly 55-75% of the lower region width.
- Leave generous whitespace around it, as if a physical ticket has been quietly placed on a clean page.
- Ticket stock: warm creamy white / light beige / ivory.
- Edges: clean and refined.
- Add slight paper thickness and a soft, restrained shadow.
- Include one obvious detachable-stub structure on the right or one side.
- Stub details may include fine vertical perforation, semicircular notches, regular ticket edge cuts, and small structured microtype.
- The object should read immediately as a travel souvenir ticket, but not as a strict functional train or airline ticket.

### Source analysis before illustration

Before designing the ticket, inspect the top photo for:
- subject;
- environment;
- mood;
- dominant palette;
- most recognizable elements;
- the visual relationship among those elements.

Extract only the most representative source-derived motifs.

### Ticket illustration language

Redraw the selected source elements into a refined, light, literary travel illustration.

Preferred visual language:
- fresh watercolor;
- light colored pencil;
- transparent wash illustration;
- travel-magazine illustration;
- refined cultural-brand packaging illustration.

Avoid children's cartoon style, anime, chibi, glossy 3D, photoreal digital painting, or hyper-detailed vector rendering.

### Ticket typography

Add one prominent English travel headline near the ticket's upper-left or primary visual area.

Suitable examples:
- `WANDERLUST`
- `ESCAPE`
- `VOYAGE`
- `SUMMER ROAD`
- `COASTAL DAY`
- `CITY STROLL`
- `MORNING TRIP`

Typography:
- elegant serif or refined uppercase display type;
- literary / magazine feel;
- not loud advertising type;
- not playful cartoon lettering.

Below the headline, optionally add one smaller English subtitle or slogan.

### Color swatches

Optionally add 3-5 small circular color swatches near the lower or lower-left portion of the ticket, extracted from the source photo.

### Negative constraints

Avoid overly complex collage, heavy vintage distressing, exaggerated ornament, busy typography, cartoon children's style, anime, flashy comic language, 3D render look, commercial advertisement feel, excessive saturation, unrelated invented subjects, oversized ticket, and official-looking fare/ticket forgery styling.
