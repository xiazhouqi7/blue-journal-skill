---
name: xiazhouqi-blue-journal-skill
description: Create or restyle mobile-first HTML webpages, tutorial pages, and visual guides in the Xiazhouqi Blue Journal style, using airy sky-blue and milk-white backgrounds, rounded paper cards, sticky notes, handwritten marks, screenshots, and poster-like information hierarchy. Use when the user asks for “蓝色手帐网页”, “蓝色手帐风格”, or “下周七蓝色手帐”. Do not use for ordinary corporate dashboards, full-bleed photo covers, or the champagne-gold rounded-card system.
---

# Xiazhouqi Blue Journal Web

Build a real, responsive webpage that carries the approved Blue Journal visual language. Do not return a flattened screenshot when the user asks for HTML. Keep text selectable, layout editable, and supplied screenshots faithful.

Before designing, read [references/style-guide.md](references/style-guide.md). For layout work, inspect [examples/blue-journal-web-template.html](examples/blue-journal-web-template.html) and the three reference images named below. Treat the HTML as the implementation baseline and the images as the visual truth.

## Choose the page mode

- Use **stacked poster sections** for tutorial steps, style boards, knowledge cards, and pages intended to feel like a sequence of 3:4 graphics.
- Use a **continuous scrolling page** for longer articles or tools, while preserving the same paper cards, handwritten annotations, color balance, and generous spacing.
- Follow the user's requested ratio or platform when specified. Otherwise, use 3:4 for poster sections and a fluid mobile-first layout for ordinary webpages.

## Core visual language

- Use sky blue, mist blue, milk white, pale cream, and blue-gray. Warm yellow, pale green, or soft orange are accents only.
- Combine a soft sky gradient with white haze, paper grain, and restrained warm light. Avoid a flat gray background.
- Build information from rounded translucent paper cards, small labels, sticky notes, tape, Polaroids, hand-drawn arrows, wavy underlines, check boxes, stars, and tiny flowers.
- Establish one clear reading path: category label or number, main title, short explanation, main screenshot or content card, then one closing note.
- Let one screenshot, device, photo, or information group lead each section. Decorative elements must support the reading path.
- Prefer natural handwriting or rounded editorial type. Avoid supermarket-poster lettering, heavy commercial display fonts, neon effects, and thick black outlines.

## Web implementation invariants

- Include a correct viewport meta tag and design mobile-first.
- The page must never move sideways on a phone. Constrain the root, body, main container, images, transforms, and absolutely positioned decorations to the viewport or their clipped poster canvas.
- Set images to `max-width: 100%`; keep transformed decoration inside an `overflow: hidden` or `overflow: clip` parent.
- For poster canvases, use `aspect-ratio: 3 / 4`, `container-type: inline-size`, and container query units so typography and decoration scale together.
- Do not make essential content depend on JavaScript. Content is visible by default; animation may be added only as progressive enhancement.
- Preserve readable contrast, semantic headings, useful alternative text, keyboard access, and reduced-motion behavior when interaction exists.
- Check at approximately 375–390 px wide and at desktop width. Confirm `scrollWidth` does not exceed `clientWidth`.

## Content fidelity

- Preserve the user's wording, screenshots, interface paths, prices, and factual details.
- Do not recreate an operating-system screen from memory when a supplied screenshot can be cropped and placed faithfully.
- Blur or cover private identifiers before using screenshots in a public result.
- Do not copy the App Store subject matter from the examples into unrelated pages. Copy the visual system, not the example topic.
- Do not add account names, “小岛周末”, watermarks, marketing buttons, generic navigation, or explanatory design labels unless requested.

## Working method

1. Inspect every supplied image and determine the required page mode, content hierarchy, and dominant visual.
2. Map the content to the closest approved reference composition.
3. Implement the semantic HTML and the full visual system, using the template as a structural reference rather than copying irrelevant text.
4. Check mobile containment before polishing. Fix horizontal overflow at the source instead of hiding broken layout with arbitrary negative margins.
5. Review title hierarchy, screenshot clarity, color cleanliness, edge safety, and decorative restraint.
6. Deliver the complete HTML and supporting assets requested by the user.

## Approved references

- `examples/blue-journal-style-preview.jpeg`: complete vocabulary, palette, element density, phone mockup, and multi-card balance.
- `examples/reference-settings-path.jpeg`: tutorial step composition, numbered heading, arrows, path card, device placement, sticky note, and speech bubble.
- `examples/reference-app-store-cover.jpeg`: tutorial cover composition, headline hierarchy, marker strokes, information card, screenshot, and bottom sticky note.
- `examples/blue-journal-web-template.html`: responsive three-canvas implementation containing all approved elements and the mobile overflow safeguards.

## Final check

- Does the first screen immediately feel like the approved Blue Journal references?
- Is the title the clearest element without looking commercial or loud?
- Are blue and milk white dominant, with warm colors used sparingly?
- Are the paper, tape, handwriting, and doodles visible but not cluttered?
- Is every important screenshot legible and factually faithful?
- Can the page be scrolled vertically on a phone without any horizontal movement?
- Does the page remain useful when JavaScript is unavailable?
