# Prompt Compiler

Compile research and Source Cards into visible pixel decisions. Keep the final prompt shorter than the analysis.

## Compiler Order

1. **Canvas:** output count, exact source-derived pixel aspect ratio (or an explicit user override), orientation, finished borderless image, shot scale.
2. **Source contract:** image role, semantic minimum, recognition anchors, transformable elements, identity fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, color-authorship mode, and allowed changes.
3. **Composition lock:** ratio, crop/headroom, focal scale, quiet-area share, horizon, major diagonal/current, viewing path, topology anchors, and whether distribution is Preserve-and-enrich or Directed-restage.
4. **Colour lock:** exposure key; source strengths/problems; Preserve-and-refine, Rebalance, or Re-script; three value groups; spatial colour roles; protected local colours; one primary contrast axis; optional collision with owners and function.
5. **Directorial proposition:** actor, visible pressure/counterforce, intended first read, and—only for Directed-restage—one primary macro departure, one supporting move and a thumbnail difference target from `directorial-contrast.md`.
6. **Focal actor and transformation:** one readable verb/relationship; for environment-emphasis, name the hero form, counterform/current, merged repeated detail and the permitted area/contour/overlap/light/color impact.
7. **Attention geometry:** composition family, central attention zone, perspective and viewing path as constrained by the composition lock.
8. **Continuity and surface:** internal colour turns, boundary relationships, shared light and interlocking strokes first; then material-specific marks, edge/detail hierarchy, spatial depth and limited graphic 2D intervention.
9. **Facial control when a face is visible:** read [facial-control.md](facial-control.md) and add the facial packet, perspective-aware eye-line and gaze guard, feature-spacing guard, expression cues and close-scale rejection conditions. Keep it after source/composition lock and before general texture language.
10. **FX:** only if story-motivated; unique shape language and edge hierarchy.
11. **Avoids:** the shortest relevant list of likely model errors and sample residue; never let avoids override the lock.

Do not include a rule that cannot become a visible pixel, tool parameter, source-role mapping, or quality check. Keep generation prompts compact: lead with the six to ten highest-impact decisions, remove redundant adjectives, and avoid long inventories that dilute shape reconstruction.

## Portable Core Before Model Wording

Write one model-neutral render contract before adding optional phrasing for a particular runtime. Keep its decisions concrete enough to survive paraphrase:

```text
Portable render contract:
- Canvas and anchors: [count, exact source-derived ratio or explicit override, orientation, identity/topology invariants].
- Composition lock: [Preserve-and-enrich or Directed-restage; crop/headroom, focal scale, quiet-area share, horizon, viewing path, permitted change].
- Macro map: [five-to-nine named interlocking masses and their area/overlap relationship].
- Value and colour lock: [exposure key; three value groups; dominant field, structural counter, focal apex, neutral bridge; protected colours; primary contrast axis].
- Contrast ownership: [Tier 1 focal peaks; Tier 2 support cues; Tier 3 context reductions].
- Shape reconstruction: [silhouette breaks; four-to-seven meaningful focal planes; merged repeated detail].
- Material grammar: [material A plane scale/direction/edges/reflectance]; [B different]; [C different when present].
- Edge hierarchy: [hardest, medium, soft/lost owners].
- Facial packet when present: [head axis; eye-line/gaze; relative eye size and interval; brow/nose/mouth/chin axis; expression cues; face-to-hair/neck/hand overlaps].
- Painterly continuity: [internal colour turns; important boundary relations; shared key/shadow/reflected colour; structural stroke current].
- Anti-filter gate: [what must visibly differ from photographic underpainting at thumbnail, mid, and close scale].
```

Treat this block as required decisions, not prose to copy verbatim. Put recognition invariants and the primary macro departure near the beginning of the final prompt and repeat the shortest critical preservation/avoid clause at the end. Avoid sampler, seed, model-version, quality-tag, or house-style vocabulary in the portable core; those controls do not transfer reliably between model families. See [model-consistency.md](model-consistency.md).

## Base Generate Template

```text
Create exactly one original [exact source-derived ratio/orientation] painterly-animation keyframe, a finished borderless image. For a supplied photo, use its original pixel width:height; do not default to 3:2, 2:3, 16:9 or square unless the user explicitly asks.

Scene and verb: [original subject, environment, one readable action/relationship]. Keep the focal event perceptually dominant inside the middle attention zone through [isolation/value/chroma/edge/perspective], while [quiet/occluding region] occupies a substantial part of the frame. Use [one composition family] and a believable spatial camera with clear foreground, middle, and atmosphere.

Composition and colour lock: use [Preserve-and-enrich or Directed-restage]. Preserve [ratio/crop/headroom/focal scale/quiet-area share/horizon/viewing path/topology] unless the user explicitly allows [change]. Organize [dominant field], [supporting mass] and [small apex] under a [high/mid/low]-key light. Assign [dominant field], [structural counter], [focal apex] and [neutral bridge] to spatial owners; use [one primary contrast axis], preserve [local-colour anchors] and avoid any unowned global grade.

Directorial proposition: [actor] is [visible pressure/relationship] against [counterforce]; the first read is [event]. If the lock is Directed-restage, make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relationship] is unmistakable at thumbnail scale; reinforce it with [supporting move]. Preserve [declared anchors]. If the lock is Preserve-and-enrich, keep the distribution and direct the change into [light shape/colour adjacency/edge rhythm/viewing current].

Value, light, and contrast ownership: organize the frame into three large value groups: [dominant field], [supporting mass], and [small apex]. The primary light is [visible/motivated source with geometry]; reserve the brightest highlight and deepest dark for [focal path]. Tier 1 [focal owner] peaks in [two or three selected contrast dimensions]; Tier 2 [support] keeps medium structural cues; Tier 3 [context] becomes a unified [scene-owned colored/chromatic-gray] field through lower [local contrast/microcontrast/edge density/hue noise/texture frequency] while retaining [depth/material cues]. Use only a restrained subordinate [bounce/rim], controlled haze, and tight bloom.

Color authorship: use the locked [Preserve-and-refine/Rebalance/Re-script] decision because [source/story reason]. Use [primary contrast strategy] with [optional subordinate strategy]. Assign [dominant field: spatial owner, hue family, value, chroma], [structural counter: owner and separation job], [focal accent/apex: owner and attention job], and [optional connector/neutral bridge]. Color collision is [None/Preserve existing/Author new: owners, adjacency, dominant side, function]. These roles may share one hue family when value/chroma does the work. Preserve [protected local-color anchors]. Let motivated light influence rather than replace material color. Warm-cool is optional; avoid formulaic teal-orange, purple-neon, global gray fog, or equal saturated competition.

Continuity and rendering: after the lock, build each major mass from a broad base plus a few unequal internal light/material turns; connect important neighbours through [occlusion/contact/turning form/atmospheric merge/reflected-colour bridge]; carry one structural stroke current across the scene; use mixed hard/broken/soft/lost edges and shared key/shadow/reflected light. Differentiate skin, cloth, metal, wall, smoke, foliage and energy by plane size, direction and reflectance. If a face is visible, preserve [head axis, eye-line, gaze, expression and relative feature spacing] with a perspective-aware eye band, aligned nose/mouth axis and eyes/brows/smile as the sharpest local construction; avoid slanted eyes, over-wide eye spacing, crossed gaze, generic anime facial replacement and full head outlines. If FX are present, use [unique graphic shape language] with one sharp core, broad motion forms, sparse particles and no global glow.

Avoid: franchise characters, logos, runes, copied architecture or camera layouts; photoreal plastic skin; generic anime facial replacement; slanted or vertically drifting eyes; an over-wide eye gap; crossed gaze; off-axis nose or mouth; generic anime cel shading; uniform black outlines; all-over texture; excessive bloom, sparks, wet gloss, or crushed muddy blacks.
```

Replace brackets. Remove irrelevant clauses rather than leaving generic filler.

## Edit Target Templates

Lead with change plus preservation:

```text
Edit Image 1 into one finished [exact source-derived ratio] painterly-animation keyframe. Derive the ratio from the original input pixels and preserve it unless the user explicitly requests another canvas; do not use a stock preset by habit.

Preserve as recognition anchors: [identity, count, relationship, gesture, signature silhouette, protected geometry, wardrobe/object color anchors, required text]. Do not add or remove subjects.
Composition/color lock: use Preserve-and-enrich unless the user explicitly asks for restaging. Keep [ratio, crop/headroom, focal scale, quiet-area share, horizon, major diagonal/current and viewing path] and [high/mid/low]-key exposure. Audit the source palette; use [Preserve-and-refine/Rebalance/Re-script], [primary contrast axis], spatial [dominant/structural/focal/neutral] roles and protected [local-colour anchors].
Reconstruct: [transformable contours, repeated props, environment micro-detail, planes, material marks and light/colour turns]. If Directed-restage is authorized, make [one primary macro departure] and [one supporting move] without changing [protected anchors]. Otherwise enrich the locked distribution without enlarging or cropping the subject by default.

[Then add the continuity packet, attention geometry, three-group value plan, material-specific edge treatment and the shortest relevant failure adapter from the base template. If a human face is visible, insert the compact facial guard from [facial-control.md](facial-control.md) before general rendering and texture terms. Do not bury it after style adjectives or let a model-specific adapter rewrite it.]
```

Do not claim exact pixels. If pixels or typography must be exact, keep those regions outside the generative edit and composite deterministically.

For **Style-first** photo remakes, use this shorter contract:

```text
Rebuild Image 1 as one finished [ratio] painterly animation keyframe; do not put an oil-paint texture over photographic shading.

Keep only these recognition anchors: [subject identity/count, action or pose, signature color anchors, essential spatial relationship]. Permit [crop, controlled proportion and contour stylization, merged folds/hardware/foliage/props, redesigned atmosphere and environment shapes].

Directorial abstraction: [dramatic proposition]. Make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relation] visibly differs from the source at 128–256 px; reinforce it with [supporting move]. Do not preserve [incidental distribution].

Shape and contrast design: use [Restrained/Expressive/Radical] abstraction; [subject silhouette and 4–7 face/object planes]; [broad environment masses]; [material A mark grammar versus material B and C]. Exposure is [high/mid/low]-key because [scene reason], with [three value groups]. Assign Tier 1 [focal], Tier 2 [support], and Tier 3 [chromatic-gray/scene-owned context quieting plus retained depth/material cues]. Color authorship is [mode] because [source/story diagnosis]; use [primary contrast], spatially assign [dominant/structural/focal/neutral roles], decide [None/Preserve/Author] color collision, and preserve [color anchors]. Make [focal event] the first read through [two cues]. Add [one restrained natural or FX graphic intervention].

Avoid photographic underpainting, source/result thumbnail layouts that differ only in surface texture, global impasto/filter texture, identical marks across materials, literal micro-detail, generic anime outlines, plastic skin, franchise motifs, unnecessary darkness, passive source color, forced warm-cool, global gray fog, and global LUT color.
```

For a **Style-first environment-emphasis** remake, use this explicit abstraction contract instead of a generic landscape prompt:

```text
Rebuild Image 1 as one finished [ratio] painterly animation environment keyframe. Use Medium/Low structural fidelity, Style-first transformation, [Expressive/Radical] abstraction, and [High/Mid/Low]-key exposure. Do not preserve scenic realism beneath painted texture.

Preserve only: [principal landform/structure, foreground-middle-distance relationship, dominant direction, protected geometry/color anchors, exact source-derived ratio unless explicitly overridden]. Treat [tree/rock/window/wave/foliage/rubble/reflection counts and minor positions] as transformable; merge them into a few rhythm groups.

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
- For image-supplied tasks, use the measured source pixel ratio by default; only an explicit user override may change it. If a backend supports only nearby sizes, choose the closest supported ratio without stretch, padding or unintended crop, preserve composition intent, and disclose the actual output ratio.
- Default to one result. Generate a batch only when requested.
- After tool output, inspect the actual image before describing it as successful.

## Compact Dark-frame Example

This example uses a scene-motivated warm/cool relationship; it demonstrates prompt syntax, not a default palette. Analogous, value-led, saturation-led, and near-monochrome solutions are equally valid when justified by the color audit.

```text
Create one original 16:9 painterly-animation keyframe of a lone maintenance diver bracing a failing pressure door in an abandoned underwater transit hub. A pale circular window behind the diver forms the central focal island; near-black pipes and a cropped foreground valve create an asymmetrical aperture. Three value masses: deep blue-green structure over most of the frame, muted rust machinery as support, and a small cold-white window/helmet apex. The window is the motivated key light; a tiny amber warning lamp is the only warm accent. Grounded stylized anatomy, faceted painted planes, spatial depth, broad shadow masses, sharpest edges at the eyes, gripping hands, and door seam, lost edges in drifting silt. Flat graphic pressure fractures radiate from one seam with a tight core and almost no particles. Avoid franchise motifs, generic neon, glossy skin, uniform rim light, excessive sparks, and muddy blacks.
```
