---
name: painterly-frame-skill
description: Create or edit original painterly frames with initial-version composition and colour control, connected brushwork, mandatory facial verification and capacity-adaptive character detail. Use this skill whenever a photo or prompt should become a strongly stylized hand-painted frame, when another image model produces pasted colour blocks, cutout subjects, flat cel bands, global texture, malformed facial features or materially generic people, or when a finished painterly frame needs source-aware composition, authored colour, shared light, face geometry and material-specific QA. Preserve a strong source distribution by default; open expressive restaging only when the user or source diagnosis permits it. Do not use for faithful photo correction, pixel-locked preservation, or copying a named work, character, logo or exact frame.
---

# Painterly Frame Skill

Translate shorthand such as “hand-painted animated film” or “painterly remake” into an original, observable visual system. The universal contract has two layers: first lock the picture's composition, value and colour authorship; then make the locked design read as one connected painted field across different image models.

Treat any demonstrated photo or failed output as a regression case, not a content template. Generalize the failure class across portraits, environments, architecture, products, creatures and action scenes; keep subject-specific materials and compositions conditional.

## Route the Request

Choose the smallest route that satisfies the request.

- **Generate:** Create one finished keyframe from text or semantic-source images.
- **Edit Target:** Repaint a supplied image while preserving declared identity, object and spatial invariants.
- **Reference Analysis:** Extract evidence, fixed rules, variables and sample residue. Do not generate unless asked.
- **Prompt-only:** Return one executable prompt. Do not generate or claim visual inspection.
- **Analyze + Generate:** Analyze references, discard sample residue and create a different subject/composition.

Default to one finished borderless image when the user asks to make an image and gives enough direction. Do not run an intake questionnaire when the answer can be safely inferred.

## Load Only Relevant References

- For every Generate, Edit Target or Prompt-only task, read [references/composition-color-lock.md](references/composition-color-lock.md), [references/style-system.md](references/style-system.md) and [references/prompt-compiler.md](references/prompt-compiler.md).
- For every Generate, Edit Target, Prompt-only or finished-frame review task, read [references/model-consistency.md](references/model-consistency.md) and [references/painterly-continuity.md](references/painterly-continuity.md). The former defines portable invariants; the latter defines connected brush fields and weak-model adapters.
- For every Generate, Edit Target, Prompt-only or finished-frame review task, read [references/directorial-contrast.md](references/directorial-contrast.md) for permitted macro departures and [references/color-authorship.md](references/color-authorship.md) for scene-owned colour decisions.
- When any image is supplied, also read [references/source-analysis.md](references/source-analysis.md).
- When a human face is visible, also read [references/facial-control.md](references/facial-control.md) and build the facial packet before compiling the final prompt. This is required for portraits, figures, groups and any cropped face that carries identity or expression.
- When any human figure is visible, also read [references/character-detail-adaptation.md](references/character-detail-adaptation.md). Use a balanced first-pass detail packet, then adapt only from inspected output behaviour; never infer capability from a model brand.
- When the environment carries the focal event or the user permits expressive scene distortion, also read [references/environment-abstraction.md](references/environment-abstraction.md).
- For multiple directions or a series, read [references/variation-engine.md](references/variation-engine.md).
- After generation/editing, or when reviewing a result, read [references/quality-gate.md](references/quality-gate.md).
- Read [references/research-basis.md](references/research-basis.md) only when the user asks how the system was derived, wants an audit or supplies new style references to reconcile.

## Source and Reference Boundaries

Assign every supplied image exactly one primary role: pixel-locked region, edit target, support insert, semantic source or style reference. Record identity/topology fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, composition mode and colour-authorship mode separately.

- Preserve declared identity, count, action, gaze, adjacency, depth order, required text, protected local colours and explicit camera/landmark relations.
- When a face is visible and identity or expression matters, preserve the head axis, eye-line, gaze, expression cues and relative feature spacing. Simplifying skin texture or lashes never authorizes slanted eyes, an over-wide eye gap, crossed gaze or an off-axis nose/mouth.
- When a person is visible, preserve material-defining evidence for skin, hair, clothing, shoes, hands and contact points at a detail level appropriate to their scale. More detail means clearer form, material and connection—not pores, every thread, every hair strand or global sharpening.
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
8. Capacity-adaptive character detail: facial verification, skin/clothing/shoe sufficiency and restraint against excess microtexture
9. Optional graphic 2D marks, FX and decoration

## Workflow

1. Inspect every target/reference image with the available image viewer. If a required image is unavailable, ask for it instead of guessing.
2. Build the Source Card from [references/source-analysis.md](references/source-analysis.md); separate observed facts from inferences.
3. Write the Composition Lock and Colour Lock from [references/composition-color-lock.md](references/composition-color-lock.md). Decide `Preserve-and-enrich` or `Directed-restage` before choosing a composition family, macro departure or palette change.
4. Distill recognition anchors and the directorial proposition. For Directed-restage only, declare one primary macro departure, one supporting move and a thumbnail difference target from [references/directorial-contrast.md](references/directorial-contrast.md). For environment emphasis, define one hero form, one counterform/current and a five-to-nine-mass budget.
5. Build the portable render contract from [references/model-consistency.md](references/model-consistency.md): canvas/anchors; composition lock; five-to-nine masses; three value groups; spatial colour roles; focal/support/context contrast tiers; shape/plane map; material grammars; edge hierarchy; continuity packet; and anti-filter conditions. When a face is present, add the facial packet and anatomy guard from [references/facial-control.md](references/facial-control.md). When a person is present, add the balanced character-detail packet from [references/character-detail-adaptation.md](references/character-detail-adaptation.md); keep facial construction first and microtexture restrained.
6. Compile a short priority-ordered prompt with [references/prompt-compiler.md](references/prompt-compiler.md). Put composition/color lock first, continuity second and only the shortest observed adapter last. Never stack every adapter.
7. Use the runtime's real image generation/editing tool once. Pass target images through its actual reference-image mechanism.
8. Inspect the returned image beside the source at thumbnail/blur, mid and close scale. Apply [references/quality-gate.md](references/quality-gate.md) and the model-consistency/continuity tests. When a face is present, the close-scale facial gate in [references/facial-control.md](references/facial-control.md) is mandatory: any failure requires correction and reinspection before pass. When a person is present, classify the observed detail behaviour as Collapsed, Adequate or High-capacity/already-dense with [references/character-detail-adaptation.md](references/character-detail-adaptation.md); judge the output, never the model label.
9. If one module fails, make at most one targeted correction. For collapsed character detail, keep composition, colour, pose and environment masses fixed while selectively restoring facial construction, quiet skin turns, clothing weight/fold origins, shoe construction/contact and important hand/prop contact. If facial geometry also fails, combine both into one focal-character correction. Adequate or high-capacity results receive no extra microtexture. Reinspect afterward; a remaining face or character-material failure is reported, not passed.
10. Return the actual image/path plus a concise fidelity or limitation note. Never claim generation, inspection or validation that did not occur.

Prompt-only and Reference Analysis routes stop before tool execution and clearly state that no image was generated or verified.

## Output Contract

- **Generate/Edit Target:** requested number of finished images; default one. Include the actual result and mention only material preservation limits or an unresolved quality issue.
- **Reference Analysis:** observed evidence, inferred intent, fixed system, variable system, sample residue and one reusable operational prompt.
- **Prompt-only:** one tool-ready prompt and any required input-role map; state that no image was generated or checked.
- **Failure:** identify the failed contract precisely. A remaining facial or focal-character material failure after the one targeted correction must be disclosed; do not present it or any uninspected draft as a pass.
