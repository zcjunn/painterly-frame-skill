---
name: painterly-frame
description: Create or edit exactly one original painterly frame with composition, colour, connected brushwork, shared light, face geometry and material-specific control. For supplied photos, inherit the exact pixel aspect ratio and preserve a strong source distribution unless expressive restaging is authorized. Use when a photo or prompt should become one hand-painted frame, or when a result has pasted blocks, cutout subjects, flat cel bands, global texture or malformed faces. Prefer gpt-5.6 Luna-极高 when available. Do not use as the page, panel-count, camera, pose or layout controller for photo-derived comic pages, 漫画组图, storyboards, sequences or requests for three or more panels; route those to photo-to-comic and contribute rendering methods only. Do not use for faithful photo correction, pixel-locked preservation or copying a named work, character, logo or exact frame.
---

# Painterly Frame

Translate shorthand such as “hand-painted animated film” or “painterly remake” into an original, observable visual system. The universal contract has two layers: first lock the picture's composition, value and colour authorship; then make the locked design read as one connected painted field across different image models. For photo inputs, the source pixel aspect ratio is a first-class composition invariant, not a generic 3:2, 2:3 or 16:9 suggestion.

Treat any demonstrated photo or failed output as a regression case, not a content template. Generalize the failure class across portraits, environments, architecture, products, creatures and action scenes; keep subject-specific materials and compositions conditional.

## Recommended Model

When the runtime allows model selection, prefer `gpt-5.6 Luna-极高` for this skill. The model's capability directly affects the image-generation result and the fidelity of composition, connected brushwork, material rendering, facial geometry and fine detail; weaker or different models may produce visibly different results even when given the same contract.

如果运行环境支持选择模型，优先推荐 `gpt-5.6 Luna-极高`。模型本身的性能会直接影响画面的生成效果与细节表现，也会影响构图执行、连续笔触、材质、人物五官和空间层次；即使使用同一份视觉合同，不同或较弱的模型仍可能产生明显差异。

## Route the Request

Choose the smallest route that satisfies the request.

- **Generate:** Create one finished keyframe from text or semantic-source images.
- **Edit Target:** Repaint a supplied image while preserving declared identity, object and spatial invariants.
- **Reference Analysis:** Extract evidence, fixed rules, variables and sample residue. Do not generate unless asked.
- **Prompt-only:** Return one executable prompt. Do not generate or claim visual inspection.
- **Analyze + Generate:** Analyze references, discard sample residue and create a different subject/composition.

### Collaboration boundary with `photo-to-comic`

When a request asks for a photo-derived comic page, 漫画组图, 分镜, sequence, storyboard, or at least three panels, `photo-to-comic` owns the outer `2:3` page, panel count, panel geometry, shot scales, camera positions, actions, poses, gaze, expressions, and narrative order. In that combined route, this skill contributes only transferable rendering methods: colour/value roles, shape and faceted-plane authorship, connected brush fields, shared boundary illumination, material-local marks, edge/contrast hierarchy, character/environment finish matching, and face-identity proportions.

Do not activate this skill's source-ratio inheritance, `Preserve-and-enrich` composition lock, single-frame camera/crop/headroom/horizon/quiet-space/subject-scale lock, pose/gaze/expression lock, single focal-event rule, or single-frame Output Contract inside a comic sequence. The source photograph becomes semantic scene/story evidence rather than this skill's Edit Target. The final result must remain one comic page with at least three visibly divided panels, never one painterly hero frame.

Default to one finished borderless image when the user asks to make an image and gives enough direction. Do not run an intake questionnaire when the answer can be safely inferred.

## Load Only Relevant References

- For every Generate, Edit Target or Prompt-only task, read [references/composition-color-lock.md](references/composition-color-lock.md), [references/style-system.md](references/style-system.md) and [references/prompt-compiler.md](references/prompt-compiler.md).
- For every Generate, Edit Target, Prompt-only or finished-frame review task, read [references/model-consistency.md](references/model-consistency.md) and [references/painterly-continuity.md](references/painterly-continuity.md). The former defines portable invariants; the latter defines connected brush fields and weak-model adapters.
- For every Generate, Edit Target, Prompt-only or finished-frame review task, read [references/directorial-contrast.md](references/directorial-contrast.md) for permitted macro departures and [references/color-authorship.md](references/color-authorship.md) for scene-owned colour decisions.
- When any image is supplied, also read [references/source-analysis.md](references/source-analysis.md).
- When a human face is visible, also read [references/facial-control.md](references/facial-control.md) and build the facial packet before compiling the final prompt. This is required for portraits, figures, groups and any cropped face that carries identity or expression.
- When the environment carries the focal event or the user permits expressive scene distortion, also read [references/environment-abstraction.md](references/environment-abstraction.md).
- For multiple directions or a series, read [references/variation-engine.md](references/variation-engine.md).
- After generation/editing, or when reviewing a result, read [references/quality-gate.md](references/quality-gate.md).
- Read [references/research-basis.md](references/research-basis.md) only when the user asks how the system was derived, wants an audit or supplies new style references to reconcile.

## Source and Reference Boundaries

Assign every supplied image exactly one primary role: pixel-locked region, edit target, support insert, semantic source or style reference. Record identity/topology fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, composition mode and colour-authorship mode separately.

- Preserve declared identity, count, action, gaze, adjacency, depth order, required text, protected local colours and explicit camera/landmark relations.
- Measure each supplied image's actual pixel width and height (not a resized chat preview). If the user has not explicitly requested a different canvas, inherit that exact source aspect ratio for the output. Never silently substitute a stock ratio such as 3:2, 2:3, 16:9 or square; when multiple images are processed independently, derive the ratio separately for each target.
- If the runtime only offers preset canvases, choose the closest supported ratio without stretching, padding or unintended crop, and disclose the actual output ratio.
- When a face is visible and identity or expression matters, preserve the head axis, eye-line, gaze, expression cues and relative feature spacing. Simplifying skin texture or lashes never authorizes slanted eyes, an over-wide eye gap, crossed gaze or an off-axis nose/mouth.
- For an Edit Target, use `Preserve-and-enrich` by default when the source already has effective headroom, negative space, focal scale, horizon, diagonal/current or colour-area hierarchy. Do not tighten the crop, enlarge the subject or lower a bright exposure merely to prove stylization.
- Use `Directed-restage` only when the user explicitly authorizes Style-first/Expressive/Radical change or the Source Card identifies a real compositional imbalance. Declare one primary macro departure, one supporting move and the anchors that remain fixed.
- Audit source colour before naming hues. Preserve-and-refine is the default; Rebalance or Re-script only for a stated hierarchy problem or user permission. Warm-cool, complementary, teal-orange and dark exposure are optional, never automatic.
- Do not promise machine-identical pixels from generative editing. Use deterministic compositing when exact pixels are required, or disclose the limitation.
- Do not leave reference characters, text, branding, exact props, locations or camera layouts in the final prompt; learn only abstract visual relationships.

## Decision Priority

1. User contract, safety and image-role boundaries
2. Semantic minimum, recognition/topology invariants and facial geometry when a face is present
3. Composition lock: ratio, crop/headroom, focal scale, quiet space, horizon, viewing path and restage permission
4. Colour lock: exposure key, three value groups, spatial colour roles, protected local colours and one primary contrast axis
5. Selected transformation, dramatic proposition and one dominant focal read
6. Permitted macro departure, supporting move and area/overlap/light/colour topology
7. Painterly continuity: internal colour turns, boundary binding, shared illumination, material marks and edge hierarchy
8. Optional graphic 2D marks, FX and decoration

## Workflow

1. Inspect every target/reference image with the available image viewer and record its actual pixel dimensions and source-derived ratio. If a required image is unavailable, ask for it instead of guessing.
2. Build the Source Card from [references/source-analysis.md](references/source-analysis.md); separate observed facts from inferences.
3. Write the Composition Lock and Colour Lock from [references/composition-color-lock.md](references/composition-color-lock.md), carrying the measured source ratio into the Canvas line unless the user explicitly overrides it. Decide `Preserve-and-enrich` or `Directed-restage` before choosing a composition family, macro departure or palette change.
4. Distill recognition anchors and the directorial proposition. For Directed-restage only, declare one primary macro departure, one supporting move and a thumbnail difference target from [references/directorial-contrast.md](references/directorial-contrast.md). For environment emphasis, define one hero form, one counterform/current and a five-to-nine-mass budget.
5. Build the portable render contract from [references/model-consistency.md](references/model-consistency.md): source-derived canvas/anchors; composition lock; five-to-nine masses; three value groups; spatial colour roles; focal/support/context contrast tiers; shape/plane map; material grammars; edge hierarchy; continuity packet; and anti-filter conditions. When a face is present, add the facial packet and the facial anatomy guard from [references/facial-control.md](references/facial-control.md) without changing the composition or colour lock.
6. Compile a short priority-ordered prompt with [references/prompt-compiler.md](references/prompt-compiler.md). Put composition/color lock first, continuity second and only the shortest observed adapter last. Never stack every adapter.
7. Use the runtime's real image generation/editing tool once. Pass target images through its actual reference-image mechanism and request the measured source ratio; do not rely on the runtime's default canvas.
8. Inspect the returned image beside the source at thumbnail/blur, mid and close scale. Apply [references/quality-gate.md](references/quality-gate.md) and the model-consistency/continuity tests. When a face is present, run the close-scale facial gate in [references/facial-control.md](references/facial-control.md). A result fails when the lock is lost, the image is a collection of attractive blocks, the source remains under a global paint filter, or a face has accidental feature drift.
9. If one module fails, make at most one targeted correction. A facial-anatomy adapter or other adapter may fix only its named rendering shortcut; it may not change the composition lock, colour lock or exposure. If the facial module fails, use the facial guard once and then report the runtime outside the supported envelope if it still fails.
10. Return the actual image/path plus a concise fidelity or limitation note. Never claim generation, inspection or validation that did not occur.

Prompt-only and Reference Analysis routes stop before tool execution and clearly state that no image was generated or verified.

## Output Contract

- **Generate/Edit Target:** requested number of finished images; default one. For each supplied photo, the finished canvas must inherit the measured source aspect ratio unless the user explicitly overrides it. Include the actual result and mention only material preservation limits or an unresolved quality issue.
- **Reference Analysis:** observed evidence, inferred intent, fixed system, variable system, sample residue and one reusable operational prompt.
- **Prompt-only:** one tool-ready prompt and any required input-role map; state that no image was generated or checked.
- **Failure:** identify the failed contract precisely. Do not present an uninspected draft as a pass.

For any photo-derived comic-page or storyboard request, defer the entire output contract to `photo-to-comic`; this skill has no authority to collapse the result to one frame or restore the source ratio/composition/pose.
