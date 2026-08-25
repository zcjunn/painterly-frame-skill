# Source Analysis and Image Roles

Read this whenever an image is supplied.

## Assign Roles Before Style

Give every image one primary role. For edit targets, choose six independent controls: identity/structure fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode.

| Role | What may enter the result | Required handling |
|---|---|---|
| Pixel-locked region | Exact original pixels | Keep outside generative redraw; composite and verify deterministically |
| Edit target | Identity/object/scene structure | Use an actual image edit call and state invariants |
| Support insert | Named person, object, texture, or prop | Number inputs and limit each to its declared role |
| Semantic source | Relationship, action, palette role, or mood | Analyze first; original pixels need not appear |
| Style reference | Composition, value, color function, material, edge, FX | Extract grammar; exclude subject, text, brand, and exact layout |

Fidelity:

- **High:** preserve identity, count, proportions, signature features, object geometry, order, and recognizable color anchors.
- **Medium:** preserve the core subject and relationships; allow crop, surface, palette, and surrounding staging changes.
- **Low:** preserve only semantic relationships or visual grammar.

Transformation mode:

- **Identity-first:** preserve recognizable face/body/object geometry closely; redesign color, light, edges, and surfaces. Use when exact likeness or product/architecture recognition dominates.
- **Balanced:** preserve signature identity, count, pose, and structural relationships; allow controlled crop, planar facial stylization, silhouette cleanup, merged detail, and environment reshaping.
- **Style-first:** preserve the semantic minimum and recognizable anchors; deliberately reconstruct proportions, contours, planes, materials, and nonessential layout. Use when the user prioritizes a stronger painterly-animation result and permits departure from 1:1 realism.

Scene emphasis:

- **Character/Object:** an inspectable face, pose, creature, product, prop, or mechanism carries the focal event.
- **Environment:** landform, architecture, spatial void, weather, light, or directional flow carries the focal event.
- **Relationship:** subject and environment depend on each other; neither may be treated as a passive backdrop.

Abstraction strength:

- **Restrained:** preserve spatial distribution and recognizable geometry; simplify surfaces, repeated detail, light, and color grouping.
- **Expressive:** preserve a short anchor set while making one thumbnail-visible primary macro departure plus one supporting move. The primary move must change a major area, contour, overlap, focal scale, negative space, light shape, perspective/depth interval, or color-zone relationship; minor movement on several axes does not qualify.
- **Radical:** preserve only the semantic minimum and a few anchors; make at least two primary-level departures and permit major restaging, subjective graphic rupture, or strong area redistribution. Use only with clear user authorization.

Do not infer abstraction from exposure. For a Style-first environment with no protected geometry, default to Expressive rather than conventional scenic realism. For identity-first or protected architecture/product geometry, default to Restrained unless the user explicitly permits more.

Exposure key:

- **High-key:** broad light field with a dark/chromatic anchor.
- **Mid-key:** balanced light and shadow groups with one controlled apex.
- **Low-key:** dominant dark field with separated shadow structure and a limited light event.

Infer exposure from the source and story. Do not default to low-key because the request mentions this style family.

Color-authorship mode:

- **Preserve-and-refine:** keep source hue families and protected anchors; improve balance and hierarchy.
- **Rebalance:** keep the source's main color identity while changing area, value, saturation, adjacency, or spatial ownership.
- **Re-script:** assign new hue families and color roles while preserving declared anchors; use only when the source is not serving the intended frame and the transformation allows it.

Choose after the color audit in `color-authorship.md`. Do not infer Re-script from Style-first, or warm-cool contrast from any mode.

## Build a Source Card

Record compactly:

```yaml
file_facts:
  size: observed dimensions if available
  ratio: observed aspect ratio
  orientation: landscape / portrait / square
  quality_limits: blur, crop, occlusion, compression
image_role: one primary role
identity_fidelity: High / Medium / Low
transformation_mode: Identity-first / Balanced / Style-first
scene_emphasis: Character/Object / Environment / Relationship
abstraction_strength: Restrained / Expressive / Radical
exposure_key: High-key / Mid-key / Low-key
color_authorship_mode: Preserve-and-refine / Rebalance / Re-script
distribution_policy: Preserve protected layout / Selectively restage / Major restage
composition_color_lock:
  mode: Preserve-and-enrich / Directed-restage
  composition_strengths: negative space, focal scale, headroom, horizon, quiet-area share, diagonal/current
  preserve: ratio, crop, topology, viewing path, value and colour hierarchy
  permitted_changes: exact user-authorized restaging only
  exposure_key: High-key / Mid-key / Low-key with reason
  primary_contrast_axis: value / analogous / complementary / warm-cool / saturation / hue-boundary / other justified axis
observed:
  core_subjects: 1-2 identity-defining subjects
  supporting_facts: 2-4 scene facts
  identity_invariants: face, body, product, architecture, markings, wardrobe color
  spatial_invariants: only declared count, left-right order, gesture, gaze, horizon, overlap, or scale relationships that must remain
  facial_packet_when_present: head axis, eye-line, gaze, expression cues, relative eye size/interval, brow-nose-mouth-chin axis, face-to-hair/neck/hand overlap
  character_detail_packet_when_present: visible skin turns, hair grouping, clothing material/weight/fold origins/joins, shoe upper-sole-closure-contact, important hands and prop contact; omit unobservable microdetail
  dominant_gesture: horizontal / vertical / diagonal / curve / gaze / motion
  current_visual_weight: area, value, chroma, texture, isolation
  color_audit:
    value_groups: large light/mid/dark ownership independent of hue
    hue_families: dominant, secondary, neutrals
    temperature_map: spatial warm/cool distribution without assuming opposition
    saturation_map: muted, concentrated, clipped, or competing regions
    spatial_material_ownership: subject, foreground, background, atmosphere, important materials
    protected_color_anchors: identity, wardrobe, product, brand, species, architecture, text
    light_shadow_reflection: source color, shadow color, reflected color, atmospheric shift
    strengths: relationships already supporting the frame
    problems: adjacency, hierarchy, material, depth, or balance issues actually needing correction
    contrast_audit: global span, local contrast, microcontrast, edge density, chroma, hue noise, texture/FX density and their current owners
  quiet_areas: low-information regions
  composition_strengths: existing negative space, subject scale, headroom, horizon, colour area or viewing path worth preserving
  visible_text_brand: preserve exactly or exclude
inferred:
  narrative_event: what appears to be happening
  emotional_tension: restrained inference, not fact
semantic_minimum: facts required for recognition
recognition_anchors: identity, count, pose, signature silhouette, spatial relationship, color anchors
transformable_elements: any user-authorized crop, minor proportions, surface construction, repeated detail, secondary props, ornament, texture, or atmosphere
directorial_transform_proposal:
  dramatic_proposition: actor + visible pressure/counterforce + intended first read
  primary_macro_departure: one scale/area/crop/occlusion/perspective/negative-space/light/color-zone/subjective-graphic change
  supporting_move: one secondary visible change
  area_contour_impact: which major mass, silhouette, overlap, light shape, or color-zone relationship changes
  protected_invariants: what this proposal may not alter
  incidental_distribution_not_preserved: headroom, exact crop/horizon, repeated assets, secondary detail, or local contrast when allowed
contrast_ownership:
  tier_1_focal: owner plus selected peak value/edge/chroma/hue-boundary/texture/FX dimensions
  tier_2_support: structural owner plus medium cues retained for depth and relation
  tier_3_context: scene-owned chromatic-gray/colored field and dimensions compressed without losing depth/material
color_collision_decision:
  mode: None / Preserve existing / Author new
  owners_and_adjacency: who meets where
  dominance_and_function: which side owns area and why the collision exists
thumbnail_difference_target: one major mass/area/contour/overlap/focal-scale/light-topology/color-zone difference visible at 128–256 px
color_plan:
  primary_contrast: value / analogous / complementary / split-complementary / warm-cool / saturation / hue-boundary / near-monochrome rupture / local-color versus illumination
  subordinate_contrast: optional; do not maximize every axis
  dominant_field: spatial owner, hue family, value, chroma
  structural_counter: spatial/material owner and separation job
  focal_accent_apex: owner and attention job
  connector_echo: optional quiet recurrence
  neutral_bridge: low-chroma family preventing equal competition
  protected_anchors: colors that must remain recognizable
continuity_plan:
  boundary_relationships: important adjacency -> occlusion / turning form / contact / atmospheric merge / reflected-colour bridge / graphic seam
  internal_colour_turns: broad base plus a few unequal light/form/material shifts for each important mass
  structural_stroke_current: cloud / field / road / cloth / water / shadow direction carrying the viewing path
  shared_light_bridges: key, shadow family and one or two reflected-colour echoes across owners
  depth_frequency_falloff: foreground / middle / atmosphere edge and mark behaviour
  likely_model_adapter: None / Cut-paper-colour-block / Poster-fill-cel-band / Brush-stamp-slab / Global-texture-filter / Sticker-airless-depth / Focal-character-detail-collapse
post_output_character_diagnosis:
  observed_capacity: Collapsed-detail / Adequate / High-capacity-or-already-dense
  evidence: face geometry, skin turns, clothing structure, shoe/contact structure, hand/prop contact, environment depth/material cues
  decision: one focal-character restoration / no change / remove redundant microtexture
environment_design:
  hero_form: primary landform, structure, void, weather mass, or light shape
  counterform_current: opposing or guiding source-owned mass/direction
  visual_verb: presses / splits / climbs / funnels / opens / resists / another visible relation
  macro_shape_budget: usually 5-9 interlocking masses
  primary_macro_departure: one source-owned transformation that changes the composition decision
  supporting_move: a second move that reinforces the hero/counterforce relationship
  optional_additional_axes: only changes that remain visibly useful; axis count alone is not success
  repeated_detail_policy: which trees, rocks, windows, waves, foliage, rubble, or reflections become grouped rhythms
shape_rebuild:
  subject_planes: silhouette and 4-7 meaningful face/object planes
  environment_masses: broad graphic forms replacing repeated detail
  material_grammars: distinct marks for 3-5 important materials
allowed_changes: user-authorized changes
hard_avoids: identity drift, added objects, sample residue, text errors
```

Do not invent unseen facial features, object backs, hidden text, location, date, or story as observed fact.

## Translate the Source

1. Keep the semantic minimum and recognition anchors; do not automatically preserve every visible detail.
2. Read `composition-color-lock.md` and choose Preserve-and-enrich or Directed-restage before applying the transformation mode. In Preserve-and-enrich, simplify and repaint without silently changing the source distribution; in Directed-restage, change only the declared axes.
3. Rebuild the focal silhouette, internal colour turns and major surrounding masses before adding brush marks. Apply the same logic to people, creatures, products, buildings, machines and environments.
4. Read `directorial-contrast.md`. For Directed-restage/Expressive/Radical work, require a dramatic proposition, one primary macro departure, one supporting move and a thumbnail difference target. Preserve-and-enrich uses light shape, colour adjacency, edge rhythm or a viewing current as its enrichment instead of mandatory crop or scale change.
5. For environment-emphasis, read `environment-abstraction.md`. Select a hero form, a counterform/current, and a visible verb. Make the primary departure change their scale, area, contour, overlap, negative-space, light-shape, perspective, or color-zone relationship rather than merely changing palette and brush texture.
6. Merge repeated micro-detail into larger shapes and assign each important material a distinct mark grammar derived from its behavior. Exact distributions of incidental trees, rocks, windows, waves, leaves, snow clumps, rubble, and reflections are not invariants unless declared.
7. Choose one focal event and one composition family from `style-system.md`; restage or crop only when the lock permits it.
8. Assign focal/support/context contrast tiers. Lower context local contrast, microcontrast, edge density, hue noise and texture frequency selectively; retain broad depth, material identity, motivated colour and any protected subject geometry.
9. Read `color-authorship.md`. Audit what already works, choose Preserve-and-refine by default (or Rebalance/Re-script with reason), then assign one primary contrast axis, an optional subordinate axis, spatially owned colour roles and an explicit None/Preserve/Author color-collision decision. Keep source-derived color anchors when recognition depends on them; never add warm-cool or complementary contrast by reflex.
10. Read `painterly-continuity.md` and bind the locked masses through boundary relationships, internal turns, shared light and material-owned strokes. Add at most one observed model adapter.
11. When a person appears, read `character-detail-adaptation.md`. Record only visible material evidence and use the balanced first-pass character packet. After generation, diagnose observed output capacity; strengthen the focal person only for Collapsed-detail behaviour, and remove or avoid redundant microtexture for an already capable result.
12. Change only what the user allowed.

For Edit Target, write prompt clauses as `Preserve anchors Y; reconstruct elements X`. Do not imply that “stylize” grants permission to change identity, count, protected geometry, or required text, but do not promote incidental photographic detail to an invariant either.

## Analyze Style References

For each reference, record:

- observed value groups and focal location;
- color roles and high-chroma area;
- light-source geometry;
- composition family and viewing path;
- material/edge/brush behavior;
- FX shape language;
- text, character, object, location, brand, and exact-layout residue.

Then separate:

- **Fixed:** repeats across multiple references and is necessary for family recognition.
- **Variable:** changes while the family remains recognizable.
- **Sample residue:** belongs to a particular frame and must not be generalized.

With one reference, label confidence as low and avoid claiming statistical rules. With multiple references, do not promote a feature merely because two frames from the same sequence share it.

## Multi-image Requests

Number inputs and state the interaction:

```text
Image 1 — High-fidelity edit target: preserve person A and clothing colors.
Image 2 — Support insert: use only the mechanical object; adapt its lighting.
Image 3 — Style reference: learn value topology and edge rhythm; copy no subject or text.
```

If two images compete to define identity, geometry, or output ratio and the user has not resolved the conflict, ask one necessary question.
