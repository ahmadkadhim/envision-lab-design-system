---
name: envision-lab-design
description: Use this skill to generate well-branded interfaces and assets for Envision Lab, a Dubai-based KHDA-approved learning design institute. Produces technical proposals, training decks, curriculum materials, and one-pagers in the brand's single-surface warm cream visual system with Source Serif 4 headers, DM Sans body, restrained gold/amber/peach accents, and a curated motif + icon library. 19 slide templates. Suitable for production work or throwaway prototypes, mocks, and exploratory designs.
user-invocable: true
---

# Envision Lab — design skill (v5, May 2026)

This skill packages the complete Envision Lab brand design system: colour and typography tokens, slide and document layouts, voice and content rules, motif and icon libraries, and ready-made HTML samples.

## Where to start

1. **Read `README.md`** — full brand brief, content fundamentals, single-surface rule, 19-slide template catalog, motif and imagery rules.
2. **Read `style-rules.md`** — voice + content rules (banned words, anti-hallucination, UAE fit) + visual guardrails. Read before writing any copy.
3. **Open `colors_and_type.css`** — single source of truth for colour and type tokens. Always link this file or copy its `:root` block; never invent new colours or sizes.
4. **Browse `slides/` and `documents/`** for working examples of every layout pattern in the system.

## Core constraints (do not violate)

- **Single-surface rule.** Warm cream (`#FEFCF7`, `--el-cream`) for every slide — cover, content, transitions, thank-you. Slide role is communicated through graphics, type treatment, and layout — never through background colour changes. Never pure white. Never a dark background surface.
- **Card inset tones.** `--el-off-white-2` (#F6F2EA), `--el-paper` (#FAF6EE), `--el-paper-tan` (#F1EAD9) are available for card backgrounds and panel differentiation within a slide — never as full slide backgrounds.
- **Type stack.** Source Serif 4 (header/display, serif), DM Sans (body/UI), JetBrains Mono (eyebrows, metadata, technical numerals). Open Sans is retained ONLY for PowerPoint round-trip compatibility — never used in HTML.
- **Gold + two restrained accents.** Gold (`#B9913F`) is the signature accent. Amber (`#E8B84C`) and peach (`#E89968`) are sourced from the EL logo gradient and used sparingly in motifs and one or two intentional accent moments per slide. **Never** place amber or peach adjacent to the EL logo.
- **Navy is text/accent only.** Navy (`#14233F`) is used for section prefixes, emphasis, and small UI. Never as a background surface.
- **No second hue.** No blue (other than navy accent), green (except chart data-viz), red, purple — even for chart differentiation. Use gold tints + navy + warm-grey ladder.
- **Slide canvas is 960 × 540 px** (10" × 5.62" @ 96 dpi). Honour exactly.
- **No drop shadows, no rounded pills, no 3D.** Hierarchy comes from type weight, scale, and whitespace. Corner radii: `--el-radius-md` (8px) for cards; never larger than `--el-radius-lg` (12px).
- **Slide titles are Source Serif 4 Regular** (400), not Light. Light serifs read anaemic at this scale.
- **Banned vocabulary** — see `style-rules.md`. Flag and ask if supplied content uses these.
- **Headlines ≤ 12 words. Bullets ≤ 8 words.** Sentence case for everything except section prefixes and small all-caps labels.
- **Render `[INSERT: ...]` placeholders verbatim** in italic warm-mid (`--el-fg-3`). Never invent client names, statistics, or facilitator details.
- **Imagery is restrained.** Full-bleed only on cover. Half-split only on thank-you/transitions. Everywhere else, photos are small accents (max 25% of canvas) or absent.
- **Tabler icons only** when icons are needed. Curated set in `assets/icons/`. Pull more from the Tabler CDN for edge cases. No clip-art, no emoji, no Unicode pictographs, no AI-style imagery.
- **Brand-permanent text** (methodology footer ribbons, Kirkpatrick levels, NeuroBoost-AI compliance, card titles on Learning Experience) must be rendered verbatim. Per-programme content goes in `[INSERT:]` placeholders.

## Slide templates (19)

See `README.md` for the full catalog with file names and roles. The templates span: Cover, Table of Contents, Why Envision Lab, Understanding Your Challenge, Programme Objective, Programme (section opener), At a Glance, Programme Arc, Programme Flow, Learning Experience & Delivery, Frameworks, Simulation (Scenario), Simulation (Structure), Learning Outcomes, Assessment & Impact, Delivery & Technology, Delivery Team, Thank You, Timeline.

Key layout patterns across slides:
- **Card grids** (4-col, 2×3, 2×2) with `var(--el-off-white-2)` backgrounds
- **Gradient icon-circles** (38px, peach gradient, coral stroke) on Why Envision Lab
- **Numbered items** (large gold serif numeral + text) on Learning Outcomes
- **Column data** (border-left separators, mono labels) on At a Glance and Assessment steps
- **Bullet lists** (6px gold dot + 12px gap + sans text) across content slides
- **Step flows** (numbered steps with separator lines) on Assessment & Impact
- **Block grids** (2×2 labeled blocks) on Simulation Structure and Delivery & Technology
- **Footer ribbon** (brand-permanent text, smaller type, rule-top) on Learning Experience

## How to use this skill

If the user asks for a deliverable (deck, document, one-pager, web page, mock, prototype):

1. Every slide uses cream (`--el-cream`). Differentiate slides through layout, type scale, motifs, and photography — not background colour.
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
