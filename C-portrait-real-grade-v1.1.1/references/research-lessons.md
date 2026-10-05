# Portrait research lessons

This file distills external guidance into C's runtime logic. Research sources are kept as links/text rather than copied images.

## 1. Person/background edits should be local, soft, and separable
Adobe Lightroom's masking system can select people and specific parts such as skin, hair, and clothes; its brush controls include Feather, Flow, and Density for soft transitions. This supports C's rule that portrait hierarchy should come from local, feathered adjustments rather than hard cutout edges.

Source: Adobe Lightroom — Apply Masking for local adjustments
https://helpx.adobe.com/lightroom/desktop/edit-photos/masking.html

## 2. Depth blur should follow depth, not a binary subject cutout
Lightroom Lens Blur uses a depth map and adjustable focus range, and allows separate refinement of focus/blur. C therefore treats foreground, subject plane, midground, and far background differently instead of applying one uniform blur to everything outside the person.

Sources:
https://helpx.adobe.com/in/lightroom-classic/desktop/process-and-develop-photos/lens-blur.html
https://helpx.adobe.com/lightroom/mobile/adjust-light-and-color/apply-lens-blur.html

## 3. Cinematic color is better built by tonal ranges
Lightroom Color Grading separates shadows, midtones, and highlights and provides Blending/Balance controls. C uses this as a model for restrained cinematic separation instead of a single global color wash.

Sources:
https://pages.adobe.com/lightroom-classic/en/learn/color-grading/
https://www.adobe.com/learn/lightroom-cc/web/adjust-photo-tone-with-color-grading

## 4. Film character can be subtle
Adobe's film-look guidance combines warm tonal character, fine grain, lower contrast, selective color work, and softened detail. C uses grain/softness as a finishing layer, not as a substitute for good light and hierarchy.

Source:
https://helpx.adobe.com/ee/lightroom-cc/how-to/create-film-style-look.html

## 5. Skin tone correction should be local and transition smoothly
Capture One's Skin Tone tools are designed to correct patchy/unwanted variation and emphasize smooth transitions; its guidance recommends local masks so skin corrections do not spill into other similarly colored areas. C therefore avoids global skin homogenization.

Sources:
https://support.captureone.com/hc/en-us/articles/360002596077-Adjusting-skin-tones
https://support.captureone.com/hc/en-us/articles/360002601358-The-Color-Editor-overview
https://support.captureone.com/hc/en-us/articles/360007944857-Making-local-adjustments-with-the-Color-Editor

## 6. Over-softening creates plastic skin
Capture One explicitly warns that excessive Clarity-based skin softening can produce unnaturally smooth/plastic texture. C preserves pores and natural facial microtexture.

Source:
https://support.captureone.com/hc/en-us/articles/360002605677-Softening-skin-in-portraits

## 7. Subject and background can be isolated as separate layers
Capture One supports subject/background/people masks and luma-range refinement. Its examples show light, contrast, white balance, and clarity being adjusted separately to create separation. C generalizes this as “relationship-based prominence,” not synthetic relighting.

Sources:
https://support.captureone.com/hc/en-us/articles/14055231933853-AI-Masking
https://support.captureone.com/hc/en-us/articles/360002622857-Creating-a-Luma-Range-Mask
https://www.captureone.com/blog/combining-masks-in-capture-one

## 8. Faces attract disproportionate viewer attention
Blackmagic Design's colorist training notes that viewers pay strong attention to faces and presents face isolation as a secondary correction after the shot is balanced. C follows the same order: stabilize the whole photograph first, then make localized portrait corrections.

Source:
https://documents.blackmagicdesign.com/UserManuals/DaVinci-Resolve-20-Colorist-Guide.pdf

## Transferable synthesis for C
- Base grade first; portrait isolation second.
- Preserve identity and natural texture before creating mood.
- Use soft local masks and small differences to establish hierarchy.
- Protect skin while grading environment separately.
- Make background softness depth-aware.
- Night atmosphere should stay dim and practical-light-driven.
- Add film texture last.

## 9. Whole-person retouch should separate structure from appearance
Professional retouch tools support local face, hair, clothing, subject, and background work rather than forcing one global “beautify” pass. C therefore treats the visible person as multiple adjustment regions while preserving one structural identity.

## 10. Shape correction should be local and geometry-protected
Liquify-style deformation is most believable when small, local, and protected from nearby architecture/straight lines. C prefers clothing drape and local tonal shaping first, then minimal contour deformation only if necessary.

## 11. Pose tools are not default beauty tools
Warp/pose tools can alter hair or body position, but large structural changes easily rewrite the photographed moment. In C they are exceptional, user-driven tools, not standard enhancement steps.

## 12. Face cleanup should preserve dimensional light
Dodge/burn and healing-style logic supports correcting small tonal/texture distractions without flattening or regenerating facial structure. C therefore avoids uniform face brightening and protects nose/eye/lip geometry.

## 13. New research modules have neutral weight
Research-derived techniques are options, not presets. Their presence in this file does not increase their runtime priority. C only activates the smallest relevant module set for the current image and user request.
