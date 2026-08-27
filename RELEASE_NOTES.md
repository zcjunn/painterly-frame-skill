# Painterly Frame — v1.0.3

This release makes `painterly-frame` the canonical repository and public name, and documents the recommended runtime for the best image-generation quality.

## Included

- Renames the GitHub repository from `painterly-frame-skill` to `painterly-frame`.
- Removes “Skill” from the public product name and the personal non-commercial license title.
- Recommends `gpt-5.6 Luna-极高` when model selection is available.
- Clarifies that model performance directly affects overall image generation quality and fine detail.

---

# Painterly Frame — v1.0.2

This release makes the source photo's original pixel aspect ratio a first-class composition invariant and restores the concise public skill identifier `painterly-frame`.

## Included

- Inherits each supplied photo's exact width:height ratio by default, measured from the original file rather than a resized preview.
- Prevents silent fallback to stock 3:2, 2:3, 16:9 or square canvases; preset-only runtimes must choose the closest ratio without stretch, padding or unintended crop and disclose it.
- Applies the ratio rule consistently to source analysis, composition/color lock, portable cross-model contract, continuity guidance, prompt compilation, eval metadata and UI invocation.
- Renames the public skill identifier, explicit invocation and UI display name to `painterly-frame`.
- Keeps the v1.0.1 initial composition/color priorities, connected brushwork contract, facial controls and personal non-commercial license unchanged.

## Deliberately not guaranteed

- Exact output dimensions when a runtime exposes only fixed presets; the selected preset and any resulting ratio difference must be reported.
- Identical pixels, seeds, brush stamps or facial microgeometry across different models.
- A user-requested alternate canvas: an explicit user override still takes precedence over source-ratio inheritance.

---

# Painterly Frame Skill — v1.0.1

This patch release keeps the universal composition/colour lock and connected-painterly continuity contract while restoring the public skill identifier to `painterly-frame-skill`.

## Included

- Restores the initial-version composition, exposure and scene-owned colour priorities from public baseline `7df746f`.
- Keeps Preserve-and-enrich as the default Edit Target route; Directed-restage requires an explicit user request or a documented source imbalance.
- Adds portable continuity rules for connected light, boundary relationships, structural stroke currents and material-specific marks, with one behaviour adapter at most.
- Adds a conditional facial-control contract for human faces: head axis, eye-line, gaze, expression, perspective-aware eye spacing, nose/mouth/chin alignment, and a close-scale anatomy gate.
- Adds a facial-geometry regression case for accidental slanted eyes, over-wide eye spacing and mismatched gaze.
- Uses `$painterly-frame-skill` consistently in the frontmatter, UI metadata, examples, evals and package.
- Keeps the personal non-commercial license and the source/reference boundary unchanged.

## Deliberately not guaranteed

- Identical pixels, seeds, brush stamps or facial microgeometry across different models.
- Correction of intentional asymmetry caused by pose, perspective, winks, squints or an explicitly stylized expression.
- Continued retries after one targeted facial-anatomy correction fails; the runtime should then be reported as outside the supported consistency envelope.
