# Model Consistency Contract

Use this reference to keep the art direction recognizable across different image models. The target is **perceptual and directorial consistency**, not identical pixels. Different model families, versions, seeds, and inference systems will vary in brush placement, small contours, texture, and facial nuance; do not promise exact reproduction across them.

## Consistency Boundary

Lock the decisions that define the visual system. Allow the model to vary only the residue that does not change those decisions.

### Required invariants

1. **Semantic and topology contract** — output count, ratio/orientation, subject identity/count/action, protected objects and colours, depth order, adjacency, and any declared camera or landmark relationship.
2. **Macro-mass contract** — name roughly five to nine interlocking masses and their area, contour, overlap, direction, or negative-space relationship. For expressive edits, state the primary macro departure and supporting move that must remain visible at 128–256 px.
3. **Value and colour-role contract** — define three large value groups plus spatial owners for dominant field, structural counter, focal apex, and neutral bridge or connector. Lock colour function and protected local colours, not exact RGB values.
4. **Contrast-ownership contract** — state which two or three contrast dimensions belong to the focal tier, which structural cues remain in the support tier, and which local-contrast, microcontrast, edge-density, hue-noise, or texture-frequency dimensions are reduced in context.
5. **Paint-architecture contract** — use [paint-architecture.md](paint-architecture.md). Lock selective contour language; unequal plane topology; the orientation/light/material/fold cause of important plane breaks; focal/support/context mark-density falloff; and the texture-removal result. `Faceted` without these fields is not a contract.
6. **Material and edge contract** — for every important material, specify construction, plane scale, mark direction, edge family, reflectance, and focal density. When three or more important materials are visible, at least three must have non-interchangeable grammars that pass the material-swap test. Assign hardest, medium, and soft/lost edge owners; forbid a complete uniform contour unless explicitly requested.
7. **Anti-shortcut contract** — reject photographic shading beneath global texture, cel/anime identity replacement, two-band cel shading, complete ink outlines, random low-poly mosaics, horizontal posterization, opaque brush slabs used as scenery, or one repeated stroke. The source/result difference must survive thumbnail inspection, form must survive texture removal, and material differences must survive close inspection.

### Allowed variation

- exact brush-stamp shape and placement;
- minor microtexture and broken contour placement;
- small secondary folds, leaves, stones, windows, droplets, or cloud fragments;
- subtle hue shifts that keep the same colour owner and dominance hierarchy;
- facial nuance that preserves identity, expression, pose, and plane hierarchy;
- runtime-specific wording or parameters outside the portable core.

Allowed variation becomes a failure when it changes the first read, breaks a recognition anchor, redistributes the major masses, swaps colour roles, equalizes focal and background contrast, or makes important materials share one surface treatment.

## Paint-architecture Fingerprint

The same visual family is recognized across models by five coupled observations, not by a style name:

1. **Contour:** focal hard fragments, medium broken joins, and lost context edges; no automatic full-object ink line.
2. **Plane topology:** one dominant plane plus fewer unequal supporting planes, each caused by orientation, light, material, fold mechanics, or a declared silhouette choice.
3. **Mark gradient:** the finest useful marks belong to the focal path; support is quieter; context uses broad grouped traces.
4. **Material coupling:** the direction, scale, edge and reflectance of a mark reveal what surface it belongs to even when hue is ignored.
5. **Spatial foundation:** overlap, perspective, atmospheric separation and value grouping remain readable beneath the 2D paint intervention.

If outputs share colour and subject but not this fingerprint, they are not cross-model consistent.

## Portable Render Contract

Before writing the final generation prompt, record this compact contract:

```text
Canvas/anchors: [count, ratio, identity, topology, protected colours]
Macro map: [5–9 masses, primary departure, supporting move, thumbnail target]
Value map: [dominant/support/apex]
Colour roles: [dominant field / structural counter / focal apex / neutral bridge]
Contrast tiers: [focal / support / context]
Paint architecture: [selective contour; focal 4–7 unequal planes and their causes; support 3–5; context 1–3 per rhythm mass; subordinate transitions]
Mark ladder: [focal 1.0 / support about 0.5 / context about 0.2–0.33]
Material grammar: [material -> construction, plane scale, mark direction, edge, reflectance; three non-interchangeable when present]
Edge hierarchy: [hard / medium / soft-lost owners]
Texture-removal result: [silhouette, depth, light, value groups that survive]
Shortcut adapter: [None / Cel-anime / Brush-slab-filter / Low-poly-posterization / Source-template]
Anti-filter gate: [thumbnail, mid-scale, close-scale failures]
```

The final prompt may be shorter, but it must express every populated line as an observable visual decision. Use spatial owners, causes, and verbs: “the umbrella owns peak chroma,” “the forest becomes two broad wedges,” “cheek and jaw planes change because they turn from the key light,” “skin uses quiet medium planes while metal uses sparse crisp streaks.” Do not depend on vague tags such as “high quality,” “masterpiece,” “more painterly,” “faceted,” or “same style.”

## Cross-model Evaluation

When actual multi-model comparison is requested:

1. Use the same source image, Source Card, portable render contract, output count, and aspect ratio for every model.
2. Keep required decisions identical; translate only the minimum syntax needed by each runtime.
3. Inspect every output at thumbnail, mid, and close scale with [quality-gate.md](quality-gate.md), plus the texture-removal, material-swap, continuous-outline and plane-cause tests in [paint-architecture.md](paint-architecture.md).
4. Mark each required invariant pass/fail. Do not average away a failure and do not select consistency by visual similarity alone.
5. A model set is consistent only when every output preserves the contract. Report remaining variation as brush residue, micro-detail variance, colour-role drift, geometry drift, or another specific module.
6. Diagnose the behaviour, not the brand: `Cel-anime`, `Brush-slab-filter`, `Low-poly-posterization`, `Source-template`, or another specific module. Append only the matching adapter while keeping the portable core unchanged.
7. If one model still fails after one targeted correction, report it as outside the supported consistency envelope. Do not keep adding adjectives or silently accept the nearest attractive image.

## What Cannot Be Guaranteed

The skill cannot guarantee identical pixels, facial microgeometry, brush stamps, or random detail across different models. Seeds are not portable evidence: identical seed values can map to unrelated latent processes. It also cannot force a runtime whose image editor ignores source geometry or negative instructions into compliance. Consistency comes from shared visual invariants, a closed paint-architecture fingerprint, behaviour-based adapters, and identical acceptance gates. For machine-identical regions, use deterministic compositing or another non-generative workflow.
