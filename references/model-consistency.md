# Model Consistency Contract

Use this reference to keep the art direction recognizable across different image models. Read `composition-color-lock.md` before writing this contract; composition and colour locks are invariants, while continuity and brush placement are rendering mechanisms. The target is **perceptual and directorial consistency**, not identical pixels. Different model families, versions, seeds, and inference systems will vary in brush placement, small contours, texture, and facial nuance; do not promise exact reproduction across them.

## Consistency Boundary

Lock the decisions that define the visual system. Allow the model to vary only the residue that does not change those decisions.

### Required invariants

1. **Semantic and topology contract** — output count, ratio/orientation, subject identity/count/action, protected objects and colours, depth order, adjacency, and any declared camera or landmark relationship. When a human face is visible, also lock head axis, eye-line, gaze, expression cues and relative feature spacing.
2. **Composition-distribution contract** — record Preserve-and-enrich or Directed-restage, crop/headroom, focal scale, quiet-area share, horizon, dominant diagonal/current, viewing path and any permitted macro change. A strong source distribution may not be silently tightened or enlarged.
3. **Macro-mass contract** — name roughly five to nine interlocking masses and their area, contour, overlap, direction or negative-space relationship. For Directed-restage, state the primary macro departure and supporting move; for Preserve-and-enrich, state the light/colour/edge/current enrichment instead.
4. **Value and colour-lock contract** — define exposure key, three large value groups, spatial owners for dominant field, structural counter, focal apex and neutral bridge, one primary contrast axis and protected local colours. Lock colour function and hierarchy, not exact RGB values.
5. **Contrast-ownership contract** — state which two or three contrast dimensions belong to the focal tier, which structural cues remain in the support tier, and which local-contrast, microcontrast, edge-density, hue-noise or texture-frequency dimensions are reduced in context.
6. **Shape and plane contract** — require rebuilt silhouettes and grouped internal planes before texture. Give the focal face/object roughly four to seven meaningful planes when appropriate; merge repeated foliage, windows, waves, folds or debris into broad rhythm groups.
7. **Material and edge contract** — for every important material, specify plane scale, mark direction, edge family, reflectance and focal density. When three or more important materials are visible, at least three must have clearly different grammars. Assign hardest, medium and soft/lost edge owners.
8. **Continuity contract** — bind important adjacencies through overlap, contact, turning form, reflected colour, shared light or atmosphere; use unequal internal colour turns and one structural stroke current without changing the composition/color lock.
9. **Facial contract when present** — use one perspective-aware eye band, a coherent gaze, a natural eye interval for the view, and a nose/mouth/chin axis that agrees with the head. Accidental slant, vertical drift, over-wide spacing, crossed gaze, off-axis features or generic replacement are failures; intentional asymmetry from pose or expression is allowed.
10. **Adaptive character-detail contract when a person is present** — first require a balanced hierarchy: face/expression; important hands and contact; clothing structure; shoe construction/contact; quiet skin turns; lower-frequency environment. After inspection, classify only the observed output as Collapsed, Adequate or High-capacity/already-dense. Collapsed output may receive one selective focal-character restoration; adequate/dense output may not receive extra pores, threads, strands, stitching or global sharpening.
11. **Anti-filter contract** — reject photographic shading preserved beneath global impasto, canvas grain, LUT, blur, bloom, vignette, uniform outlines or one repeated stroke. The source/result difference must survive thumbnail inspection and material differences must survive close inspection.

### Allowed variation

- exact brush-stamp shape and placement;
- minor microtexture and broken contour placement;
- small secondary folds, leaves, stones, windows, droplets, or cloud fragments;
- subtle hue shifts that keep the same colour owner and dominance hierarchy;
- facial nuance that preserves identity, expression, pose, plane hierarchy, head axis, gaze and relative feature spacing;
- exact skin, clothing and shoe micro-mark density when the face and material-sufficiency gates still pass and the focal/support/context hierarchy remains stable;
- runtime-specific wording or parameters outside the portable core.

Allowed variation becomes a failure when it changes the first read, breaks a recognition anchor, redistributes locked major masses, swaps colour roles, changes exposure key, equalizes focal and background contrast, or makes important materials share one surface treatment.

## Portable Render Contract

Before writing the final generation prompt, record this compact contract:

```text
Canvas/anchors: [count, ratio, identity, topology, protected colours; facial packet when present]
Composition lock: [Preserve-and-enrich or Directed-restage; crop/headroom, focal scale, quiet-area share, horizon, viewing path, permitted change]
Macro map: [5–9 masses, enrichment or primary departure, supporting move, thumbnail target]
Value/colour lock: [exposure key; dominant/support/apex; dominant field / structural counter / focal apex / neutral bridge; primary axis]
Contrast tiers: [focal / support / context]
Plane map: [silhouette and focal 4–7 planes; repeated detail groups]
Material grammar: [material -> plane scale, direction, edge, reflectance]
Edge hierarchy: [hard / medium / soft-lost owners]
Facial packet when present: [head axis; eye-line/gaze; eye size and interval; brow/nose/mouth/chin axis; expression; face-to-hair/neck/hand overlap]
Character detail when present: [balanced first-pass face/skin/hair/clothing/shoe/hand packet; intended density hierarchy; observed Collapsed/Adequate/High-capacity diagnosis; restoration or restraint decision]
Continuity packet: [internal turns; boundary relationships; shared light; structural current]
Anti-filter gate: [thumbnail, mid-scale, close-scale failures]
```

The final prompt may be shorter, but it must express every populated line as an observable visual decision. Use spatial owners and verbs: “the umbrella owns peak chroma,” “the forest becomes two broad wedges,” “skin uses quiet medium planes while metal uses sparse crisp streaks.” Do not depend on vague tags such as “high quality,” “masterpiece,” “more painterly,” or “same style.”

## Cross-model Evaluation

When actual multi-model comparison is requested:

1. Use the same source image, Source Card, composition/color lock, portable render contract, output count, and aspect ratio for every model.
2. Keep required decisions identical; translate only the minimum syntax needed by each runtime.
3. Inspect every output at thumbnail, mid, and close scale with [quality-gate.md](quality-gate.md). When people are present, also use [character-detail-adaptation.md](character-detail-adaptation.md) and [facial-control.md](facial-control.md); a model name is not a capacity diagnosis.
4. Mark each required invariant pass/fail. Do not average away a failure and do not select consistency by visual similarity alone.
5. A model set is consistent only when every output preserves the contract. Report remaining variation as brush residue, micro-detail variance, colour-role drift, geometry drift, lock drift, or another specific module.
6. If one model fails, make at most one correction targeted to the failed module. A combined face/material collapse may use one focal-character restoration packet. If it still fails, report that model as outside the supported consistency envelope.

## What Cannot Be Guaranteed

The skill cannot guarantee identical pixels, facial microgeometry, brush stamps, or random detail across different models. Seeds are not portable evidence: identical seed values can map to unrelated latent processes. Consistency comes from shared visual invariants plus identical acceptance gates. For machine-identical regions, use deterministic compositing or another non-generative workflow.
