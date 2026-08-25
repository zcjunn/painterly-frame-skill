# Painterly Frame Skill — v1.0.2

This release keeps the composition/colour lock and connected-painterly continuity contract, makes facial verification and correction mandatory, and adds output-observed adaptive character detail.

The preceding `v1.0.1` state is preserved by both its release tag and `backup-v1.0.1`.

## Included

- Restores the initial-version composition, exposure and scene-owned colour priorities from public baseline `7df746f`.
- Keeps Preserve-and-enrich as the default Edit Target route; Directed-restage requires an explicit user request or a documented source imbalance.
- Adds portable continuity rules for connected light, boundary relationships, structural stroke currents and material-specific marks, with one behaviour adapter at most.
- Requires actual post-generation facial inspection: head axis, eye-line, gaze, expression, perspective-aware eye spacing and nose/mouth/chin alignment must pass; a failed face receives one targeted correction and reinspection before pass.
- Adds `references/character-detail-adaptation.md` for visible people: balanced first-pass face, skin, hair, clothing, shoe, hand and contact detail without maximum microtexture.
- Diagnoses capacity from the inspected output rather than the model name: Collapsed-detail output receives one selective focal-character restoration, Adequate output is unchanged, and already-dense output is restrained instead of sharpened further.
- Adds regression cases for weak-environment/person material collapse and for over-rendering an already capable result.
- Uses `$painterly-frame-skill` consistently in the frontmatter, UI metadata, examples, evals and package.
- Keeps the personal non-commercial license and the source/reference boundary unchanged.

## Deliberately not guaranteed

- Identical pixels, seeds, brush stamps or facial microgeometry across different models.
- Correction of intentional asymmetry caused by pose, perspective, winks, squints or an explicitly stylized expression.
- Continued retries after one targeted focal-character correction fails; remaining facial or material limitations must be reported outside the supported consistency envelope.
