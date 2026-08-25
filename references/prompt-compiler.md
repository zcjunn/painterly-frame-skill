# Prompt Compiler

Compile research and Source Cards into visible pixel decisions. Keep the final prompt shorter than the analysis.

## Compiler Order

1. **Canvas:** output count, aspect ratio, orientation, finished borderless image, shot scale.
2. **Source contract:** image role, semantic minimum, recognition anchors, transformable elements, identity fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, color-authorship mode, and allowed changes.
3. **Directorial proposition:** actor, visible pressure/counterforce, intended first read, one primary macro departure, one supporting move, protected anchors, and a thumbnail difference target from `directorial-contrast.md`.
4. **Focal actor and transformation:** one readable verb/relationship; for environment-emphasis, name the hero form, counterform/current, merged repeated detail, and the major area/contour/overlap/light/color impact of the primary departure.
5. **Attention geometry:** composition family, central attention zone, perspective, quiet area, viewing path.
6. **Value, light, and contrast ownership:** three mass groups, brightest/deepest placement, motivated source geometry, haze/rim restraint, and focal/support/context contrast tiers.
7. **Color authorship:** source strengths/problems; Preserve-and-refine, Rebalance, or Re-script; one primary contrast axis and at most one subordinate axis; dominant field, structural counter, focal apex, optional connector/neutral bridge; context chromatic-gray/quiet-color family; optional color-collision owners/adjacency/dominance/function; protected anchors.
8. **Paint architecture:** protected topology and silhouette; macro masses; unequal major planes with named causes; subordinate transition planes; focal/support/context mark-density ladder; non-interchangeable material marks; mixed edge ownership; spatial depth; limited graphic 2D intervention.
9. **FX:** only if story-motivated; unique shape language and edge hierarchy.
10. **Avoids:** the shortest relevant list of likely model errors and sample residue.

Do not include a rule that cannot become a visible pixel, tool parameter, source-role mapping, or quality check. Keep generation prompts compact: lead with the six to ten highest-impact decisions, remove redundant adjectives, and avoid long inventories that dilute shape reconstruction.

## Portable Core Before Model Wording

Write one model-neutral render contract before adding optional phrasing for a particular runtime. Keep its decisions concrete enough to survive paraphrase:

```text
Portable render contract:
- Canvas and anchors: [count, ratio, orientation, identity, pose/action, prop state/contact/orientation, adjacency/occlusion/depth order, landmark and negative-space invariants].
- Macro map: [five-to-nine named interlocking masses and their area/overlap relationship].
- Value and colour roles: [three value groups; dominant field, structural counter, focal apex, neutral bridge; protected colours].
- Contrast ownership: [Tier 1 focal peaks; Tier 2 support cues; Tier 3 context reductions].
- Paint architecture: [selective contour fragments; four-to-seven unequal focal planes with orientation/light/material/fold causes; subordinate transitions; merged repeated detail].
- Mark ladder: [focal 1.0; support about 0.5; context about 0.2–0.33; broad-to-small scale].
- Material grammar: [material A construction/mark scale/direction/edges/reflectance]; [B non-interchangeable]; [C non-interchangeable when present].
- Edge hierarchy: [hardest, medium, soft/lost owners].
- Texture-removal result: [silhouette, depth, light and value groups that remain without surface marks].
- Applicable shortcut adapter: [None / Cel-anime / Brush-slab-filter / Low-poly-posterization / Source-template].
- Anti-filter gate: [what must visibly differ from photographic underpainting at thumbnail, mid, and close scale].
```

Treat this block as required decisions, not prose to copy verbatim. Use [paint-architecture.md](paint-architecture.md) to close every plane, mark and material term. Put recognition invariants and the primary macro departure near the beginning of the final prompt and repeat the shortest critical preservation/avoid clause at the end. Avoid sampler, seed, model-version, quality-tag, house-style vocabulary, or a named artwork as the style anchor; those controls do not transfer reliably between model families. See [model-consistency.md](model-consistency.md).

## Compile Planes as Causes, Not Adjectives

Do not write only `faceted planes`, `large brushwork`, `painterly texture`, or `material detail`. Compile an observable packet:

```text
Paint architecture: preserve [topology anchors]. Use [selective contour language, with no complete ink outline]. Build [focal owner] from [4–7 unequal major planes] caused by [surface orientation/light/material/fold mechanics]; keep [support] to [3–5 grouped planes] and [context] to [1–3 broad planes per rhythm mass]. Marks fall from focal 1.0 to support about 0.5 and context about 0.2–0.33. [Material A] uses [construction and marks], while [B] and [C] use visibly non-interchangeable grammars. Without surface marks, [silhouette/depth/light/value groups] remain clear. Avoid [one applicable shortcut family].
```

Select a shortcut adapter by observed output behaviour, not model brand. Keep the portable core unchanged across models and append at most one primary adapter plus the source-template adapter when an edit has already drifted. If the runtime still fails after one targeted correction, report it outside the supported consistency envelope.

## Base Generate Template

```text
Create exactly one original [ratio/orientation] painterly-animation keyframe, a finished borderless image.

Scene and verb: [original subject, environment, one readable action/relationship]. Keep the focal event perceptually dominant inside the middle attention zone through [isolation/value/chroma/edge/perspective], while [quiet/occluding region] occupies a substantial part of the frame. Use [one composition family] and a believable spatial camera with clear foreground, middle, and atmosphere.

Directorial proposition: [actor] is [visible pressure/relationship] against [counterforce]; the first read is [event]. Make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relationship] is unmistakable at thumbnail scale; reinforce it with [supporting move]. Preserve [declared anchors], but do not preserve [incidental distribution].

Value, light, and contrast ownership: organize the frame into three large value groups: [dominant field], [supporting mass], and [small apex]. The primary light is [visible/motivated source with geometry]; reserve the brightest highlight and deepest dark for [focal path]. Tier 1 [focal owner] peaks in [two or three selected contrast dimensions]; Tier 2 [support] keeps medium structural cues; Tier 3 [context] becomes a unified [scene-owned colored/chromatic-gray] field through lower [local contrast/microcontrast/edge density/hue noise/texture frequency] while retaining [depth/material cues]. Use only a restrained subordinate [bounce/rim], controlled haze, and tight bloom.

Color authorship: use [Preserve-and-refine/Rebalance/Re-script] because [source/story reason]. Use [primary contrast strategy] with [optional subordinate strategy]. Assign [dominant field: spatial owner, hue family, value, chroma], [structural counter: owner and separation job], [focal accent/apex: owner and attention job], and [optional connector/neutral bridge]. Color collision is [None/Preserve existing/Author new: owners, adjacency, dominant side, function]. These roles may share one hue family when value/chroma does the work. Preserve [protected local-color anchors]. Let the motivated light influence rather than replace material color. Warm-cool is optional; avoid formulaic teal-orange, purple-neon, global gray fog, or equal saturated competition.

Rendering: grounded stylized proportions and spatial depth rebuilt through [named macro masses]. Use selective contour fragments rather than a complete ink outline. Build [focal form] from [4–7] unequal planes caused by [orientation/light/material/fold], with subordinate transition planes; keep repeated context in [1–3] broad planes per rhythm group. Marks fall from focal to support to context and stay smaller than the form they describe. [Skin construction and marks], [cloth visibly different], and [metal/wall/foliage visibly different]. The silhouette, three value groups, light direction and depth remain readable when surface texture is mentally removed. If FX are present, use [unique graphic shape language] with one sharp core, broad motion forms, sparse particles, and no global glow.

Avoid: franchise characters, logos, runes, copied architecture or camera layouts; generic anime facial replacement, two-band cel shading, complete black outlines, equal-size polygon mosaics, horizontal poster bands, giant opaque scenery strokes, all-over texture, interchangeable material marks, excessive bloom, sparks, wet gloss, or crushed muddy blacks.
```

Replace brackets. Remove irrelevant clauses rather than leaving generic filler.

## Edit Target Templates

Lead with change plus preservation:

```text
Edit Image 1 into one finished [ratio] painterly-animation keyframe.

Preserve as recognition anchors: [identity and feature spacing, count, pose/action/gaze, prop type/state/orientation/contact, subject/landmark positions, adjacency/occlusion/depth order, signature silhouette, key negative space/motion line, protected geometry/colours, required text]. Do not add, remove, substitute, or generically re-pose subjects.
Reconstruct: [transformable proportions/contours, crop/headroom, minor folds/hardware, repeated props, environment micro-detail, area/value/color/light/contrast organization]. Use [Identity-first/Balanced] transformation, [Restrained/Expressive] abstraction, [High/Mid/Low]-key exposure, and [Preserve-and-refine/Rebalance/Re-script] color authorship. Make [primary macro departure] and [supporting move] without changing [protected anchors].

[Then add attention geometry, three-group value plan, color roles, motivated light, faceted material/edge treatment, and relevant avoids from the base template.]
```

Do not claim exact pixels. If pixels or typography must be exact, keep those regions outside the generative edit and composite deterministically.

For **Style-first** photo remakes, use this shorter contract:

```text
Rebuild Image 1 as one finished [ratio] painterly animation keyframe; do not put an oil-paint texture over photographic shading.

Keep only these recognition anchors: [subject identity/count, action or pose, signature color anchors, essential spatial relationship]. Permit [crop, controlled proportion and contour stylization, merged folds/hardware/foliage/props, redesigned atmosphere and environment shapes].

Directorial abstraction: [dramatic proposition]. Make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relation] visibly differs from the source at 128–256 px; reinforce it with [supporting move]. Do not preserve [incidental distribution].

Shape and contrast design: use [Restrained/Expressive/Radical] abstraction. Preserve [topology anchors]. Build [subject] from [4–7 unequal major planes and their orientation/light/material causes], [support from 3–5 grouped planes], and [context rhythm masses from 1–3 broad planes]; transition pieces stay subordinate. Use focal/support/context mark density about [1.0/0.5/0.2–0.33]. [Material A construction/marks] must not work on [B] or [C]. Exposure is [high/mid/low]-key because [scene reason], with [three value groups]. Assign Tier 1 [focal], Tier 2 [support], and Tier 3 [chromatic-gray/scene-owned context quieting plus retained depth/material cues]. Color authorship is [mode] because [source/story diagnosis]; use [primary contrast], spatially assign [dominant/structural/focal/neutral roles], decide [None/Preserve/Author] color collision, and preserve [color anchors]. Make [focal event] the first read through [two cues]. Add [one restrained natural or FX graphic intervention].

Avoid photographic underpainting, source/result thumbnail layouts that differ only in surface texture, global impasto/filter texture, generic anime identity replacement, complete outlines, two-band cel shading, equal polygon mosaics, giant opaque scenery strokes, identical marks across materials, literal micro-detail, plastic skin, franchise motifs, unnecessary darkness, passive source color, forced warm-cool, global gray fog, and global LUT color.
```

For a **Style-first environment-emphasis** remake, use this explicit abstraction contract instead of a generic landscape prompt:

```text
Rebuild Image 1 as one finished [ratio] painterly animation environment keyframe. Use Medium/Low structural fidelity, Style-first transformation, [Expressive/Radical] abstraction, and [High/Mid/Low]-key exposure. Do not preserve scenic realism beneath painted texture.

Preserve only: [principal landform/structure, foreground-middle-distance relationship, dominant direction, protected geometry/color anchors, ratio if required]. Treat [tree/rock/window/wave/foliage/rubble/reflection counts and minor positions] as transformable; merge them into a few rhythm groups.

Environmental drama: make [hero form] [visual verb] against [counterform/current]. Reduce the frame to about five to nine interlocking macro masses. Make [primary macro departure] so [major area/contour/overlap/light/color relationship] changes at thumbnail scale; reinforce it with [supporting move] [plus a second primary-level departure for Radical]. Permit controlled restaging of [crop/horizon/overlap/spacing/local perspective] without breaking the preserved anchors. Make [focal event] the first read through [two cues] and keep [quiet field] intentionally broad.

Value/light/contrast: [three value groups] and [motivated light geometry]. Exposure remains [selected key]; do not use darkness as a style shortcut. Tier 1 [hero/focal event] owns [selected peak dimensions], Tier 2 [counterform] keeps [medium cues], and Tier 3 [context] compresses [local contrast/microcontrast/edge density/hue noise/texture frequency] into [chromatic-gray/scene-owned quiet family] while retaining [depth/material]. Color authorship: use [mode] because [source diagnosis], [primary contrast strategy], and spatially owned [dominant field/structural counter/focal apex/optional connector or neutral bridge]; color collision is [None/Preserve/Author with owners and boundary]; preserve [protected color anchors]. Do not add warm-cool or complementary opposition unless it improves the scene.

Material design: [material A] uses [large-shape/edge/mark grammar], [B] uses [different grammar], and [C] uses [different grammar]. Add [restrained broken contour/dry-brush vector/flat shadow seam] over spatial depth.

Avoid conventional scenic realism, source/result blur maps with the same major area ratios, generic matte-painting polish, literal repeated asset counts, photographic underpainting, global brush or color filters, identical marks across materials, uniform volumetric or gray fog, forced color-wheel formulas, franchise motifs, and invented text or subjects.
```

State concrete deformations and a thumbnail difference target; words such as “dramatic,” “stylized,” “abstract,” or “painterly” alone do not satisfy the environment contract.

## Semantic-source or Analyze + Generate

Compile in two stages:

1. State extracted semantic minimum and visual grammar without names, copied text, or exact objects/layout.
2. Generate a new subject, action, camera, environment, prop set, and exact palette. Keep only the abstract relationships and fixed system.

## Prompt-only

Return the compiled prompt plus an input-role map when images are expected. End with: `No image was generated or visually verified.`

## Reference Analysis Output

Return:

1. Observed evidence per reference
2. Inferred narrative/emotional intent
3. Fixed system with confidence
4. Variable system
5. Sample residue/no-copy list
6. One reusable operational prompt

Do not invoke an image tool unless the user also asks for a result.

## Tool Execution

- Use the runtime's real image generation/editing mechanism; attach every Edit Target and Support Insert through tool parameters, not prose alone.
- Use the requested ratio when supported. If a backend supports only nearby sizes, preserve composition intent and disclose the actual output.
- Default to one result. Generate a batch only when requested.
- After tool output, inspect the actual image before describing it as successful.

## Compact Dark-frame Example

This example uses a scene-motivated warm/cool relationship; it demonstrates prompt syntax, not a default palette. Analogous, value-led, saturation-led, and near-monochrome solutions are equally valid when justified by the color audit.

```text
Create one original 16:9 painterly-animation keyframe of a lone maintenance diver bracing a failing pressure door in an abandoned underwater transit hub. A pale circular window behind the diver forms the central focal island; near-black pipes and a cropped foreground valve create an asymmetrical aperture. Three value masses: deep blue-green structure over most of the frame, muted rust machinery as support, and a small cold-white window/helmet apex. The window is the motivated key light; a tiny amber warning lamp is the only warm accent. Grounded stylized anatomy, faceted painted planes, spatial depth, broad shadow masses, sharpest edges at the eyes, gripping hands, and door seam, lost edges in drifting silt. Flat graphic pressure fractures radiate from one seam with a tight core and almost no particles. Avoid franchise motifs, generic neon, glossy skin, uniform rim light, excessive sparks, and muddy blacks.
```
