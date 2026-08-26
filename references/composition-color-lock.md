# Composition and Colour Lock

Read this reference before directorial restaging, paint architecture, or model-specific wording. It restores the initial Painterly Frame control layer: composition and colour are decided first, then continuity rules explain how the image is painted.

## Precedence

The lock is a decision contract, not a request for photographic literalness.

1. Preserve the user's explicit ratio, crop, topology, identity, action, landmark relations and protected colours.
2. When a photo is supplied and the user does not specify a different canvas, measure its actual pixel width and height and inherit that exact aspect ratio. A resized preview, a common preset, or the runtime's default canvas is not permission to change the ratio. If several photos are processed independently, each target carries its own source ratio.
3. If an Edit Target already has an effective distribution, use **Preserve-and-enrich** by default: keep the source camera, focal scale class, headroom, horizon share, quiet-area share, major diagonal/current and colour-area hierarchy.
4. If the user explicitly asks for Style-first/Expressive/Radical restaging, or the Source Card identifies a real compositional failure, use **Directed-restage**: declare one primary macro departure and one supporting move before changing the distribution.
5. Use the painterly continuity contract only after these choices are fixed. Continuity binds masses together; it does not enlarge the subject, compress the sky, invent a new colour script or change the exposure key.

Do not make a source look more “painterly” by automatically tightening the crop, enlarging the face, lowering the sky, adding a dark vignette or forcing complementary colour.

## Composition Lock Record

Write this before the final prompt:

```text
Composition lock:
- Mode: Preserve-and-enrich / Directed-restage.
- Canvas: exact source-derived ratio (pixel width:height), orientation, borderless output and shot scale; state any explicit user override.
- Topology anchors: subject count, action/gaze, depth order, adjacency, landmark positions.
- Distribution to preserve or change: crop, headroom, horizon, focal scale, quiet-area share,
  major negative-space owner, dominant diagonal/current and viewing path.
- Focal zone: perceptual first-read region and the two or three cues that own it.
- Restage permission: exact user-authorized changes only.
- If Directed-restage: one primary macro departure, one supporting move and the protected anchors.
```

### Preserve-and-enrich

Choose this for a strong environmental portrait, quiet landscape, high-key scene, or any source whose empty space already creates the feeling. Enrich the existing decision through grouped value planes, light geometry, local colour turns, edge hierarchy, material marks and a viewing-path current. The result may be visibly painted without changing the source's area map.

### Directed-restage

Choose this only with permission or a diagnosed imbalance. The macro change may be scale takeover, area reallocation, crop/restage, foreground occlusion, perspective compression, negative-space takeover, light-shape rearchitecture or colour-zone restaging. Name what changes and what does not. A new colour cast or more texture is not a macro departure.

## Colour Lock Record

Audit the source before naming hues. Record:

```text
Colour lock:
- Exposure key: High-key / Mid-key / Low-key, with scene reason.
- Source strengths: colour relationships already carrying mood, identity or depth.
- Source problems: only the hue/value/chroma/adjacency issues that need correction.
- Value groups: dominant field, supporting structure, small apex; area hierarchy from the source
  unless a restage is explicitly allowed.
- Spatial colour roles: dominant field, structural counter, focal apex, connector/echo,
  neutral bridge and their owners.
- Protected local colours: identity, wardrobe, product, species, signage or architecture.
- Primary contrast axis: one of value, analogous, complementary, warm-cool, saturation,
  hue-boundary, near-monochrome rupture or local-colour versus illumination.
- Subordinate axis: optional; do not maximize every axis.
- Collision: None / Preserve existing / Author new, with owners, boundary, dominant side and job.
```

### Preserve-and-refine is the default

Keep source hue families and protected anchors when the palette already works. Improve separation through value grouping, saturation hierarchy, neutral balance, shadow coherence and local adjacency. Rebalance only the area/value/chroma ownership that causes a real focal or depth problem. Re-script only when the user allows a new palette or the source palette actively prevents the requested hierarchy.

Do not inherit a fixed warm/cool, teal/orange, complementary or dark grade from a style label. A quiet analogous or near-monochrome source may be the stronger design.

## Prompt Ordering

The final prompt should present decisions in this order:

1. preserve/transform anchors and composition distribution;
2. three value groups, exposure key and spatial colour roles;
3. directorial proposition and any permitted macro departure;
4. continuity: internal turns, boundary relations, shared light and stroke current;
5. material grammars, edge hierarchy and selective 2D marks;
6. only the shortest observed failure adapter.

This ordering prevents a weak model from satisfying “painterly” with texture while losing the picture's initial colour and composition.

## Lock Failure Conditions

Reject or correct when:

- an Edit Target loses the source's effective negative space, subject scale class, horizon or viewing path without permission;
- a supplied photo is silently rendered at a stock ratio, stretched, padded or cropped instead of inheriting its measured source ratio (unless the user explicitly overrides it);
- a Preserve-and-enrich edit invents a new dominant hue family, darkens a high-key scene or moves the focal apex to the background;
- colour roles are listed without spatial owners, or every region receives similar saturation and contrast;
- the output uses a global LUT/grade as a substitute for local colour decisions;
- a macro departure is claimed but only texture, grain, fog, bloom, slight hue shift or polygon count changed;
- continuity clauses create equally busy, equally sharp or equally saturated masses and erase the quiet field;
- an adapter changes composition, exposure, protected local colour or focal ownership instead of correcting its named rendering shortcut.

## Compact Prompt Block

```text
Composition/color lock: use [Preserve-and-enrich or Directed-restage]. Preserve [ratio, crop/headroom/horizon, focal scale, quiet-area share, topology and viewing path] unless explicitly changed by [permission]. Organize [dominant field], [supporting structure] and [small apex] under a [high/mid/low]-key light. Assign [dominant field], [structural counter], [focal apex] and [neutral bridge] to their spatial owners; use [one primary contrast axis], preserve [local-color anchors], and make no unowned global grade. Only after this lock, connect the masses with internal colour turns, mixed edges, shared light and interlocking material-specific strokes. Add [one observed failure adapter] only if needed, without changing the lock.
```
