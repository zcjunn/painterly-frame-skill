---
name: cinematic-painterly-remake
description: Create or edit original cinematic painterly-animation keyframes with thumbnail-visible directorial restaging, scene-owned colour authorship, focal-versus-context contrast ownership, high/mid/low-key exposure, reconstructed or expressively exaggerated graphic shapes, faceted planes, spatial depth, and selective 2D marks. Use when a photo or prompt should become a strongly stylized animated-film frame, abstract scene reconstruction, or finished-frame review. Do not use for faithful photo correction, pixel-locked preservation, or copying a named work, character, logo, or exact frame.
---

# Cinematic Painterly Remake

Translate shorthand such as “hand-painted animated film” or “dark graphic cartoon mood” into an original, observable visual system. Optimize the finished frame, not resemblance to a protected sample.

Treat any demonstrated photo or failed output as a regression case, not a content template. Generalize the failure class across portraits, environments, architecture, products, creatures, and action scenes; keep subject-specific materials and compositions conditional.

## Route the Request

Choose the smallest route that satisfies the request.

- **Generate:** Create a new finished keyframe from text or semantic-source images.
- **Edit Target:** Restage or repaint a user image while preserving declared identity, object, or spatial invariants.
- **Reference Analysis:** Extract evidence, fixed rules, variables, and sample residue. Do not generate unless asked.
- **Prompt-only:** Return an executable prompt. Do not generate or claim visual inspection.
- **Analyze + Generate:** Analyze references, discard sample residue, then create a different subject and composition.

Default to one finished borderless image when the user asks to make an image and gives enough direction. Do not run an intake questionnaire when the answer can be safely inferred.

## Load Only Relevant References

- For every Generate, Edit Target, or Prompt-only task, read [references/style-system.md](references/style-system.md) and [references/prompt-compiler.md](references/prompt-compiler.md).
- For every Generate, Edit Target, Prompt-only, or finished-frame review task, read [references/directorial-contrast.md](references/directorial-contrast.md). This is the macro-departure and contrast-ownership contract.
- For every generation, edit, prompt-only, reference-analysis, or finished-frame review task, read [references/color-authorship.md](references/color-authorship.md). Color balance is required; warm-cool contrast is optional.
- When any image is supplied, also read [references/source-analysis.md](references/source-analysis.md).
- When the environment carries the focal event, no character/object anchor is present, or the user permits expressive scene distortion, also read [references/environment-abstraction.md](references/environment-abstraction.md).
- For multiple directions or a series, read [references/variation-engine.md](references/variation-engine.md).
- After generation/editing, or when reviewing a result, read [references/quality-gate.md](references/quality-gate.md).
- Read [references/research-basis.md](references/research-basis.md) only when the user asks how the system was derived, wants an audit, or supplies new style references to reconcile.

## Source and Reference Boundaries

Assign each supplied image exactly one primary role before prompting: pixel-locked region, edit target, support insert, semantic source, or style reference. Record identity/structure fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode separately. Never infer that stronger style means darker exposure, that recognizable identity requires photographic literalness, that an empty environment should remain a conventional realistic landscape, or that this visual family requires a fixed warm-cool/complementary palette.

- Do not promise machine-identical pixels from generative editing. Use deterministic compositing when exact pixels are required, or disclose the limitation.
- Preserve only the declared recognition-critical invariants before style. Nonessential folds, hardware, foliage, texture, atmospheric detail, and repeated props may be merged, exaggerated, or redesigned when the selected transformation mode allows it.
- In Style-first/Expressive work, preserve a short anchor set and deliberately transform the remaining scene through one primary macro departure plus one supporting move. The primary move must alter a major area, contour, overlap, focal scale, negative space, light shape, or color-zone relationship at 128–256 px; axis count and surface texture alone do not qualify.
- Treat source fidelity and source distribution separately. Preserve declared identity, count, action, protected geometry, text, and recognition colors; do not automatically preserve documentary headroom, crop, horizon, incidental asset positions, or local contrast distribution.
- Assign contrast ownership across focal, supporting, and context tiers. Non-focal regions may become quieter chromatic-gray fields through lower local contrast, microcontrast, edge density, hue noise, and texture frequency, but must retain broad depth, material, and motivated color.
- From style references, learn attention geometry, value topology, color function, material treatment, edge rhythm, and FX behavior. Exclude characters, text, branding, exact props, runes, locations, and camera layouts.
- Treat named-style shorthand as a discovery phrase. Compile it into visible decisions; do not leave a protected work's name as the main style instruction in the final image prompt.

## Decision Priority

1. User contract, safety, and image-role boundaries
2. Semantic minimum and declared identity/structure invariants
3. Selected transformation/abstraction mode, dramatic proposition, and one dominant focal read
4. Primary macro departure, supporting move, area/overlap/light/color topology, and viewing path
5. Scene-owned exposure, contrast ownership, deliberate color authorship, and motivated light
6. Material-specific planes, edge hierarchy, and graphic 2D marks/FX
7. Optional decoration and variant preferences

## Workflow

1. Inspect every target/reference image with the available image viewer. If a required image is unavailable, ask for it instead of guessing.
2. Build the Source Card from [references/source-analysis.md](references/source-analysis.md); separate `observed` from `inferred`, then choose identity fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode independently.
3. Distill recognition anchors from transformable detail. Write the dramatic proposition, primary macro departure, supporting move, contrast-ownership map, optional color-collision decision, and thumbnail difference target from [references/directorial-contrast.md](references/directorial-contrast.md). Rebuild silhouette, internal planes, and large environment shapes before specifying brush texture. For environment-emphasis, define one hero form, one counterform/current, a macro-shape budget, and source-owned transform decisions from [references/environment-abstraction.md](references/environment-abstraction.md). Audit the source palette and build a role-based color plan from [references/color-authorship.md](references/color-authorship.md); choose one primary contrast axis and at most one subordinate axis rather than forcing warm-cool. Select one composition family, value plan, light hierarchy, and a different mark grammar for each important material.
4. Compile a short priority-ordered prompt using [references/prompt-compiler.md](references/prompt-compiler.md). Explicitly reject photographic underpainting with a global paint filter when the user wants strong stylization.
5. Use the runtime's image generation/editing tool once. Pass target images through the tool's actual reference-image mechanism.
6. Inspect the returned image beside the source at 128–256 px, blurred/thumbnail scale, mid scale, and close scale. Apply [references/quality-gate.md](references/quality-gate.md). For Style-first/Expressive edits, fail the result when the macro/colour-block map remains essentially interchangeable with the source even if close-up brushwork is attractive.
7. If a specific module fails, make at most one targeted correction. Do not regenerate blindly or change unrelated modules.
8. Return the actual image or path plus a concise fidelity/limitation note. Never claim generation, inspection, or validation that did not occur.

Prompt-only and Reference Analysis routes stop before tool execution and clearly say no image was generated or verified.

## Output Contract

- **Generate/Edit Target:** requested number of finished images; default one. Include the actual result and mention only material preservation limits or an unresolved quality issue.
- **Reference Analysis:** observed evidence, inferred intent, fixed system, variable system, sample residue, and a reusable operational prompt.
- **Prompt-only:** one tool-ready prompt and any required input-role mapping; state that no image was generated or checked.
- **Failure:** identify the failed contract precisely. Do not present a draft or uninspected output as a pass.
