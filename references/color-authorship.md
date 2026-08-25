# Color Analysis and Authorship

Read this for every generation, edit, prompt-only, reference analysis, or finished-frame review. The objective is not to force a particular palette; it is to make the system accountable for color selection, balance, hierarchy, and source fidelity.

## Separate Observation from Design

When a source image exists, audit it before proposing colors:

- large value groups independent of hue;
- dominant and secondary hue families, neutrals, and near-neutrals;
- warm/cool distribution without assuming it must be opposed;
- saturation map: where color is muted, concentrated, clipped, or competing;
- spatial ownership: foreground, subject, environment, atmosphere, focal event;
- material/local-color anchors that affect identity, brand, wardrobe, species, architecture, or recognition;
- light color, shadow color, reflected color, and atmospheric shift;
- adjacent regions that merge unintentionally or compete for attention;
- what already works and what actually needs correction.

Do not call a source “flat” merely because it is monochrome, cool, warm, pastel, or low-saturation. A narrow palette can be excellent when value, chroma, and spatial ownership are deliberate.

## Choose an Authorship Mode

Choose independently from identity fidelity, abstraction, and exposure.

- **Preserve-and-refine:** retain the source hue families and protected color anchors; improve value separation, saturation hierarchy, neutral balance, shadow coherence, and focal ownership. Use when the source palette is already functional or color identity is protected.
- **Rebalance:** retain the source's main hue identity but change relative area, value, chroma, adjacency, or spatial placement so the focal path and material separation work better.
- **Re-script:** assign new hue families and color roles while preserving declared anchors. Use when the source palette undermines the requested mood/hierarchy or the user authorizes stronger transformation.

Do not default to Re-script merely because the transformation is Style-first. First ask whether the source palette already supports the intended frame. Do not use Re-script to overwrite protected skin, wardrobe, product, brand, species, signage, or architectural colors unless allowed.

## Select Contrast by Function

Choose one primary contrast axis and, only when useful, one subordinate axis. The best choice is the one that solves the frame's attention, separation, depth, or emotional problem.

| Strategy | Best use | Control |
|---|---|---|
| Value-led, narrow hue family | solemn, misty, nocturnal, pale, archival, or restrained scenes | keep hue close; separate masses through light/dark and edge |
| Analogous harmony | continuity, quiet atmosphere, organic flow, memory | create hierarchy through value/chroma; allow one small hue departure if needed |
| Complementary or split-complementary | explicit tension or subject/environment separation | make one family dominant; prevent equal saturated competition |
| Warm-cool organization | light/shadow, intimacy/distance, body/environment, practical/ambient separation | use only when scene/material/light logic benefits; either side may dominate |
| Saturation contrast | focal event inside a muted world | localize peak chroma and keep supporting colors quieter |
| Hue-boundary separation | adjacent equal-value forms need distinction | shift hue locally; do not recolor the whole frame |
| Near-monochrome with rupture | pressure, isolation, graphic clarity | let one small hue/value event break the field |
| Local color versus colored illumination | identity/material must remain while lighting changes | preserve local-color anchors and show believable light influence |

These are tools, not presets. Never require a warm accent in a cool scene, a cool anchor in a warm scene, complementary pairs, or teal-orange simply to signal style.

## Build a Role and Ownership Map

Assign visible responsibilities before exact hues:

- **Dominant field:** the broad emotional/atmospheric family;
- **Structural counter:** separates depth, subject, architecture, or major material masses;
- **Focal accent/apex:** the color event with highest attention ownership; it may be small or occupy a larger focal subject;
- **Connector/echo:** an optional quieter recurrence that links distant regions;
- **Neutral bridge:** black, gray, cream, brown, desaturated local colors, or another low-chroma family that prevents every region from competing.

For every role, specify spatial owner, approximate area hierarchy, value range, and saturation level. Do not list attractive colors without saying where they live. Exact percentages are optional; dominance must be visible. Avoid two unrelated high-chroma families occupying similar area unless equal conflict is the intended narrative.

Roles do not need different hues. In analogous, near-monochrome, or value-led plans, the structural counter and focal apex may come from value, chroma, edge, or material shifts inside one hue family. “Balanced” means controlled visual weight, not equal color area.

## Build Richness Through Area and Anchors

When the user wants colour that feels richer, stronger, or more memorable, do not respond with a global saturation increase or with excessive background desaturation. Use the positive target in [positive-quality-anchor.md](positive-quality-anchor.md):

- let one dominant field occupy enough area to establish the frame's colour identity;
- give one structural counter a different value, hue, temperature, material or chroma role;
- localize the cleanest chroma or strongest hue boundary on the focal apex;
- keep a neutral bridge so large saturated fields have visual breathing room;
- place one contained dark or light anchor so the image does not collapse into equally bright midtones.

Large coloured areas are allowed and may remain saturated. Richness comes from clean ownership, area hierarchy, value separation, and neutral/dark support—not from making every object vivid. If the source already has a strong broad blue, green, earth, snow, water, wall, skin, cloth, or other field, Preserve-and-refine or Rebalance may strengthen it rather than washing it into chromatic gray.

Run the **colour-area test** at thumbnail scale: can the dominant field, structural counter, focal apex, neutral bridge, and dark/light anchor be located spatially? Roles may merge when the scene is intentionally restrained, but a colour-rich request fails when all regions converge to pale, dusty, equal mid-chroma or when context quieting erases the source's attractive colour identity.

## Quiet Context Through Chromatic Gray

When non-focal areas compete, reduce their color complexity rather than neutralizing the entire frame.

- Converge minor hues toward one scene-owned near-neutral family: blue-gray, green-gray, violet-gray, warm stone gray, desaturated local color, or another motivated chromatic gray.
- Lower hue noise and mid-saturation competition before lowering all saturation.
- Preserve broad light/shadow depth shifts, local-color traces, and material differences; snow, wood, skin, stone, foliage, metal, and fog must not become the same gray substance.
- Pair color quieting with lower local contrast, microcontrast, hard-edge density, and texture frequency in the Tier 3 context field from `directorial-contrast.md`.
- Keep the focal owner and protected colors stable. Do not correct a busy background by globally desaturating or lifting blacks over the subject.
- Reduce hue noise, competing small accents, microcontrast, hard-edge density and texture frequency before reducing the area or saturation of a successful large colour field.

The objective is a colored, coherent field that reads before its individual objects. Uniform gray fog, muddy low saturation, and a full-frame faded overlay fail.

## Decide Whether a Color Collision Is Needed

Color collision is optional. Declare `None`, `Preserve existing`, or `Author new`.

If authoring a collision, specify:

- the two spatial/material owners;
- the boundary or transition where they meet;
- the dominant side by area;
- the attention, depth, relationship, or event problem it solves;
- the protected colors that may not be overwritten.

The collision may use hue, temperature, saturation, value, near-white/near-black rupture, local color versus illumination, or a hard material/color boundary. It need not be complementary or warm-cool. Keep the strongest collision localized to the focal path or one deliberate counterweight; do not distribute equal collisions across the frame.

When the source palette is already quiet and strong, choose no new collision and preserve its topology. More difference is not automatically better color authorship.

## Balance Color with Value, Light, Material, and Depth

- Verify the focal read in grayscale; hue contrast must not conceal a broken value plan.
- Let light modify local color rather than replacing every material with the light hue.
- Tint shadows deliberately, but preserve separation inside dark masses and avoid neutral-black fill.
- Use atmospheric color shifts to support depth, not as a uniform haze overlay.
- Keep skin, cloth, metal, water, foliage, stone, smoke, snow, and energy materially distinct even when they share a hue family.
- Reserve peak saturation, clean complements, and the strongest hue boundary for the focal path or a deliberate counterweight.
- Reduce color noise before adding accents. A missing neutral bridge often causes imbalance more than a missing complementary hue.
- Evaluate the color-block map at thumbnail scale. Rebalance/Re-script should change visible area, adjacency, or ownership, not merely produce a different overall cast.

## Generalized Evidence from the Visual References

Across the researched bright/dark, character/environment, civic/industrial, organic, action, and abstract color keys, stable behavior is functional rather than palette-specific:

- story and attention determine color roles before exact hue;
- exact palettes change dramatically while a dominant field, structural counter, and controlled apex remain legible;
- colored light and nonliteral shadow can create emotion without erasing material/local-color identity;
- hue, value, chroma, edge, and atmosphere share the separation workload rather than all being maximized;
- palette changes can accompany narrative or spatial transitions, but one frame still needs internal balance;
- graphic color boundaries reinforce planes and 2D intervention;
- no character, city palette, rune color, or single published color script is reusable content.

Use researched frames as evidence for these behaviors, never as palettes to sample or exact color layouts to copy.

## Prompt Compilation

Use a compact visible contract:

```text
Color authorship: use [Preserve-and-refine/Rebalance/Re-script]. The source already succeeds at [observed strengths] and needs correction at [specific issue]. Use [primary contrast strategy] with [optional subordinate strategy]. Assign [dominant field: location, hue family, value, chroma], [structural counter: owner and function], [focal accent/apex: owner and function], and [optional connector/neutral bridge]. The Tier 3 context converges toward [scene-owned chromatic gray/quiet color family] through lower [hue noise/local contrast/microcontrast/edge density/texture frequency] while retaining [depth/material cues]. Color collision is [None/Preserve existing/Author new: owners, adjacency, dominance, function]. Preserve [protected local-color anchors]. Let [motivated light] influence rather than replace material color. Avoid [specific likely imbalance or cliché].

For colour-rich work, also name [contained dark or light anchor] and state which large field may retain saturation after context quieting.
```

Name exact hue families only after roles are clear. Prefer two or three important color decisions over a long palette inventory.

## Color Failure Conditions

Reject or correct:

- a global LUT or gradient map standing in for spatial color design;
- forced warm-cool, complementary, teal-orange, purple-green, or other formula without scene ownership;
- source colors copied passively when they undermine the requested hierarchy;
- source colors changed unnecessarily when their identity and balance already work;
- equal-area/equal-saturation competition without intentional conflict;
- decorative accent colors that do not belong to subject, material, light, atmosphere, or narrative;
- hue contrast with collapsed values, or value contrast that destroys protected color identity;
- muddy mixtures caused by too many mid-saturation hues and no neutral bridge;
- non-focal regions carrying the same peak chroma, hue-boundary strength, microcontrast, and edge density as the focal owner;
- colour-rich source fields washed into pale or dusty equal midtones merely to make context quieter;
- uniform gray fog, global desaturation, or lifted-black haze replacing scene-owned chromatic gray and spatial depth;
- a strong color collision with no declared owners, adjacency, dominant side, or narrative/attention function;
- every shadow sharing one hue regardless of material and illumination;
- color that makes depth, lighting direction, or material response contradictory.
