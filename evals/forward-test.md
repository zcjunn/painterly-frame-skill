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
- If the model renders cut-paper blocks, append only the cut-paper or sticker adapter; keep the locked composition and colour roles unchanged.

## Failure checks

Fail if the output:

1. turns the high-key frame into low-key teal/orange or another unowned global cast;
2. crops away the quiet sky or enlarges the subject without permission;
3. preserves the photo under one universal paint texture;
4. uses isolated slabs, uniform hard outlines or identical marks across skin, cloth, grass and sky;
5. applies a continuity adapter that redesigns the composition or colour ownership.
