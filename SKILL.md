---
name: zinxpho
description: Create two radically different high-energy web design directions from a user-provided photo. Use when the user invokes "zinxpho" or wants bold editorial art direction built around an authentic subject, with subject preservation, strong motion, dense typography, A/B HTML outputs, and optional Apple Live Photo / 实况图 packaging for easier Douyin/Xiaohongshu sharing.
---

# Zinxpho

## Overview

Use this skill when the user wants graphic-design-heavy, image-led output based on a real photo rather than a generic website or a fully regenerated portrait.

This skill is for:
- preserving the user's authentic subject
- isolating or cleaning the subject when needed
- integrating the subject into visually intense HTML/CSS compositions
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

If you need raster isolation, background removal, or photo transformation, use the installed `imagegen` skill. In current Codex, that means using the built-in `image_gen` tool through the `imagegen` workflow, not a nonexistent `generate_image` tool.

When the workflow needs true subject isolation, read [references/extraction-prompts.md](./references/extraction-prompts.md) and use its prompt skeleton or retry prompt rather than improvising loosely.

Do not pin the workflow to a specific image model version unless the user explicitly asks for one. By default, use the latest built-in image generation path exposed by the current Codex environment.

When the design needs the person separated from the source photo, treat this as a **true foreground extraction** task, not a loose reframing task.

When prompting image generation or editing:
- explicitly preserve identity
- explicitly forbid face and clothing changes
- prefer extraction, cleanup, and compositing over redraw
- ask for a transparent background first when the workflow needs a usable cutout
- ask for a neutral solid background only when transparency is unavailable or clearly inferior
- prefer the environment default/latest image model instead of hardcoding a dated model name

Hard extraction rules:
- do not accept a simple crop, zoom, or reframed portrait as a substitute for cutout
- preserve the full usable silhouette whenever possible, including hair, shoulders, arms, hands, clothing outline, and leg shape if visible
- keep edge fidelity high enough that the subject can be placed over a different background without an obvious box, matte, or leftover scene fragments
- remove original background content behind the subject instead of merely blurring or darkening it when the design needs true isolation

If a first extraction result behaves more like a crop than a cutout, iterate immediately with a stricter prompt focused on foreground separation, transparent background, and edge cleanup.

If the original photo is already compositionally strong, do not force extraction. You may keep the image mostly intact and use it as the core layer of the design.

### Step 2: Solve integration, not just cutout

After extraction, make the subject belong to the composition. Do not stop at dropping a raw cutout on top of a background.

Use CSS and composition techniques such as:
- aggressive color grading with `filter`
- masking with `mask-image`, gradients, blur falloff, or soft edge treatments
- layered glow, haze, and shadow systems
- perspective, depth, and scale contrasts
- intentional overlap between typography, shape systems, and the subject silhouette

When using heavy 3D transforms, do not rely on blend modes alone to hide extraction edges.

### Step 3: Use a full-canvas, high-motion composition

The design should occupy the full viewport with clear hierarchy and deliberate motion. Avoid narrow boxed artboards unless the user explicitly wants one.

Preferred traits:
- `100vw` by `100vh` layout
- bold typography crossing the canvas
- multiple animated layers
- strong visual density without becoming unreadable
- loop-safe motion if animation is present

Prefer plain HTML/CSS/JS unless the current project already uses another frontend stack.

Default creative bias:
- prefer bold but usable over safe but flat
- prefer a memorable silhouette and strong composition over generic balance
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
- elegant vs chaotic
- light vs dark
- classical ornament vs futuristic glitch
- restrained negative space vs saturated visual overload

Do not overwrite `index.html`. Create new files named for the direction, for example:
- `william_morris_zinxpho.html`
- `acid_glitch_zinxpho.html`

If intermediate assets are generated, keep filenames theme-specific and non-destructive.

Prefer maximally contrasted directions over conservative variations. The second direction should feel like a real alternative worldview, not a mild restyling of the first.

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
- do not send to iPhone by default; only share/AirDrop from Photos if the user explicitly asks for phone transfer

Do not copy the `livephoto` implementation into this skill. Treat `livephoto` as the packaging/export layer and keep `zinxpho` focused on the visual directions.

### Step 6: Validate before presenting

Before handing off, verify:
- both directions exist as separate files
- both files load with valid relative asset references
- the authentic subject remains recognizable
- the two directions are materially different, not palette swaps
- the stronger motion and density do not make the design unusable
- the canvas contains no explanatory copy, design notes, or self-referential labels unless explicitly requested
- if the user did not provide copy, the generated text reads like invented display language rather than a description of the image
- if extraction was required, the subject is actually isolated rather than merely cropped, and the edges are clean enough for compositing
- if Live Photos were requested, each direction has a validated `jpg`/`mov` pair and has been imported into Mac Photos as `实况`

If one direction is weaker, revise it before final delivery.

Do not treat intensity, asymmetry, maximalism, aggression, or visual weirdness as defects by themselves. Revise only when there is actual breakage, loss of identity, illegibility, weak differentiation, or an obvious drop in compositional quality.

## Aesthetic guidance

Do not collapse into one default style. Draw from a broad visual vocabulary when appropriate:
- Swiss graphic design
- William Morris and decorative floral systems
- Baroque theatrical depth
- Romantic lighting and atmosphere
- Ukiyo-e inspired flattening and rhythm
- futuristic glass, chrome, wireframe, and glitch systems

Pick directions that fit the photo and maximize contrast between the two outputs.

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
- Only specify an exact image model when the user asks for one, or when a regression requires a temporary pin for reliability.
