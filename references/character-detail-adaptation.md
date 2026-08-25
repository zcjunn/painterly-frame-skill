# Adaptive Character Detail and Material Control

Use this reference whenever a human figure appears. It protects enough facial and material information for the person to feel complete while preventing the model from turning “more detail” into pores, fabric noise, oversharpening or a pasted high-resolution subject.

Judge capacity from the inspected output, not from the model name, version, price or reputation. Start with a restrained balanced character packet; strengthen it only after the first result shows a specific collapse.

## Character Detail Packet

Record only visible and identity-relevant evidence:

- **Face:** use the facial packet in [facial-control.md](facial-control.md); preserve geometry and expression before adding surface information.
- **Skin:** retain broad cheek, forehead, nose, jaw, arm and leg turns; local warm/cool variation; restrained reflected colour; and contact or cast shadows where skin meets hair or clothing.
- **Hair:** one dominant mass plus a few directional ribbons and broken silhouette clumps; individual strands only at the focal edge.
- **Clothing:** material weight, major fold origins, overlap, hem/collar/cuff structure and a few source-visible seams or fasteners. Show whether the material is knit, woven, denim, leather, rainwear or another visible class through plane scale and edge response rather than uniform texture.
- **Shoes:** readable upper/sole division, closure or lace logic when visible, material response and ground contact. Do not inventory every stitch or tread.
- **Hands and limbs:** readable joint direction, finger grouping at important gestures, and contact with props or ground. Do not sharpen every knuckle equally.

If the person is too small or occluded for a feature to be observed, do not invent microdetail. Preserve the silhouette, pose, colour anchors and the few readable material cues; disclose the resolution limit when identity-level inspection is impossible.

## Balanced First Pass

Use a moderate detail hierarchy on the first attempt:

1. face geometry and expression own the clearest local construction;
2. hands, prop contact and shoes receive secondary structural clarity;
3. clothing receives broad material/fold information plus a few selective seams;
4. skin receives quiet tonal and colour turns without pore-level texture;
5. environment keeps enough perspective, material and depth cues to prevent a sticker subject, but remains lower in microcontrast and mark frequency.

Do not ask for `ultra-detailed`, `8k skin`, `visible pores`, `every fabric thread`, `individual hair strands`, `intricate shoes` or global sharpening. Those phrases do not express the intended hierarchy and often damage likeness or painterly continuity.

## Diagnose Output Capacity

After inspecting the first result at thumbnail, mid and close scale, classify the observed behaviour:

Sparse environment detail is a diagnostic signal, not an automatic order to sharpen the person. It should trigger a closer character-material check. Restore the person only when one or more required face/skin/clothing/shoe/hand cues also fall below the sufficiency gate; if the person already passes, keep it unchanged even when the environment is intentionally quiet.

### Collapsed-detail output

Use this only when several signals agree:

- the environment has lost material/depth cues and reads as generic or empty;
- the face is geometrically intact or correctable but simplified into flat marks;
- skin, cloth and shoes share one treatment or have lost their visible construction;
- important seams, fold origins, shoe/ground contact or reflected colour disappear.

This indicates a limited rendering budget. Preserve the composition, colour and continuity contracts, then reallocate the remaining useful detail toward the focal person. Restore facial construction first, followed by material-defining structure for skin, clothing and shoes. Keep the environment broad, but retain a few necessary perspective, contact and material cues so the person remains embedded in the scene.

### Adequate output

The face passes the geometry gate; skin has quiet form turns; clothing and shoes read as different materials; the environment retains broad depth and material cues. Make no detail correction. Minor brush residue may vary.

### High-capacity or already-dense output

The face, skin, clothing, shoes and environment already read clearly at their intended scales. Do not strengthen microtexture. If anything competes, reduce redundant pores, threads, seams, hair strands, hard edges or high-frequency marks while preserving the material read.

## Focal Character Restoration Adapter

Use only for observed collapsed-detail output:

```text
Keep the composition lock, colour lock, pose, silhouette, shared light and environment masses unchanged. Restore the focal person with selective material clarity: correct and recheck the facial geometry and expression; give skin a few quiet cheek/jaw/limb colour turns with restrained reflected light; show clothing weight through major fold origins, overlap, hem/collar/cuff structure and only a few source-visible seams; show shoes through the upper/sole division, closure logic and ground contact. Concentrate the sharpest small marks around the eyes, expression, important hand contact and one or two shoe/clothing joins. Keep hair grouped and the environment broad but spatially legible. Do not add pores, every fabric thread, individual hair strands, dense stitching, global high-pass sharpening, extra accessories or texture pasted over all materials.
```

If the face also fails, the same targeted retry must include the facial-anatomy guard from [facial-control.md](facial-control.md). This is one focal-character correction, not two stacked stylistic adapters.

## Detail Sufficiency Gate

When a visible person is important, check:

1. facial geometry and expression pass the facial gate before surface detail is judged;
2. skin reads through quiet form and colour turns rather than flat fill, plastic gradient or pore noise;
3. clothing shows material weight and a few structural folds/joins rather than generic cloth texture or every wrinkle;
4. shoes show basic construction and ground contact rather than shapeless blocks or excessive stitching;
5. hands and prop contact remain readable where they carry the action;
6. the subject shares reflected colour, contact shadow and edge rhythm with the environment;
7. detail density supports the focal path: it is neither missing on the person nor maximized everywhere.

A result fails when the important person remains materially generic after the first pass, or when a capable result is degraded by unnecessary microtexture. Make at most one focal-character restoration correction. Reinspect the face and material gate afterward; if either still fails, report the limitation and do not call the image a pass.
