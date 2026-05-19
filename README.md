# Envision Lab — Design System

A boutique, government-appropriate visual system for **Envision Lab**, a Dubai-based, KHDA-approved learning design institute. The system produces technical proposals, training decks, curriculum materials, and one-pagers for UAE government, semi-government, and private-sector clients.

The brand reads as **boutique, considered, government-appropriate, warmly authoritative** — never corporate-blue, never Silicon Valley sleek, never academic-dry, never AI-default. The design language carries the same restraint as the writing: **direct, declarative, concrete, no marketing fluff.**

> **Constraint, in one line.** Three surfaces (navy · off-white · beige) used by zone. A serif header voice (Newsreader). DM Sans for body. JetBrains Mono for eyebrows. One warm gold accent + two restrained photographic accents drawn from the EL logo gradient. Generous whitespace. No drop shadows. No emoji. No clip-art icons. No AI-style imagery.

---

## What changed in v3 (May 2026)

This is a deliberate departure from the v2 "beige-only + gold" monoculture. The goals were:

1. **Stop looking AI-generated.** Models default to beige + amber + Fraunces + Lucide; this system actively pushes off all four.
2. **Introduce navy** as a contrast surface for openers, transitions, and statement slides — and as a restrained text accent.
3. **Reset the type stack.** Newsreader (serif) for headers, DM Sans for body, JetBrains Mono for eyebrows/metadata. Open Sans is retained ONLY for PowerPoint round-trip compatibility — never used in HTML.
4. **Sparingly add two photographic accents** (amber + peach) drawn from the EL logo gradient, used in motifs, charts, and a small number of intentional moments per slide.
5. **Demote beige to a contextual surface.** Default content lives on a subtler off-white. Beige carries thank-you, contact, transitions.
6. **Build a real motif library** — abstract architectural geometry, dune contours, editorial marks, orbital gradients — used by slide type.
7. **Bundle Tabler icons** (a curated 28) at brand stroke weight, recoloured to navy or gold. Document the CDN for edge cases.
8. **Add five new slide templates** for the section types the v2 deck was missing: Table of Contents, Roadmap, Timeline, Investment, Roles & Responsibilities.
9. **Rebuild the Thank-you slide** on a beige surface with three explorable variants (Tweaks toggle).
10. **Imagery has three sizes** — full-bleed (cover only), half-split (section openers), and small accent (everywhere else, *restrained*). Photos do not appear on content slides as primary visuals; the design carries itself.

The brand's spine — **warm-tinted neutrals, signature gold, restraint, the numeral-as-icon, the placeholder-as-visible-marker** — is preserved.

---

## Sources

This system is reconciled against the source PPTX files supplied by Tara:

- `uploads/EnvisionLab_Slide_Template_v3.pptx` — the 16-slide master deck (the v3 system's ground truth).
- `uploads/Emaar_Change_Management_Agility.pptx` — example deck showing the template in production use.
- `style-rules.md`, `uploads/differentiators.md`, `uploads/proposal-structures.md` — voice, content, and section-structure rules.

---

## Index — what's in this folder

| Path | What it is |
|---|---|
| `README.md` | You are here. Brand brief + content + visual + iconography fundamentals. |
| `style-rules.md` | Voice + content rules (banned words, anti-hallucination, UAE fit). Read this before writing copy. |
| `colors_and_type.css` | All color, type, geometry, and spacing tokens as CSS custom properties + base element styles. |
| `SKILL.md` | Agent-Skills compatible front-matter so this folder works in Claude Code. |
| `preview/` | Design-system tab cards (colors, type, motifs, icons, imagery, spacing, components, brand). |
| `slides/` | All 15 slide templates (cover, TOC, content, transitions, thank-you). |
| `documents/` | Long-form A4 document and one-pager samples. (Untouched in v3 — pending separate refresh.) |
| `assets/` | Logos, photography, motifs, icons. |
| `assets/photography/` | Five UAE-context training photos for half-split and accent use. |
| `assets/motifs/` | Thirteen reusable SVG motifs (architectural, topographic, editorial, orbital). |
| `assets/icons/` | Twenty-eight Tabler icons at brand stroke weight. |
| `fonts/` | Open Sans variable .ttfs — retained for PPTX round-trip only. |

---

## Content fundamentals

(Unchanged from v2 — voice, tone, banned vocabulary, placeholder-as-visible-marker. See `style-rules.md` for the full set.)

**Length discipline.**
- **Headlines:** ≤ 12 words.
- **Bullets:** ≤ 8 words.
- **Sublines:** single sentence, ≤ 12 words.

**Action verbs only** on outcomes: *analyse, design, build, evaluate, decide, present, draft, diagnose, prioritise, simulate, recommend, plan, lead*.

**Banned vocabulary** — do not render: *transformational, world-class, cutting-edge, robust, bespoke, holistic, leverage, empower, ignite, journey, immersive, dynamic, innovative (adj.), unlock, harness, elevate*.

**Placeholders are visible, not invented.** Render `[INSERT: client logo]` verbatim, in italic warm-mid (`--el-mid`).

**Punctuation.**
- Middle dot `·` for inline separators.
- En-dash for ranges.
- Right arrow `→` for stage progression.
- No exclamation points. No emoji. No emoticons.

---

## Visual foundations

### Three-zone background rule

This is the system's defining rule. Every slide picks one of three surfaces, and **the zone is determined by the slide's role in the deck**:

| Zone | Token | Hex | Where it appears |
|---|---|---|---|
| **Navy** | `--el-navy` | `#14233F` | Cover · Table of Contents · Section openers · Big-statement slides |
| **Off-white** | `--el-off-white` | `#FCFAF6` | **DEFAULT** content surface — at-a-glance, frameworks, programme arc/flow, simulation, outcomes, roadmap, timeline, investment, roles, all data-heavy slides |
| **Beige** | `--el-paper` | `#FAF6EE` | Thank-you · Contact · Transitional warm-paper slides between major sections |

**Cadence.** A typical proposal opens on navy (cover → TOC), descends into off-white for the body, lifts to navy at each section opener, and closes on beige (thank-you). The navy slides act as breaths between content-heavy stretches.

**Never** use beige for the cover or as the default content surface. **Never** use pure white. **Never** use navy for tabular or data-dense content (it kills legibility).

### Colour

**Type ladder (warm neutrals — no cool greys):** `#1E1D1C` → `#55524E` → `#777167` → `#B5AEA3` → `#D8D2C4`.

**On-navy type ladder:** `#F6F2EA` (warm off-white) → `#BDC4D3` → `#7E8AA1`.

**Surface ladder:** `#FCFAF6` (off-white, default) · `#FAF6EE` (beige) · `#14233F` (navy).

**Gold accent (retained):** `--el-gold #B9913F`. Used on type accents (section prefixes, slide numerals, small rules) on light surfaces. **`--el-gold-warm #E8B84C`** is the navy-surface variant of the gold.

**Two new logo-sourced accents** — used sparingly, **never near the logo**:
- `--el-amber #E8B84C` — yellow-amber pulled from the EL gradient
- `--el-peach #E89968` — peachy-orange pulled from the EL gradient

**Accent usage rule.** Reserve amber/peach for:
1. SVG motifs (orbital gradients, dune washes).
2. Data viz second/third colours.
3. One or two intentional moments per slide (a status pill, a chart segment, a small motif).

Cap at ~2 accent moments per slide. Do **not** use either accent on cover, thank-you, or any slide where the EL logo is prominent — the logo carries its own gradient and should stay the visual anchor.

**Anti-pattern:** any cool grey, pure white, blue-other-than-our-navy, green, red, purple. Hierarchy lives in type weight, scale, and whitespace.

### Typography

- **Header / display → Newsreader** (Google Fonts, Production Type). Editorial workhorse serif designed for screen, with weight and elegance. Used for titles, sublines, slide numerals, statement slides. Default is Regular (400); the Tweaks toggle exposes Italic Light (300), Semibold (600), and Bold (700) variants for deck authors to dial the temperature.
- **Body / UI → DM Sans** (Google Fonts, optical-size variable). Used for body copy, captions, in-card text, buttons.
- **Eyebrow / tag / metadata → JetBrains Mono** (Google Fonts). Used for section prefixes, all-caps eyebrows, metadata labels, technical numerals (dates, times, page nums, IDs).
- **Open Sans → legacy only.** Self-hosted variable .ttfs (`fonts/`) are retained so PPTX exports round-trip cleanly with the v2 template. Open Sans is NEVER invoked in HTML deliverables. If you find yourself reaching for it, you're looking at the legacy stack — switch back to the brand stack.

**Sizing — slide canvas (10" × 5.62"):**
- Eyebrow / mono label: 9pt
- Section prefix: 10pt
- Body: 11pt
- Subline: 13pt
- Caption: 8.5pt
- Title (serif): 34pt
- Big-statement (serif): 62pt
- Mega numeral (serif): 120pt
- Slide numeral (serif): 32pt

No body text below 8.5pt anywhere. No `font-weight: 100`. Slide titles are Newsreader **Regular**, not Light (light serifs read as anaemic at this scale).

### Iconography

**Tabler Icons** ([github.com/tabler/tabler-icons](https://github.com/tabler/tabler-icons), MIT). A curated 28-icon set lives in `assets/icons/` at brand stroke weight (2px, 24×24 viewBox, `currentColor`). Use them at 16–24px on light surfaces (recoloured to `--el-ink` or `--el-gold`) and on navy surfaces (recoloured to `--el-on-navy-1` or `--el-gold-warm`).

**For edge cases**, pull more from the Tabler CDN:
```html
<img src="https://unpkg.com/@tabler/icons/icons/outline/[name].svg" style="filter: …">
```
or inline the SVG and set `stroke="currentColor"`. **Never** mix icon families — pick one stroke style and hold the line.

**The numeral is still the primary icon.** Across cards (commitments, frameworks, stages, roles), a small two-digit gold numeral (`01`, `02`, `03`) in JetBrains Mono is the visual anchor. Tabler icons are secondary — a row of metadata, a single domain marker, a delta indicator. The numeral leads.

**Forbidden as before.** No Office defaults. No emoji. No Unicode pictographs (☎ ✉ ⚙). No icon-font glyphs. No clip-art.

### Motif library

Thirteen reusable SVG motifs in `assets/motifs/`, organised by slide type:

| Category | Motifs | Used on |
|---|---|---|
| **Architectural geometry** (mashrabiya) | `mashrabiya-star`, `mashrabiya-grid`, `arch-frame` | Section openers, TOC, thank-you (large-scale, low opacity) |
| **Topographic flow** (dune contours) | `contour-lines`, `dune-curves`, `ridge-line` | Roadmap, timeline, programme arc (mid-opacity, behind content) |
| **Editorial marks** | `asterisk`, `corner-arrow-down-left`, `corner-arrow-up-right`, `bracket-corners` | Content slides (small-scale, accent only) |
| **Orbital gradients** (atmosphere) | `orbital-navy`, `orbital-gold`, `orbital-peach` | Cover, big-statement, transitions (large blurred fills) |

Motifs use `currentColor` where possible so they take on the parent type colour. Render at low opacity (0.05–0.18 typical for backdrops) so they read as atmosphere, not decoration. **Never** place a motif inside a card or content block.

### Imagery

**Three patterns. Honour the size — over-large imagery breaks professional expectations for proposals.**

1. **Full-bleed with navy overlay** — Cover only. Photo + 90% navy gradient overlay + warm-cream serif title.
2. **Half-split** — Section openers and transitions only. Photo occupies 35–45% of the canvas; type and content sit on navy or off-white in the remaining ~60%.
3. **Small accent** — Everywhere else. Maximum 25% of canvas area. Used to anchor a single content slide (simulation, an outcomes slide, a transitional moment). Most content slides have **no imagery**; the design carries itself.

**Bank:** five UAE-context training photos in `assets/photography/` (coaching, leadership, hero-portrait, whiteboard, meeting), plus two textures (mashrabiya, dunes) used as motif sources, not as content photos. **Never use the textures as full photos** — they live as gradient/SVG inspiration.

**Hard ban.** No staged corporate stock, no handshakes, no AI-generated imagery, no glowing brains, no abstract networks.

### Geometry & layout

- **Slide canvas:** `10.00" × 5.62"` (960 × 540 px @ 96 dpi). Honour exactly.
- **Outer slide margin:** 0.4" (38 px).
- **Column grid:** 12 columns, 0.1" gutters, used loosely.
- **Vertical rhythm:** ~24–32 pt baseline.
- **Whitespace:** generous. Do not pack edge-to-edge.

### Borders, rules, and corner radii

- **Hairlines** are `1px solid var(--el-rule)` (`#D8D2C4`) on light, `1px solid var(--el-navy-rule)` on navy.
- **Gold rules** are `1.5px solid var(--el-gold)`. Used to mark major transitions or anchor a single key element.
- **Corner radii:** 0 default; up to 2px for inset panels. Never larger. No pills, capsules, or rounded buttons.

### Shadows, depth, blur, animation

**None.** No drop shadows, no glows, no 3D, no bevels. No frosted glass. No translucent overlays (other than navy/gold gradient washes inside motifs). No motion on slides intended for export; if motion appears in a prototype, restrict to 200–280 ms `ease-out` fades and short slides.

---

## Caveats and asks

1. **Newsreader, DM Sans, JetBrains Mono** are loaded from Google Fonts CDN. For offline export (government clients, air-gapped review), request `.ttf` bundles and we'll self-host. Open Sans is already self-hosted.
2. **No vector EL logo.** The rasterised PNG (`assets/envision-lab-logo.png`) is sufficient at on-screen and standard PPTX export resolution but will soften at large print sizes. Request original SVG/EPS/AI.
3. **Photography is a starter bank.** Five UAE-context images cover most section opener and accent needs. Real client engagements should commission proper photography of facilitators and (with consent) real participants.
4. **Sample-client logos are not bundled.** Client logos slot in per project via `[INSERT: client logo]` placeholders.
5. **Documents (`one-pager.html`, `proposal-long-form.html`) are still on the v2 system.** Refresh pending a separate pass.

**Bold ask:** original vector EL logo + a handful of real facilitator portraits + one or two real client lockups would let us swap the placeholders out at the lockup-card level so every new proposal starts fully branded.
