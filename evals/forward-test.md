# Painterly Frame Skill — forward contract test

## Input scenario

One high-key outdoor portrait with a broad blue-white sky, low horizon, small seated figure, green foreground and one protected clothing accent. The user asks for a painterly remake that preserves the initial composition and colour balance while fixing weak-model cutout behaviour.

## Expected route

`Edit Target` → `Preserve-and-enrich`.

## Expected portable decisions

- Composition lock keeps ratio, crop/headroom, focal scale class, low horizon, quiet-area share and viewing path.
- Colour lock keeps the source high-key exposure, dominant sky field, supporting green ground, protected wardrobe/skin colours and one primary value/analogous contrast axis.
- No subject enlargement, dark grade, forced complementary split, new object or global LUT.
- Continuity then binds sky/subject/ground with mixed edges, contact/reflected colour/shared light and a cloud-to-field stroke current.
- The first pass uses a balanced character packet: verified face geometry, quiet skin turns, grouped hair, clothing weight/major folds, readable shoe construction/contact and important hand/prop contact, with no pore/thread/strand inventory.
- After inspecting the result, classify the observed character detail as Collapsed, Adequate or High-capacity/already-dense. If environment and person materials collapse together, restore only the focal person's necessary material structure while retaining a few context depth cues; if already adequate, add nothing.
- If the model renders cut-paper blocks, append only the cut-paper or sticker adapter; keep the locked composition and colour roles unchanged.

## Failure checks

Fail if the output:

1. turns the high-key frame into low-key teal/orange or another unowned global cast;
2. crops away the quiet sky or enlarges the subject without permission;
3. preserves the photo under one universal paint texture;
4. uses isolated slabs, uniform hard outlines or identical marks across skin, cloth, grass and sky;
5. leaves a malformed face uncorrected or claims success without reinspecting the corrected face;
6. leaves an important person materially generic when the inspected output shows detail collapse;
7. adds pores, thread inventory, individual hair strands, dense shoe stitching or global sharpening to an already adequate result;
8. applies a continuity adapter that redesigns the composition or colour ownership.
