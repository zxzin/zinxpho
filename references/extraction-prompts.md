# Extraction Prompts

Use this file only when the workflow needs a real person cutout rather than a reframed source image.

## Goal

Produce a true usable foreground extraction:
- the person is separated from the original background
- edges are clean enough for compositing
- the result behaves like a cutout, not a crop

## Hard rules

- Ask for transparent background first when possible.
- If transparency is not available, ask for a pure solid neutral background that can be masked cleanly later.
- Explicitly say this is not a crop, zoom, or reframing request.
- Explicitly preserve identity, pose, clothing, and silhouette.
- Explicitly remove background remnants around hair, shoulders, arms, and clothing edges.

## Prompt skeleton

```text
Edit this image as a true foreground extraction task, not a crop or reframing task.
Keep the subject's real face, hair, body proportions, pose, expression, and clothing unchanged.
Remove the original background and isolate the subject as a clean full cutout.
Preserve the usable silhouette, including hair edges, shoulders, arms, hands, clothing outline, and lower body where visible.
Do not zoom in, crop tighter, or replace cutout quality with a portrait-style reframing.
Output the subject on a transparent background.
If transparent output is unavailable, place the subject on a pure solid background with no shadows, scenery, or leftover fragments.
```

## Stricter retry prompt

Use this when the first result looks like a crop, partial silhouette, or background-muted portrait rather than a cutout.

```text
Retry as strict background extraction.
This must be a real cutout, not a portrait crop, zoom, vignette, or blurred-background image.
Keep the entire visible subject intact and remove the source environment behind them.
Do not trim the silhouette.
Do not leave tree edges, wall edges, ground patches, glow boxes, or blurred scene residue around the body.
Return a clean isolated subject suitable for compositing onto a new design background.
```

## Failure signs

Treat these as failed extraction:
- the result is just a tighter crop
- the old background is still faintly visible
- the subject is sitting inside a soft rectangle or matte box
- limbs, hair, or clothing edges are missing for no compositional reason
- the model zoomed to the face instead of isolating the full figure

If any of these happen, retry before building the design around the asset.
