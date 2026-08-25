# Facial Feature and Expression Control

Use this reference only when a human face is visible or when the subject's identity depends on facial features. It is a recognition and quality guard, not a demand for photorealistic skin or perfectly bilateral symmetry.

## Facial Packet

Before prompting, record the smallest facial packet that the source and user require:

- head tilt and head axis;
- eye-line direction and intended gaze;
- relative eye sizes and visible eyelid shape;
- inter-eye spacing relative to the face width;
- brow, nose bridge, mouth and chin positions on the head's perspective axis;
- expression-defining cues such as smile width, cheek lift, jaw opening or brow tension;
- face-to-hair, face-to-neck and face-to-hand occlusion.

For an edit target, preserve these relationships unless the user explicitly permits identity or expression changes. A painterly transformation may simplify pores, lashes, teeth and small skin texture, but it must not use simplification to erase feature spacing, gaze, expression or head orientation.

## Geometry Before Paint

Construct the face in this order:

1. establish the skull, jaw and neck silhouette;
2. lay one perspective-aware brow/eye band along the head axis;
3. place the nose bridge and nose plane on the same facial centerline;
4. place the mouth, chin and cheek turns in relation to the nose and jaw;
5. add hair, hands and clothing as overlapping forms that do not detach the face from the body.

Use the source perspective rather than a rigid frontal template. In a three-quarter or profile view, the far eye may be narrower and closer to the centerline, while the near eye carries more width; both eyes still follow one coherent head tilt and gaze. In a near-frontal view, start from a natural eye-to-eye interval of roughly one eye width, then adjust for perspective and expression. This is a guide, not a fixed measurement.

Avoid accidental divergence: one eye tilted or raised without a perspective cause, an inter-eye gap that is visibly too wide for the face, pupils aimed in different directions, a nose or mouth drifting off the face axis, or a smile that no longer matches the source expression. Do not “correct” an intentional wink, squint, asymmetrical pose or stylized expression when the source clearly contains it.

## Painterly Treatment

- Keep the eyes, brows, mouth and gripping/expressive hands in the focal edge tier; they need the clearest local construction, not a hard outline around the whole head.
- Use quiet, unequal skin planes caused by light direction, cheek/jaw turns and facial expression. Do not replace the face with smooth plastic gradients, generic anime eyes, or two-band cel shading.
- Let hair overlap the forehead, cheeks and neck with grouped ribbons; preserve contact shadows and reflected scene colour so the face belongs to the shared light field.
- Keep small highlights subordinate to the eye-line and expression. Avoid adding catchlights that change the gaze or make both eyes read as identical stickers.

## Prompt Block

When a face is present, append a compact facial guard after the source/composition lock and before general paint texture:

```text
Facial anatomy guard: preserve the source head tilt, eye-line, gaze, expression and feature spacing. Build the skull/jaw first, then one perspective-aware brow/eye band, nose bridge, mouth and chin on the same head axis. Keep the inter-eye interval natural for the face and view; in three-quarter view let the far eye narrow and move toward the centerline rather than forcing frontal symmetry. Align both pupils to the same intended gaze and let asymmetry come only from pose, perspective or an explicit expression. Keep eyes, brows, smile and expressive hands as the sharpest local construction while using quiet unequal skin planes, grouped hair ribbons and shared scene light. Avoid slanted or vertically drifting eyes, an over-wide eye gap, crossed gaze, off-axis nose/mouth, generic anime facial replacement, plastic skin, full head outlines or two-band cel shading.
```

## Close-Scale Gate

At close scale, fail the face module if any of these is true:

1. the eye-line contradicts the head tilt without a deliberate perspective or expression cause;
2. one eye is unintentionally higher, skewed or differently angled;
3. the inter-eye gap is visibly too wide or the eyes are mismatched in scale for the view;
4. pupils/irises do not share the intended gaze;
5. nose, mouth or chin drifts off the facial axis and changes the expression;
6. the face reads as a generic replacement or a pasted sticker rather than a form connected to hair, neck and shared light.

## Mandatory Verification and Correction

Preservation language is not evidence that the face succeeded. After every generated or edited result containing an inspectable face:

1. compare the actual face with the recorded facial packet at close scale;
2. mark each applicable gate item pass/fail;
3. if any facial item fails, do not return the result as a pass—make one targeted facial-anatomy correction;
4. reinspect the corrected result against the same packet before describing it as successful.

Keep the composition lock, colour lock, macro masses and painterly continuity packet unchanged during correction. When facial geometry and character material detail fail together, combine this guard with the focal-character restoration adapter in [character-detail-adaptation.md](character-detail-adaptation.md) as one targeted focal-character correction. If the runtime still fails after that correction, report facial geometry as outside the supported consistency envelope instead of adding unrelated style adjectives or silently accepting the face.
