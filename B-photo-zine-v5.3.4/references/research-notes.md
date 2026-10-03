# Research Notes — distilled design lessons

> **R6 runtime rule:** Research expands the toolbox only. It does not create default behavior, does not gain weight because it is new, and does not override source fidelity or user-approved baselines.

The original research images and raw tutorial/reference material are intentionally not shipped in the runtime package. Only transferable principles remain here.

## Transferable lessons
- Define a style by **composition logic + source policy + material behavior + color logic + typography hierarchy + negative constraints**, not by fashionable adjectives alone.
- Separate photographic treatment from graphic treatment. A photo can remain truthful while the page around it changes.
- Negative space and density control are often more valuable than adding decoration.
- Medium choice should change real visual behavior (edge, ink, wash, paper, registration) rather than merely add a style word.
- Strong source geometry, light, crop, and depth should be described independently from graphic styling.
- New mediums are **optional vocabulary**, not required batch roles.

## Runtime status of experimental media
The following are available only conditionally:
- `GOUACHE_POSTCARD` — explicit painterly intent or clearly validated reference;
- `RISO_POSTCARD` — explicit/clearly reference-led print treatment;
- `CYANOTYPE_MEMORY` — explicit/clearly reference-led cyanotype treatment;
- `LINOCUT_HERITAGE` — explicit/clearly reference-led printmaking treatment;
- `DUOTONE_BRUTALIST` — only when source geometry and user intent strongly support it.

The following are disabled for this project unless the user explicitly reopens them:
- `FILMSTRIP_DIARY`;
- `CONTACT_SHEET_STORY`.

“Swiss grid” refers only to **single-page alignment/typographic structure**, never to a multi-photo nine-grid/contact sheet.

## Core recipe rule
A robust recipe may specify:

`source policy + composition grammar + material behavior + color logic + typography hierarchy + negative constraints`

This makes a chosen style coherent. It does **not** imply that a batch must demonstrate multiple styles.

## Archive policy
Once a research image/tutorial has been distilled into stable text, do not keep it in the distributable runtime unless forensic re-analysis is specifically needed. This keeps the package light and prevents old research images from becoming accidental templates.

## Distilled examples from removed research-only material
- **Last Blue** — useful principle: a narrow dominant color field plus silhouette/line rhythm can carry a page. Do not conclude that every dusk image needs brush masks or a script title.
- **Lakeside Line** — useful principle: architectural framing and directional depth can support a calm editorial split with low-density copy. Do not conclude that every travel image needs botanical decoration or the same serif hierarchy.
