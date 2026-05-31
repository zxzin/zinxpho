# Copy Style Systems

Use this file only when the user did not provide exact copy and the design needs display text.

The goal is not to describe the image. The goal is to invent a small verbal world that makes the image feel like a campaign, poster, editorial spread, myth, or character launch.

## Copy decision authority

Before writing or placing copy, decide the user's authority level.

### Level 1: Locked copy

Use when the user provides exact wording, a slogan, a product name, a brand line, a title, a CTA, or text they clearly want used.

User authority is highest. The agent may:
- split lines
- repeat fragments as ticker or microtype
- change case when the alphabet supports it
- adjust punctuation only when it is purely typographic
- translate only when the user asks for translation

The agent must not:
- rewrite the main meaning
- replace names, slogans, or product terms
- invent a better headline instead of the user's wording
- hide the user's required text in tiny type
- turn exact copy into vague decorative fragments
- let a foreground person, 3D transform, animated ribbon, or crop-safe margin hide required text in the rendered frame

If exact copy is too long or visually weak, keep it but solve with hierarchy: dominant excerpt, secondary line, ticker fragments, or a companion short lockup. Mention the tradeoff in the final response if important.

### Level 2: Guided copy

Use when the user gives a theme, keywords, mood, selling points, audience, platform, product feature, or partial text, but not final wording.

The user controls:
- must-use words
- language or bilingual direction
- tone boundaries
- claims that must be true
- forbidden words or topics

The agent controls:
- headline invention
- secondary line
- microtype and ticker fragments
- hierarchy and repetition
- how much copy appears on each visual

Keep must-use words visible enough to matter. Do not bury the user's key phrase in decorative microtype unless it is also present elsewhere.

### Level 3: Agent-led copy

Use when the user gives no copy and only provides an image or a visual direction.

The agent should generate a complete copy system using the templates below. The generated copy should feel like a campaign, editorial title, character launch, mythic label, or visual identity system.

The user still has final revision authority, but the first pass should not require the user to write the copy.

### Level 4: Promo or explain copy

Use when the output promotes Zinxpho itself, explains what the skill does, compares before/after behavior, or is part of a social launch set.

In this mode, plan two copy roles:
- explain variant: can contain value-prop copy, short feature claims, and "how it works" language
- display variant: should use normal poster copy and show the effect without sounding like a tutorial

Do not make both variants the same design with text turned on or off. The explain version can be more legible and instructional; the display version should be more desirable as a standalone post.

## Minimum copy brief

Do not ask the user a long intake form. If the work cannot proceed safely without copy context, ask only the missing critical item.

Useful fields when available:
- exact required text
- language: Chinese, English, bilingual, or platform-specific
- audience and platform
- tone: luxury, mythic, funny, pop, technical, intimate, aggressive, soft
- must-use or banned words
- claims that need to be accurate
- CTA, if any

If the user does not provide these, infer them from the image and task.

## Selection rule

1. Pick the closest style template below if one clearly matches the image's implied energy.
2. If none matches well, create a fresh copy system using the fixed fallback format at the end of this file.
3. Even when using a template, adapt the wording to the image. Do not blindly paste examples.

## Global hard rules

- Never describe visible objects back to the viewer.
- Never write the copy like an alt-text, moodboard note, metadata label, or image prompt.
- Prefer identity, aura, myth, tension, swagger, ritual, humor, or destiny over literal description.
- Headline copy should usually feel usable as a poster title, campaign lockup, album title, or character-branding device.
- Secondary copy should support the world, not explain the image.
- Microtype should feel like signal, tags, codes, fragments, or campaign debris.
- Copy must fit the layout. If text is clipped, too small, too long, edge-cropped, or competing with the face, revise the copy or hierarchy rather than forcing it into the design.
- Do not use false claims. For feature or product copy, keep claims short, true, and visually useful.
- Avoid generic AI-marketing phrases such as "unlock creativity", "stunning visuals", or "next-level design" unless the user explicitly wants that tone.

## Fixed copy-system format

When inventing copy, silently draft it in this format first:

```text
COPY SYSTEM
Style family: <template name or custom>
Headline: <1 to 4 words>
Secondary line: <2 to 8 words>
Microtype fragments:
- <2 to 5 words>
- <2 to 5 words>
- <2 to 5 words>
Ticker fragments:
- <2 to 4 words>
- <2 to 4 words>
- <2 to 4 words>
- <2 to 4 words>
Copy authority: <locked/guided/agent-led/promo>
Must-use text: <none or exact phrases>
Do-not-use text: <none or exact phrases>
```

Do not show this scaffold to the user unless they explicitly ask for the copy plan. Use it internally, then place only the strongest parts on the canvas.

## Placement rules

Assign each line a visual job:
- headline: first read, large, short, memorable
- secondary line: supports the world or value proposition
- microtype: texture, codes, issue labels, metadata, seals, small fragments
- ticker or rail: repeated rhythm, movement, border language
- badge or stamp: compact status, edition, issue, number, claim, or CTA

For Chinese copy, prefer concise poster phrases over full explanatory sentences. If the line needs to explain process, move that explanation to the final chat response and keep the canvas line short.

Do not default to bordered boxes for captions, labels, or stamps. Integrate copy with typography: vertical rules, soft blur backing, baseline microtype, rail text, mask-revealed type, tone-on-tone placement, or type that belongs to the depth stack.

Keep copy away from eyes and mouth unless the style intentionally creates a face-safe overlap. On social posts, keep important copy away from extreme bottom and side edges.

When bilingual copy is useful, do not translate every line. Use one language for the main emotional read and the other for microtype, subtitle, or ticker rhythm.

## Promo copy for Zinxpho

When promoting Zinxpho, avoid explaining too much inside the artwork. Prefer compact claims that map to visible output.

Good claim directions:
- real photo preserved
- cutout-led design
- motion poster
- live photo ready
- two visual directions
- HTML as source
- subject first

Bad claim directions:
- vague "AI makes it better"
- long workflow explanations
- model or provider names
- promises about platforms that were not validated
- paragraphs pasted into the poster

For a launch set, use paired variants:
- explain copy example: `先把人物立住，再让版式、切片和文字围绕她运动。`
- display copy example: `日常封神`

The exact words should change per image and style; the structure should remain.

## Template 1: Mythic Monument

Use when the image feels statuesque, iconic, ceremonial, slow, heavy, or legendary.

Signal words:
- monument
- throne
- reign
- dynasty
- rite
- crown
- relic
- empire

Headline pattern:
- `<Noun> <Power Word>`
- `<Place> <Myth Word>`

Secondary pattern:
- short phrase suggesting power, ritual, permanence, or fate

Good examples:
- LAWN THRONE
- STATIC DYNASTY
- AFTER THE CROWN

Avoid:
- literal scenery description
- jokey copy that breaks the monument tone

## Template 2: Editorial Luxury

Use when the image feels elegant, fashion-coded, poised, polished, cool, or expensive.

Signal words:
- edition
- house
- line
- reserve
- state
- archive
- emblem
- issue

Headline pattern:
- `<Surname/Persona> <Mode>`
- `<Word> <Edition>`

Secondary pattern:
- restrained line with confidence, poise, or social control

Good examples:
- SUBURBAN EDITION
- PRIVATE MODE
- SILENT RESERVE

Avoid:
- over-explaining
- technical words
- goofy myth language if the image wants polish

## Template 3: Deadpan Hero

Use when the image is funny, absurd, awkward, or iconic in a low-key way, but should still feel composed.

Signal words:
- local
- civilian
- mode
- shift
- state
- regular
- standard
- supreme

Headline pattern:
- `<Ordinary Word> <Grand Word>`
- `<Mundane Word> <Hero Word>`

Secondary pattern:
- calm, understated line that treats absurdity like official business

Good examples:
- REGULAR SUPREME
- CIVIC GLORY
- LOCAL LEGEND

Avoid:
- explaining the joke
- meme captions
- direct references to "funny" or "absurd"

## Template 4: Campaign Power

Use when the image feels assertive, dominant, punchy, slogan-friendly, or suited for brand launch energy.

Signal words:
- power
- command
- strike
- rise
- force
- unit
- campaign
- motion

Headline pattern:
- `<Verb/Noun> <Power Noun>`
- short imperative or statement-like lockup

Secondary pattern:
- compressed slogan with momentum and command

Good examples:
- HOLD THE FRAME
- STILL RUNS DEEP
- POWER IN PLAIN SIGHT

Avoid:
- ornamental softness if the image wants punch
- descriptive taglines

## Template 5: Nocturnal Cult

Use when the image feels eerie, sacred, shadowed, secretive, or like a coded underground poster.

Signal words:
- chapel
- signal
- rite
- dusk
- hush
- order
- sleep
- omen

Headline pattern:
- `<Dark Noun> <Signal Word>`
- `<Ritual Word> <Place Word>`

Secondary pattern:
- murmured, suggestive line implying secrecy or prophecy

Good examples:
- SHADE ORDER
- SLEEP SIGNAL
- GARDEN OMEN

Avoid:
- cheerful brand voice
- direct horror clichés unless the image really needs them

## Template 6: Pop Icon Launch

Use when the image feels bold, colorful, memeable, character-forward, youth-coded, or like a launch card for a pop persona.

Signal words:
- icon
- mode
- star
- club
- season
- fever
- signal
- deluxe

Headline pattern:
- `<Persona Word> <Mode>`
- `<Word> <Deluxe/Season/Signal>`

Secondary pattern:
- high-confidence line with attitude or social magnetism

Good examples:
- BACKYARD ICON
- WEEKEND SIGNAL
- STAR MODE ONLY

Avoid:
- stiff luxury language
- moody myth language if the image wants direct pop energy

## Fallback generation rule

If none of the above templates matches:

1. Decide the image's strongest abstract energy in one line:
- sovereign
- feral
- deadpan
- devotional
- glamorous
- comic-grand
- spectral
- militant
- tender-epic

2. Generate a copy system using the fixed format:
- Headline: 1 to 4 words, highly memorable
- Secondary line: 2 to 8 words, atmosphere not explanation
- Microtype fragments: 3 short fragments that reinforce the world
- Ticker fragments: 4 short fragments that can repeat as border/ticker language

3. Check the result:
- Would this still work if the viewer never saw the original image description?
- Does it feel like a title system rather than a note?
- Is it stronger than simply narrating the frame?

If the answer is no, rewrite.
