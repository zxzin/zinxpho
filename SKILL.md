---
name: zinxpho
description: Create two radically different high-energy web design directions from a user-provided photo. Use when the user invokes "zinxpho" or wants bold editorial art direction built around an authentic subject, with subject preservation, true person cutout/extraction, sacred/epic subject portrayal, stable subject motion, reference-quality layered HTML/CSS motion, surprising multi-style visual worlds, dense environmental typography, A/B HTML outputs, and optional Apple Live Photo / 实况图 packaging for easier Douyin/Xiaohongshu sharing.
---

# Zinxpho

## Overview

Use this skill when the user wants graphic-design-heavy, image-led output based on a real photo rather than a generic website or a fully regenerated portrait.

This skill is for:
- preserving the user's authentic subject
- isolating or cleaning the person/subject as a foreground cutout when the image is person-led
- integrating the subject into visually intense HTML/CSS compositions
- making the person or authentic subject the first visual read when the source image is person-led
- portraying the person with a sacred, epic, monumental presence across styles
- building layered depth, typography, motion, and graphic systems around the subject instead of placing flat labels on top of a photo
- producing surprising, high-impact visual directions across different aesthetics rather than locking into one house style
- producing two clearly different design directions as separate files
- optionally packaging dynamic HTML outputs as Apple Live Photo pairs for social sharing
- shipping final-facing banners, posters, and hero compositions rather than annotated mockups

Do not use this skill for:
- ordinary UI polish
- simple banners or posters with one safe layout
- requests without a usable image when the subject's real likeness matters

## Trigger and input requirements

This skill should trigger when:
- the user explicitly says `zinxpho`
- the user wants extreme editorial/graphic-design treatment around their real photo
- the user wants multiple bold directions instead of one conservative layout
- the user wants a shareable dynamic image, Live 图, 实况照片, or image post that can still show the HTML motion

This skill requires an image when the user's authentic likeness is central to the request. If no usable image is available, stop and ask for one.

## Required workflow

Follow this workflow in order.

### Step 1: Preserve the authentic subject

The subject's face, features, and clothing must remain recognizably authentic. Do not redraw the person from scratch when the task depends on their real likeness.

If the user provides a local image file, inspect it with `view_image` first so the image is available in context.

If you need raster isolation, background removal, or photo transformation, use the best image generation/editing capability available in the current agent environment.

When the workflow needs true subject isolation, read [references/extraction-prompts.md](./references/extraction-prompts.md) and use its prompt skeleton or retry prompt rather than improvising loosely.

Do not pin the workflow to a specific image model or provider unless the user explicitly asks for one. By default, use the strongest available image generation/editing route exposed by the current agent environment.

When the source image is person-led, default to making a **true foreground extraction** before design. Treat the person cutout as the hero layer, and treat the original photo/background as optional texture, context, or backup. Only skip extraction when the user explicitly asks to keep the whole photo intact, the person is not central, or extraction quality would clearly damage identity.

When prompting image generation or editing:
- explicitly preserve identity
- explicitly forbid face and clothing changes
- prefer extraction, cleanup, and compositing over redraw
- ask for a transparent background first when the workflow needs a usable cutout
- ask for a neutral solid background only when transparency is unavailable or clearly inferior
- prefer the current agent's strongest available image generation/editing route instead of hardcoding a model or provider name

Hard extraction rules:
- do not accept a simple crop, zoom, or reframed portrait as a substitute for cutout
- do not treat a full rectangular photo frame as the main solution when the task is person-led and asks for a designed result
- preserve the full usable silhouette whenever possible, including hair, shoulders, arms, hands, clothing outline, and leg shape if visible
- keep edge fidelity high enough that the subject can be placed over a different background without an obvious box, matte, or leftover scene fragments
- remove original background content behind the subject instead of merely blurring or darkening it when the design needs true isolation

If a first extraction result behaves more like a crop than a cutout, iterate immediately with a stricter prompt focused on foreground separation, transparent background, and edge cleanup.

If the original photo is already compositionally strong, you may keep it as a background, texture, reflection, or secondary layer, but still prefer a separate foreground subject layer for the main design read when the person is central.

### Step 2: Solve integration, not just cutout

After extraction, make the subject belong to the composition. Do not stop at dropping a raw cutout on top of a background.

When the source image is person-led, the person must remain the dominant visual focus. Typography, overlays, background systems, glitches, masks, and motion should frame, amplify, or interact with the person rather than burying them.

Use CSS and composition techniques such as:
- aggressive color grading with `filter`
- masking with `mask-image`, gradients, blur falloff, or soft edge treatments
- perspective, depth, and scale contrasts
- intentional overlap between typography, shape systems, and the subject silhouette
- 3D text ribbons, banner bands, ticker strips, repeated words, image slices, clipped photo echoes, and rotating microtype with visible front/back depth
- graphic rings, arches, crowns, wave bands, grid bands, or ornament bands that wrap around the cutout instead of behaving like loose overlay effects
- style-specific graphic systems that wrap around the cutout, such as chrome/glass shards, botanical ornament, ukiyo-e waves, baroque curtains, zine scraps, pixel grids, neon signage, halftone dots, or editorial type architecture
- controlled flicker, jump cuts, scanline flashes, and rhythmic layer swaps that add energy without hiding the face

When using heavy 3D transforms, do not rely on blend modes alone to hide extraction edges.

If a composition needs grandeur, create it with scale, framing, depth separation, arches, crowns, layered typography, monumental negative space, and strong silhouette contrast. The epic read should come from the whole composition and subject-centered systems, not from a loose overlay effect.

### Step 2.5: Make the person monumental, not jittery

When the source image is person-led, treat the person as a stable icon, monument, saint, heroine, sovereign figure, altar centerpiece, or mythic protagonist. This sacred/epic presence should hold across styles, even when the surrounding style is pop, zine, cyber, Swiss, ukiyo-e, baroque, floral, chrome, or risograph.

The person should feel elevated rather than tossed around by the graphic system.

Hard motion rules for the subject layer:
- do not apply random body jitter, step-based slipping, wiggle, twitch, shake, or comedic wobble to the main person layer
- do not rotate the whole body back and forth unless the user explicitly asks for a playful or chaotic effect
- keep the face and body posture visually stable across the loop
- if the subject layer moves, limit it to slow ceremonial parallax, tiny breathing scale, or a restrained camera push that does not change the person's dignity
- put motion on the surrounding system instead: text ribbons, banner bands, graphic rings, typography, particles, curtains, waves, grid lines, scanlines, shadows, reflections, and background plates
- keep text-ribbon crowns, graphic rings, and orbit bands slow and ceremonial; they should feel like ritual motion, not UI loading spinners or glitch effects
- reserve faster motion only for small peripheral accents such as tiny scanlines, edge sparkles, small ticker details, or brief signal pulses, and never let those accents become the main read
- duplicate/echo subject layers are allowed only as aura, shadow, reflection, or afterimage; they must not make the person look like they are glitching or being shaken

Good motion reads as:
- the world is slowly moving around the person
- text banners, ornament, and symbols orbit the person like a halo, procession, or ceremonial frame
- the orbit system passes partly behind and partly in front of the subject, creating a real wraparound read
- the camera is reverently pushing toward the person

Bad motion reads as:
- the person is vibrating
- the person is being dragged by the layout
- the body is bouncing for no reason
- the portrait feels goofy, nervous, or unstable
- halo-like text or ornaments whip around the person like a carnival sign

### Step 2.6: Build a reference-quality depth stack

If the user points to a folder of strong HTML examples, inspect at least three matching files before designing. Treat their code and rendered screenshots as reference for motion grammar, not as templates to reskin.

Proven Zinxpho-style HTML usually has a deliberate stack:
- a stage or camera container using `perspective` and `transform-style: preserve-3d`
- a deep photo bed from the original image, often blurred, color-graded, oversized, or clipped into echoes
- a style-world layer: Swiss grid, image shards, cyber grid, ornamental arch, halftone field, theatrical panel, botanical frame, chrome shards, waves, or print texture
- environmental typography: giant type tracks, vertical text, stamps, rails, mastheads, side labels, or ticker systems that belong to the world
- a stable foreground subject cutout with strong edge treatment and shadow
- foreground accents such as particles, scanlines, small tickers, petals, route rings, metadata stamps, or mask wipes

Good motion is layered: slow camera or world drift, medium typography or module movement, and small fast peripheral accents. Bad motion is a flat photo with a label, one large band covering the face, repeated template reskins, or a pile of unrelated UI components.

### Step 2.7: Treat ribbons and orbits as one motif

Text ribbons, orbit bands, and graphic rings are useful only when they serve the chosen visual world. Do not make every design a circular halo plus diagonal banner.

When the design uses words around a person:
- turn text into a physical banner, sash, tape strip, crown band, rail, ticker track, or ceremonial scroll
- place it with real depth, using behind/in-front layering, masks, perspective, blur, or `clip-path`
- keep face and expression clear; bands may cross shoulders, lower torso, edges, or negative space, but should not block the eyes or mouth
- keep halo-like and ceremonial bands slow enough to read
- use alternatives freely when they fit better: sliced photo panels, scrolling Swiss rows, theatrical arches, cyber grids, zine scraps, botanical ornament, chrome shards, waves, or editorial mastheads

### Step 3: Use a full-display, high-motion composition

The design should occupy the intended display surface with clear hierarchy and deliberate motion. Avoid narrow boxed artboards unless the user explicitly wants one.

For vertical social posts, Live Photos, Douyin/Xiaohongshu assets, or any 9:16 deliverable, build the artwork inside a fixed vertical stage centered in the browser:
- use a stage such as `width: min(100vw, 56.25vh); height: min(100vh, 177.7778vw); aspect-ratio: 9 / 16`
- keep all poster elements inside that stage, using stage-relative units, percentages, or container units
- let the outer body letterbox or center the stage; do not stretch the artwork to a landscape desktop browser viewport
- render and inspect the stage at `1080x1920` before exporting Live Photo assets

Preferred traits:
- full-bleed stage layout for the target format
- bold typography crossing the canvas
- multiple animated layers with deliberate motion
- kinetic text when it fits the direction: 3D text ribbons, orbiting rings, circular type, ticker strips, mirrored words, repeated slogans, or snapping editorial type
- style-specific motion such as sliced image panels, drifting ornamental frames, grid crawl, ticker rails, collage float, print offset, or theatrical parallax
- visible flicker, pulse, parallax, shimmer, wipe, ripple, or layer-swap accents
- a clear style world beyond "nice photo plus text"; every direction should have a distinct visual language
- strong visual density without becoming unreadable
- loop-safe motion if animation is present

Default motion bias:
- motion should read within the first second through layered world movement, not only a slow ambient drift
- use short 3-second loops for Live Photo exports, with clear changes in position, scale, color, flicker, or layer ordering
- make typography feel alive: words can slide, orbit, blink, repeat, or snap into new positions, but halo-like, crown-like, or ribbon-like text should move slowly
- keep the person stable and let the surrounding world carry most of the kinetic energy
- use slow, legible timing for ceremonial rings or ribbons when they appear; use other motion grammars when they fit the style better
- keep flicker localized and purposeful; avoid full-screen white strobe or rapid flashing that makes the subject hard to view
- if the first preview looks like a static framed photo with slight breathing, revise it toward stronger cutout-led compositing and motion
- if the first preview makes the person jitter, wobble, or rotate awkwardly, remove subject-layer motion and move the motion to text ribbons, graphic rings, typography, or background systems

Prefer plain HTML/CSS/JS unless the current project already uses another frontend stack.

Default creative bias:
- prefer bold but usable over safe but flat
- prefer a memorable silhouette and strong composition over generic balance
- prefer one clear "wow" move per direction: impossible scale, surreal depth, unexpected typography behavior, dramatic ornament, graphic rupture, or a style collision that still preserves the person
- do not average the design down just because a stranger option feels riskier

### Step 3.5: Treat the HTML as the final display artifact

The delivered HTML is the finished poster, banner, or motion graphic surface. It is not a design presentation, explainer page, moodboard, or case-study mockup.

Hard rules unless the user explicitly asks otherwise:
- do not place explanatory or process-oriented paragraphs on the canvas
- do not describe the art direction, editing choices, subject preservation, or design rationale inside the artwork
- do not add side panels, info cards, captions, or labels such as `self portrait`, `raw frame`, `sunset edit`, or other meta-description text
- only include on-canvas text that behaves like real display copy: the user's supplied line, a headline, a short slogan, a date/time stamp, or minimal decorative microtype
- if you are unsure whether a text block is ornamental or explanatory, remove it
- keep design explanation in the final chat response, never inside the delivered HTML

### Step 3.6: Generate real display copy, not image description

When the user does not provide copy, read [references/copy-style-systems.md](./references/copy-style-systems.md) and use it to select the closest copy direction before designing.

If the user provides exact copy, treat it as source-of-truth and design around it.

If the user does **not** provide copy, do not fill the canvas with literal description of the image, subject, outfit, lighting, or style. Do not write text that reads like an alt-text caption, mood summary, or visual annotation.

Hard rules for no-copy cases:
- do not describe what is visibly in the frame
- do not write style-summary lines such as `tree-shadow glamour`, `soft glare`, `white tee authority`, or similar image-explainer phrasing
- do not generate text that sounds like a prompt, tag list, metadata label, or editorial note
- do not use copy whose only function is to narrate the picture back to the viewer

Instead, infer **evocative display copy** from the image's implied energy, archetype, attitude, tension, humor, status, or mythology.

Generation rule:
- first try to map the image to one of the bundled copy-style templates
- if no template matches closely, generate original copy with the model's own judgment
- even in fallback mode, keep the generated copy inside the fixed copy-system format defined in [references/copy-style-systems.md](./references/copy-style-systems.md)

Preferred directions for generated copy:
- slogan-like
- campaign-like
- poster-like
- fashion/editorial-like
- mythic or character-branding-like
- emotionally suggestive rather than descriptive

When inventing copy, build it as a small system:
- one dominant headline, usually 1 to 4 words
- one secondary line, usually 2 to 8 words
- optional microtype fragments, tags, or ticker text that reinforce the same world

Internal rule:
- before placing text on the canvas, silently draft a full copy system using the reference format
- then place only the parts that improve the composition
- do not dump the whole copy system onto the design surface unless the layout genuinely needs it

Copy generation heuristics:
- derive text from the subject's implied role, not their visible inventory
- exaggerate aura, attitude, destiny, ritual, or legend
- prefer memorable language over accurate description
- if the image has humor or absurdity, lean into myth, swagger, or deadpan gravity rather than explaining the joke
- if the image contains an iconic or fictional character, translate that energy into a graphic persona or campaign voice instead of merely naming what is seen

Good default copy behaves like:
- a campaign title
- an album name
- a fashion spread line
- a pseudo-brand slogan
- a chapter heading from an imagined world

Bad default copy behaves like:
- a visual summary
- an art-direction explanation
- a style tag sentence
- a sentence listing objects or lighting conditions

### Step 4: Always produce two opposing directions

Generate two different outputs for every invocation. Do not return only one concept.

The two outputs should diverge meaningfully, for example:
- editorial luxury vs chaotic zine
- botanical ornament vs futuristic chrome
- ukiyo-e rhythm vs neon street signage
- baroque theatrical depth vs Swiss kinetic typography
- restrained cinematic negative space vs saturated visual overload

Do not overwrite `index.html`. Create new files named for the direction, for example:
- `william_morris_zinxpho.html`
- `acid_glitch_zinxpho.html`

If intermediate assets are generated, keep filenames theme-specific and non-destructive.

Prefer maximally contrasted directions over conservative variations. The second direction should feel like a real alternative worldview, not a mild restyling of the first.

### Step 4.5: Enforce batch-level visual diversity

When producing a batch, a social promo set, or more than two outputs from multiple photos, do not use one shared template with swapped colors, titles, and background textures. Batch outputs should feel like a curated set of different art directions, not a contact sheet of one system.

Before building a batch, create a private style allocation matrix. For every output, assign a distinct:
- composition skeleton
- subject scale and crop strategy
- typography architecture
- motion grammar
- depth/wraparound method
- supporting graphic language

Hard diversity rules:
- do not repeat the same centered halo, same diagonal banner, same subject placement, or same lower caption structure across most outputs
- do not let every image use the same "person in front of circular ring plus one text sash" formula
- do not make style names do the work; the canvas must visibly prove the style difference
- no single hero motif may dominate more than two outputs in the same batch unless the user explicitly requests a uniform campaign system
- if an output uses a 3D text ribbon, vary its structure across the batch: circular crown, vertical orbit, shoulder sash, foreground scroll, architectural type frame, or segmented graphic band
- vary motion by style: some designs can use ribbon orbit, others can use curtain reveal, wave procession, grid displacement, collage flips, chrome shard rotation, zine sticker jumps, or typographic camera moves
- keep the subject monumental in every direction, but do not solve monumentality with the same circle-and-banner layout every time
- do not reuse one background formula with different colors; each output needs its own depth stack and style-world layer

Good batch contrast looks like:
- one image built as a magazine masthead cover with huge cropped type
- one image built as a theatrical arch or stage with curtain motion
- one image built as a Swiss grid system with strict alignment and sliding modules
- one image built as an ukiyo-e wave composition where bands move like water
- one image built as chrome/glass relic architecture with reflective shards
- one image built as botanical manuscript ornament where leaves and text grow around the silhouette
- one image built as risograph or zine collage with torn-paper layers and print offsets

Batch QA:
- make a contact sheet before final export
- squint at the contact sheet: if the layouts read as the same poster with different skins, redesign at least half of them
- check whether the person, main type, primary graphic system, motion grammar, and background use different spatial relationships in each output
- verify that "explain" and "display" variants are not simply text-on/text-off versions of the same design unless the user asks for a matched pair
- if the user's feedback says the set feels similar, treat that as a design failure and revise the skill or generation plan before producing more assets

### Step 5: Deliver workspace-ready files

The final deliverable should be directly usable from the workspace.

Output contract:
- save both HTML files in the workspace
- keep all referenced assets in the workspace with relative paths
- do not leave project-required assets only under `$CODEX_HOME`
- do not depend on hidden temporary paths
- do not ship explanation panels or commentary text inside the visual unless the user explicitly requests that format

If the user did not specify a destination, create a small task-local output folder and place both directions there.

### Step 5.5: Package Live Photos when sharing matters

If the user asks for `Live 图`, `实况照片`, an image upload that still moves, Douyin/Xiaohongshu dynamic image sharing, or says the output needs to be easier to share, use the installed `livephoto` skill after the HTML directions are complete.

Default Live Photo contract:
- export one Apple Live Photo pair per direction: `direction.jpg` and `direction.mov`
- keep the original `direction.html` as the editable/source artifact
- use vertical `1080x1920`, 3 seconds, 30 fps unless the user asks otherwise
- use the HTML's own animation as the motion source, not a separately invented video unless the HTML is static
- make the JPG still frame work as a poster frame with the strongest readable moment
- validate each pair with `PHLivePhoto.request` via the `livephoto` workflow before calling it ready
- default final delivery is to import each validated pair into Mac Photos so each direction appears as one `实况` item there

Do not copy the `livephoto` implementation into this skill. Treat `livephoto` as the packaging/export layer and keep `zinxpho` focused on the visual directions.

### Step 6: Validate before presenting

Before handing off, verify:
- both directions exist as separate files
- both files load with valid relative asset references
- the authentic subject remains recognizable
- when the source image is person-led, the person is the first visual read and is not overpowered by text, background graphics, effects, or motion
- when the source image is person-led, the design uses a real foreground subject/cutout layer unless there is an explicit documented reason not to
- the two directions are materially different, not palette swaps
- the stronger motion and density do not make the design unusable
- motion is visibly kinetic within the first second, with layered world movement, typography movement, flicker/pulse accents, or style-specific layer changes rather than only slow drifting
- when the source image is person-led, the person feels sacred, epic, stable, and monumental rather than jittery, goofy, or randomly shaken
- the visual direction has a distinct style world and at least one surprising composition move, not only a framed photo with decorative text
- in a batch, the contact sheet passes the diversity test: different composition skeletons, not repeated reskins
- if vertical social output is intended, the HTML is actually framed as a 9:16 stage and does not stretch across a landscape browser viewport
- the canvas contains no explanatory copy, design notes, or self-referential labels unless explicitly requested
- if the user did not provide copy, the generated text reads like invented display language rather than a description of the image
- if extraction was required, the subject is actually isolated rather than merely cropped, and the edges are clean enough for compositing
- if Live Photos were requested, each direction has a validated `jpg`/`mov` pair and has been imported into Mac Photos as `实况`

If one direction is weaker, revise it before final delivery.

Do not treat intensity, asymmetry, maximalism, aggression, or visual weirdness as defects by themselves. Revise only when there is actual breakage, loss of identity, illegibility, weak differentiation, or an obvious drop in compositional quality.

## Aesthetic guidance

Do not collapse into one default style. Draw from a broad visual vocabulary when appropriate:
- pop art, manga/comic print, benday dots, sticker poster graphics, zine collage, and saturated flat-color systems
- Swiss graphic design
- William Morris and decorative floral systems
- Baroque theatrical depth
- Romantic lighting and atmosphere
- Ukiyo-e inspired flattening and rhythm
- futuristic glass, chrome, wireframe, and glitch systems

Pick directions that fit the photo and maximize contrast between the two outputs.

When strong local HTML references are available, mine their structural tricks: depth planes, photo-slice movement, oversized type tracks, foreground cutouts, ornamental frames, small metadata systems, and different animation tempos. Do not copy the same surface look unless the user explicitly asks for that style.

When in doubt, increase directional contrast rather than smoothing both concepts toward the middle.

## Final response requirements

The final response should include:
- the saved paths of both directions
- one short explanation of the art direction for each
- one short note about how the photo was preserved and integrated
- if Live Photos were requested, the saved `jpg`/`mov` paths, validation status, and whether the assets were imported into Mac Photos

## Failure handling

- If there is no usable image, ask for one.
- If image generation tools are unavailable, say so plainly and stop rather than pretending the workflow completed.
- Only specify an exact image model or provider when the user asks for one, or when a regression requires a temporary pin for reliability.
