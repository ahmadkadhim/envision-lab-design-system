---
name: envision-lab-design
description: Use this skill to generate well-branded interfaces and assets for Envision Lab, a Dubai-based KHDA-approved learning design institute. Produces technical proposals, training decks, curriculum materials, and one-pagers in the brand's three-zone (navy · off-white · beige) visual system with serif headers, restrained accents, and a curated motif + icon library. Suitable for production work or throwaway prototypes, mocks, and exploratory designs.
user-invocable: true
---

# Envision Lab — design skill (v3, May 2026)

This skill packages the complete Envision Lab brand design system: colour and typography tokens, slide and document layouts, voice and content rules, motif and icon libraries, and ready-made HTML samples.

## Where to start

1. **Read `README.md`** — full brand brief, content fundamentals, three-zone background rule, motif and imagery rules.
2. **Read `style-rules.md`** — voice + content rules (banned words, anti-hallucination, UAE fit). Read before writing any copy.
3. **Open `colors_and_type.css`** — single source of truth for colour and type tokens. Always link this file or copy its `:root` block; never invent new colours or sizes.
4. **Browse `slides/`, `documents/`, and `preview/`** for working examples of every layout pattern in the system.

## Core constraints (do not violate)

- **Three-zone background rule.** Navy (`#14233F`) for cover, TOC, section openers, statement slides. Off-white (`#FCFAF6`) as the DEFAULT for all content. Beige (`#FAF6EE`) for thank-you, contact, transitions. Never pure white. Never invent a fourth surface.
- **Type stack.** Newsreader (header/display, serif), DM Sans (body/UI), JetBrains Mono (eyebrows, metadata, technical numerals). Open Sans is retained ONLY for PowerPoint round-trip compatibility — never used in HTML.
- **Gold + two restrained accents.** Gold (`#B9913F`) is the signature accent on light, gold-warm (`#E8B84C`) on navy. Amber (`#E8B84C`) and peach (`#E89968`) are sourced from the EL logo gradient and used sparingly in motifs and one or two intentional accent moments per slide. **Never** place amber or peach adjacent to the EL logo.
- **No second hue.** No blue (other than our navy), green, red, purple — even for chart differentiation. Use gold tints + navy + warm-grey ladder.
- **Slide canvas is `10.00" × 5.62"`** (960 × 540 px @ 96 dpi). Honour exactly.
- **No drop shadows, no gradients (other than motifs and navy overlays), no 3D, no rounded pills.** Hierarchy comes from type weight, scale, and whitespace.
- **Slide titles are Newsreader Regular** (400), not Light. Light serifs read anaemic at this scale.
- **Banned vocabulary** — see `style-rules.md`. Flag and ask if supplied content uses these.
- **Headlines ≤ 12 words. Bullets ≤ 8 words.** Sentence case for everything except section prefixes and small all-caps labels.
- **Render `[INSERT: ...]` placeholders verbatim** in italic warm-mid. Never invent client names, statistics, or facilitator details.
- **Imagery is restrained.** Full-bleed only on cover. Half-split only on section openers. Everywhere else, photos are small accents (max 25% of canvas) or absent.
- **Tabler icons only** when icons are needed. Curated set in `assets/icons/`. Pull more from the Tabler CDN for edge cases. No clip-art, no emoji, no Unicode pictographs, no AI-style imagery.

## How to use this skill

If the user asks for a deliverable (deck, document, one-pager, web page, mock, prototype):

1. Decide the zone for each slide based on its role (cover/TOC/opener → navy; content → off-white; thank-you → beige).
2. Produce **static HTML** that links `colors_and_type.css` and follows the slide patterns in `slides/`.
3. Copy the visual assets you need from `assets/` into the deliverable folder rather than referencing across the skill.
4. Use the curated icon set in `assets/icons/` and motifs in `assets/motifs/`. Don't invent new ones unless asked.
5. Surface every `[INSERT: ...]` placeholder visibly so the user can see exactly what's missing.

If the user invokes this skill with no specific brief, ask:

1. What are we producing — slide deck, long-form proposal, one-pager, web page, something else?
2. Who is the audience — UAE government, semi-government, private sector, internal?
3. What is the programme or topic?
4. Is the content supplied, or should the agent flag content gaps?
5. Are any source assets (logos, photography, custom illustrations) available?

Then produce the artefact, surfacing every `[INSERT: ...]` placeholder visibly.
