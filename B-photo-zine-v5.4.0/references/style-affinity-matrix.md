# Style Affinity Matrix v5.1

## Strength and photographic-restraint scope

Read `delivery-contract.md` first. Default strong B is independent of photographic T/PRESERVE. Quiet/photo-led means less repainting/clutter, not weaker page design; historical taste cannot lower the current contract.

This matrix provides a deterministic prior for candidate generation. Values are 0-3:
- 0 = generally weak
- 1 = situational
- 2 = useful
- 3 = strongly aligned

It is a prior, not a final decision. Contraindications and source-damage risk can override it.

| Family | Geometry | Negative space | Light | Color | Texture | Narrative | Detail | Second World | Text tolerance |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| A Ticket | 1 | 2 | 1 | 2 | 1 | 2 | 1 | 0 | 3 |
| B Watercolor | 1 | 2 | 2 | 3 | 1 | 1 | 1 | 0 | 2 |
| C Minimal Collage | 3 | 3 | 1 | 2 | 1 | 1 | 2 | 1 | 3 |
| D Second World | 3 | 2 | 1 | 1 | 1 | 3 | 1 | 3 | 2 |
| E Analog Diary | 1 | 1 | 3 | 2 | 2 | 3 | 1 | 0 | 1 |
| F Museum | 2 | 3 | 1 | 1 | 3 | 1 | 3 | 0 | 2 |
| G Light Poetry | 1 | 3 | 3 | 2 | 1 | 1 | 0 | 1 | 1 |
| H Cinematic | 2 | 2 | 3 | 2 | 1 | 3 | 0 | 1 | 1 |
| I Modern Chinese | 2 | 2 | 1 | 3 | 3 | 1 | 2 | 0 | 2 |
| J Magazine | 2 | 2 | 2 | 2 | 1 | 2 | 1 | 0 | 3 |
| K Documentary | 2 | 1 | 2 | 0 | 3 | 3 | 2 | 0 | 1 |
| L Detail Card | 2 | 2 | 1 | 2 | 3 | 0 | 3 | 0 | 2 |

---

## Using the matrix

For each profile dimension scored 0-3, multiply it by the corresponding affinity and sum the relevant terms. Normalize only enough to rank candidates; do not treat this as a photographic truth score.

Example rough prior:

```text
prior =
  geometry_strength * GeometryAffinity +
  negative_space * NegativeSpaceAffinity +
  light_value * LightAffinity +
  color_value * ColorAffinity +
  texture_value * TextureAffinity +
  narrative_strength * NarrativeAffinity +
  detail_extraction_value * DetailAffinity +
  second_world_potential * SecondWorldAffinity +
  text_tolerance * TextToleranceAffinity
```

Then apply:
- archetype boost;
- subject compatibility as a weak prior;
- transformability compatibility;
- contraindications;
- source-damage penalties;
- batch-diversity value.

## Special correction rules

- If `color_value = 3`, K Monochrome receives an additional risk flag unless the color can be intentionally retained as a controlled accent.
- If `second_world_potential < 2`, D should usually be removed from the candidate pool.
- If `negative_space = 0`, G should usually be removed unless light alone clearly drives the image.
- If `detail_extraction_value = 0`, L should be removed.
- If `text_tolerance = 0`, A and J should be heavily penalized.
- If `light_value = 3` and the original light is already exceptional, prefer PRESERVE families before painterly or DISTILL families.
