# Paint Architecture Contract

Use this reference whenever a prompt, edit, generation, or review mentions large colour shapes, planes, brushwork, material marks, or cross-model consistency. It closes terms that image models otherwise interpret as cel shading, low-poly faceting, posterization, or a global paint filter.

## Target

The target is a spatially believable scene rebuilt as designed painted shapes. Form must remain readable before surface texture is added. Brushwork describes a material or transition; it never substitutes for composition, volume, identity, or light.

Cross-model consistency means the outputs share the same **paint architecture fingerprint**:

- selective rather than fully inked contours;
- hierarchical, light- and material-derived planes rather than uniform polygons;
- broad-to-small mark scale with a focal-to-context density falloff;
- visibly different construction for different materials;
- three-dimensional overlap and atmosphere beneath restrained flat graphic intervention.

It does not mean identical pixels or identical brush stamps.

## Closed Vocabulary

Use these meanings. Do not rely on the bare words `painterly`, `faceted`, `large brushwork`, `animation`, or `stylized`.

| Term | Operational meaning | It is not |
|---|---|---|
| Macro mass | One contiguous compositional area with an owner, value role, contour, overlap and direction; together the masses fill the canvas | a visible brush stamp, horizontal poster band, or per-object flat fill |
| Major structural plane | A broad region created by a change in surface orientation, light exposure, material boundary, or intentional silhouette simplification | random triangulation, equal-size mosaic pieces, or two-tone cel shading |
| Transition plane | A subordinate bridge between major planes that clarifies turning form, reflected light, or material change | a decorative polygon added to look complex |
| Material mark | A bounded directional trace whose scale, edge and rhythm follow a named material | one repeated texture or canvas grain over the whole image |
| Graphic accent | A sparse contour fragment, seam, dry-brush vector, flat shadow break, atmospheric shape, or effect mark with a story/structure job | an outline around every object or a giant brush slab used as scenery |

## Mandatory Construction Order

Build and judge in this order. A later layer cannot repair a failed earlier one.

1. **Topology and silhouette:** preserve the declared identity, count, pose/action, prop state, orientation, contact, occlusion, depth order, landmark relation and key negative space. Simplify contours only inside that contract.
2. **Macro masses:** reduce the complete frame to roughly five to nine named interlocking masses. Record each mass's owner, approximate area, contour direction, overlap and value/colour role.
3. **Major structural planes:** divide only important forms where orientation, light, material or purposeful design changes. Use unequal, asymmetrical plane sizes with one dominant plane and fewer subordinate planes.
4. **Transition planes:** add only enough intermediate pieces to make turning form, reflected colour, folds or atmosphere readable. They must remain visually subordinate to the major planes.
5. **Material marks:** add marks inside or along already coherent forms. Their direction, scale, density, edge and reflectance must be owned by a material.
6. **Accents:** reserve the smallest, sharpest and highest-frequency marks for the focal path. Context receives only a few structural traces.

Run the **texture-removal test**: mentally remove all material marks and grain. The subject, depth, light direction and three value groups must still read. If form collapses, texture has replaced construction and the result fails.

## Plane Topology

### Legal causes for a plane break

A plane boundary must be justified by at least one of:

- surface orientation turning toward or away from the light;
- cast shadow, occlusion, reflected light or atmospheric separation;
- a real material or construction boundary;
- a fold family caused by tension, compression, gravity or contact;
- an intentional graphic simplification that strengthens silhouette, gesture or focal hierarchy.

### Starting counts, not quotas

- Inspectable focal face/object: usually 4–7 major planes before tiny accents.
- Supporting subject or prop: usually 3–5 grouped planes.
- Context object group: usually 1–3 broad planes; merge repeated objects into rhythm masses rather than faceting each instance.

Do not add planes merely to reach a count. Do not make them equal in size. Do not outline every plane. One broad plane should carry most of each important form, with fewer unequal supporting planes.

### Plane separation

Separate adjacent planes primarily through controlled value, temperature, chroma, edge or material response. Use a dark drawn line only when it is an observed seam, an overlap, a focal contour fragment, or a deliberately selected graphic accent. A continuous ink contour around a complete face, body, garment, cloud, tree line or building is a cel/comic failure unless the user explicitly requests that medium.

## Mark Hierarchy and Coverage

Use a density ladder rather than distributing brush texture evenly:

- **Tier 1 focal:** relative mark density `1.0`; broad structural joins plus a few medium/small accents.
- **Tier 2 support:** about half the focal density; mostly broad and medium marks.
- **Tier 3 context:** about one fifth to one third of focal density; broad grouped traces only, with selected perspective or material cues.

These are perceptual ratios, not pixel measurements. The rule is visible when the focal area contains the finest useful mark and context never contains a competing field of equally sharp repeated marks.

Keep these scale relationships:

- macro mass is larger than any visible brush mark;
- major plane is larger than the transition marks it contains;
- material marks are smaller than the form they describe and follow its volume or motion;
- accents occupy the least area and never tile the canvas.

Reject opaque rectangular strokes that impersonate clouds, mountains, fields, walls or water without following their volume. Reject an all-over canvas texture, identical dry-brush edge on every object, or one brush size repeated from foreground to background.

## Structural Large Marks

Large visible brushwork is a valid part of the target when it constructs a named mass. Do not shrink every mark into safe, evenly distributed impasto merely to avoid the brush-slab failure.

A structural large mark:

- follows cloud turning, field/foliage growth, water flow, fold expansion, wall perspective, rock weight, light direction, atmospheric shear, or another visible form/motion cause;
- interlocks with neighbouring marks into a coherent volume or current rather than floating as an isolated stamp;
- remains smaller than and subordinate to the macro mass it describes;
- changes scale, direction, edge and opacity according to material and depth;
- strengthens a contour, area relationship, viewing path, or three-value read at thumbnail or mid scale.

A decorative brush slab:

- is an opaque rectangle or repeated stamp with no volume, perspective, light, material or motion job;
- replaces a cloud, field, wall, mountain or water body with one flat plate;
- repeats the same edge, scale and orientation across unrelated materials;
- becomes the scene's main attraction while the subject, light and depth remain underdesigned.

Run the **structural-large-mark test**: name the owner, form/motion cause, direction, depth tier and material grammar of every conspicuously large stroke. If those fields cannot be named, reduce or rebuild it. A scene may share a coherent painted medium; coherence does not permit material interchangeability.

## Material Construction Library

Choose only materials present in the scene. Derive an unlisted material from rigidity, reflectance, porosity, motion and focal importance.

| Material | Major-plane construction | Material marks and edges | Reject |
|---|---|---|---|
| Skin | quiet wedge and curved planes following brow, cheek, nose, jaw and limb cylinders; shadows stay chromatic | very few soft joins; tiny hard accents only at selected features | generic anime face, enlarged eyes, porcelain gradient, black facial outline, impasto or stippling |
| Hair | one dominant dark/light mass plus 3–5 grouped directional ribbons | broken silhouette clumps and sparse sheen breaks | individual strand rendering, helmet fill, repeated glossy stripes |
| Woven/soft cloth | plane families follow gravity, tension points and compressed folds | broad dry joins, selective seam or fold-tip accents | evenly spaced triangles, every wrinkle traced, identical treatment to skin |
| Rigid fabric/rainwear | larger angular planes defined by construction and sharper fold changes | sparse controlled specular seams | wet plastic gloss over every fold |
| Grass/foliage | 2–4 clustered masses per depth zone, not a blade/leaf inventory | a few directional foreground blades; progressively broader and quieter marks with depth | full-field repeated strokes, uniform neon green, leaf-by-leaf texture |
| Sky/cloud | broad atmospheric value fields whose edges turn with cloud volume and light | soft joins, broken vapor edges, a few directional scumbles inside the volume | giant opaque white rectangles, decorative brush slabs, equal hard edges |
| Water | broad flow ribbons and pressure/foam masses aligned to current or wave | broken foam seams, selected crisp crests, lost mist edges | equal short strokes everywhere, pasted white texture |
| Rock/earth | a few interlocking weight-bearing planes following fracture and slope | selective cracks and granular accents near focus | random low-poly triangulation, uniform pebble noise |
| Snow/ice | broad light/shadow fields shaped by terrain and compression | sparse crust edges, wind ribbons and reflected-colour seams | featureless white fill or noisy blue texture |
| Wood | long planes following grain and construction | limited directional grain breaks at focal scale | grain texture over every surface |
| Metal | compact planar reflections tied to light and surrounding colour | sparse crisp streaks and hard seams | glossy outline around the whole object, chrome on unrelated materials |
| Architecture | perspective-correct masses and a few load-bearing planes | selected corners, joins and window rhythm | white block inventory, every window outlined, arbitrary cubist facets |
| Fog/smoke | overlapping translucent masses with depth-owned value | lost edges, occasional sharper core or shear boundary | uniform gray veil over the image |

### Material-swap test

Choose three visible materials. Imagine exchanging their mark grammar while keeping colour constant. If the swap would be hard to notice, the materials are not differentiated enough. Skin marks must not work unchanged on grass; cloud marks must not work unchanged on a skirt; rock planes must not work unchanged on a face.

## Identity and Source Fidelity

For edit targets, style reconstruction does not authorize a generic character replacement. Record and preserve, unless the user explicitly releases them:

- facial identity and feature spacing;
- body proportion, pose, gesture and gaze;
- prop type, open/closed state, orientation and hand contact;
- subject/landmark positions, left-right order, depth order and overlap;
- key negative-space shapes and dominant motion lines;
- protected wardrobe, product or local colours.

Planes may simplify an identity; they may not replace it with a model's default anime face, fashion pose, body type, expression or prop state.

## Portable Paint-Architecture Packet

Write this packet before model-specific wording:

```text
Paint architecture:
- Contour language: [selective hard fragments / broken medium edges / lost context edges; complete outlines forbidden].
- Plane topology: [focal 4–7 unequal light/material-derived planes; support 3–5; context grouped into 1–3 broad planes].
- Plane causes: [orientation/light/material/fold/graphic reason for the important breaks].
- Mark ladder: [focal 1.0 / support about 0.5 / context 0.2–0.33; broad-to-small scale].
- Material ownership: [material A construction and marks]; [B visibly different]; [C visibly different].
- Texture-removal result: [what silhouette, depth, light and value groups remain readable without surface marks].
- Forbidden shortcuts: [only the applicable cel/outline, brush-slab/filter, low-poly/posterization, generic-face failures].
```

This packet is the style anchor. A named artwork, model-specific quality tag, exact seed, or general phrase such as “painterly animation” is not a style anchor.

## Behaviour-based Model Adapters

Keep the portable packet unchanged. Append only the adapter matching an observed failure; do not identify a model by brand.

### Cel/anime shortcut

```text
No continuous ink contour, two-band cel shading, manga facial proportions or generic anime replacement. Preserve real feature spacing and build volume from unequal light-derived planes with mixed edges.
```

### Brush-slab/filter shortcut

```text
No global canvas texture, opaque rectangular scenery slabs without volumetric work, or one repeated brush edge. Allow structural large marks when they interlock into a named volume/current and follow its material, light, perspective or motion. Macro masses and volume must read before local marks.
```

### Low-poly/posterization shortcut

```text
No triangulated mosaic, equal-size polygon tiling or horizontal poster bands. Every important plane break must come from orientation, light, material, fold mechanics or a declared silhouette decision; keep one dominant plane per form.
```

### Source-template shortcut

```text
Do not replace the source with a generic scene containing similar nouns. Preserve the declared pose, prop state, contact, orientation, adjacency, overlap, landmark relationship and negative-space map.
```

If the selected runtime does not obey the portable packet after one targeted adapter, report it as outside the supported consistency envelope rather than adding an unlimited stack of adjectives.

## Immediate Failures

Fail the output before polish scoring when any applies:

- it reads primarily as cel-shaded anime or a vector/cartoon poster;
- a complete subject is enclosed by a uniform dark outline;
- the focal form is an equal-size polygon mosaic or mechanical triangulation;
- giant decorative brush slabs replace the volume of sky, cloud, land, water or architecture; structurally caused large marks are allowed;
- texture or grain is spread uniformly across unrelated materials;
- the same mark grammar can be swapped across three important materials;
- removing texture destroys the form, light or depth read;
- context has the same small-mark density and hard-edge frequency as the focal area;
- an edit preserves only object nouns while changing identity, pose, prop state, adjacency or scene topology.
