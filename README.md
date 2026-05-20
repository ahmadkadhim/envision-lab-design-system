# Envision Lab — Design System

A boutique, government-appropriate visual system for **Envision Lab**, a Dubai-based, KHDA-approved learning design institute. The system produces technical proposals, training decks, curriculum materials, and one-pagers for UAE government, semi-government, and private-sector clients.

The brand reads as **boutique, considered, government-appropriate, warmly authoritative** — never corporate-blue, never Silicon Valley sleek, never academic-dry, never AI-default. The design language carries the same restraint as the writing: **direct, declarative, concrete, no marketing fluff.**

> **Constraint, in one line.** Single warm cream surface (`#FEFCF7`) for every slide. A serif header voice (Source Serif 4). DM Sans for body. JetBrains Mono for eyebrows. One warm gold accent + two restrained accents (amber, peach) drawn from the EL logo gradient. Generous whitespace. No drop shadows. No emoji. No clip-art icons. No AI-style imagery.

---

## What changed in v5 (May 2026)

v5 builds on the single-surface system established in v4. Key changes:

1. **Restructured the programme section.** A generic "Programme" section opener now introduces the programme block (At a Glance → Programme Arc → Programme Flow → Frameworks → Simulation → Outcomes).
2. **Redesigned "Why Envision Lab."** Replaced left-border card panels with centred gradient icon-circle cards on off-white. Four SVG icons (pencil, play-circle, book, map-pin) sit inside warm gradient circles. DDDD framework and credentials ribbon flow without a divider.
3. **Genericised template content.** Delivery Team and Section Opener slides now use `[INSERT:]` placeholders throughout — no baked-in facilitator names or programme-specific copy.
4. **Added 6 new content slides** — Understanding Your Challenge, Programme Objective, Learning Experience & Delivery, Simulation Structure, Assessment & Impact, Delivery & Technology. Closes the gap with the proposal-gen skill's 16-slide content spec.
5. **Removed About Envision Lab slide** — redundant with Why Envision Lab.
6. **Moved Timeline after Thank You** (slide 19) as an optional appendix.
7. **19-slide deck** (up from 13 in v4, covering the full proposal-gen content spec plus TOC, section opener, and timeline).

### Earlier milestones

- **v4** — Single-surface pivot. Replaced the three-zone background rule (navy / off-white / beige) with warm cream throughout. Navy demoted to text/accent only. Swapped Newsreader for Source Serif 4. Added forest/sage chart accents. Introduced the gradient-wave background motif.
- **v3** — Introduced navy as a contrast surface, added the motif library, bundled Tabler icons, added five new slide templates (TOC, Roadmap, Timeline, Investment, Roles & Responsibilities).

---

## Sources

This system is reconciled against the source PPTX files supplied by Tara:

- `uploads/EnvisionLab_Slide_Template_v3.pptx` — the original 16-slide master deck.
- `uploads/Emaar_Change_Management_Agility.pptx` — example deck showing the template in production use.
- `style-rules.md`, `uploads/differentiators.md`, `uploads/proposal-structures.md` — voice, content, and section-structure rules.

---

## Index — what's in this folder

| Path | What it is |
|---|---|
| `README.md` | You are here. Brand brief + visual foundations. |
| `style-rules.md` | Voice + content rules (banned words, anti-hallucination, UAE fit) + visual guardrails. |
| `colors_and_type.css` | All color, type, geometry, and spacing tokens as CSS custom properties + base element styles. Single source of truth. |
| `slides/` | All 19 slide templates (cover, TOC, content, section openers, thank-you, timeline). |
| `slides/index.html` | Full deck overview — loads all 19 slides in a scrollable stack. |
| `documents/` | Long-form A4 document and one-pager samples. (Pending separate refresh.) |
| `assets/` | Logos, photography, motifs, icons, gradient-wave background. |
| `assets/photography/` | UAE-context training photos for cover and accent use. |
| `assets/motifs/` | Reusable SVG motifs (architectural, topographic, editorial, orbital). |
| `assets/icons/` | Tabler icons at brand stroke weight. |
| `fonts/` | Open Sans variable .ttfs — retained for PPTX round-trip only. |

---

## Slide templates (19)

| # | Template | File | Role |
|---|---|---|---|
| 01 | Cover | `cover.html` | Full-bleed photo + title + client logo placeholder |
| 02 | Table of Contents | `table-of-contents.html` | 14-item TOC with mashrabiya motif |
| 03 | Why Envision Lab | `why-envision-lab.html` | Four icon-circle differentiator cards + DDDD framework + credentials |
| 04 | Understanding Your Challenge | `understanding-your-challenge.html` | 3 pressure bullets + OUR RESPONSE box |
| 05 | Programme Objective | `programme-objective.html` | Objective statement + 3 capability bullets |
| 06 | Programme | `section-opener.html` | Section opener with arch-frame motif + mega numeral |
| 07 | At a Glance | `at-a-glance.html` | Five-column key facts grid |
| 08 | Programme Arc | `programme-arc.html` | Multi-day programme timeline |
| 09 | Programme Flow | `programme-flow.html` | Session-by-session breakdown |
| 10 | Learning Experience | `learning-experience.html` | 2×3 method card grid + design-standards footer ribbon |
| 11 | Frameworks | `frameworks.html` | Methodology cards |
| 12 | Simulation | `simulation.html` | Simulation description with photo accent |
| 13 | Simulation — Structure | `simulation-structure.html` | 2×2 block grid (do / gain / powerful / matters) |
| 14 | Learning Outcomes | `outcomes.html` | Numbered outcome items |
| 15 | Assessment & Impact | `assessment-impact.html` | 3-step measurement flow + Kirkpatrick 4-level legend |
| 16 | Delivery & Technology | `delivery-technology.html` | 4 blocks: format, TalentLMS, NeuroBoost-AI, materials |
| 17 | Delivery Team | `delivery-team.html` | Two facilitator cards with `[INSERT:]` placeholders |
| 18 | Thank You | `thank-you.html` | Contact info + credential logo badges + skyline photo |
| 19 | Timeline | `timeline.html` | Milestone timeline (appendix) |

---

## Content fundamentals

(See `style-rules.md` for the full set — voice, tone, banned vocabulary, placeholder-as-visible-marker.)

**Length discipline.**
- **Headlines:** ≤ 12 words.
- **Bullets:** ≤ 8 words.
- **Sublines:** single sentence, ≤ 12 words.

**Action verbs only** on outcomes: *analyse, design, build, evaluate, decide, present, draft, diagnose, prioritise, simulate, recommend, plan, lead*.

**Banned vocabulary** — do not render: *transformational, world-class, cutting-edge, robust, bespoke, holistic, leverage, empower, ignite, journey, immersive, dynamic, innovative (adj.), unlock, harness, elevate*.

**Placeholders are visible, not invented.** Render `[INSERT: client logo]` verbatim, styled with `.el-placeholder` (italic, warm-mid color). Never fill in data you don't have.

**Punctuation.**
- Middle dot `·` for inline separators.
- En-dash for ranges.
- Right arrow `→` for stage progression.
- No exclamation points. No emoji. No emoticons.

---

## Visual foundations

### Single-surface rule

Every slide uses **warm cream** (`#FEFCF7`, token `--el-cream`). Never pure white. Never a dark background surface.

Slide role (cover vs. content vs. thank-you) is communicated through **graphics, type treatment, and layout** — not background color. The amber-peach gradient wave (`slide-bg-gradient-waves.png`), photography, real logos, and type weight at scale carry the visual differentiation.

Within a slide, these tones are available for **card insets and panel differentiation** — never as full slide backgrounds:

| Token | Hex | Use |
|---|---|---|
| `--el-off-white-2` | `#F6F2EA` | Card backgrounds, inset panels |
| `--el-paper` | `#FAF6EE` | Subtle card inset |
| `--el-paper-tan` | `#F1EAD9` | Deeper card inset |
| `--el-paper-cream` | `#EFE7D6` | Deepest warm inset |

### Colour

**Type ladder (warm-tinted neutrals — no cool greys):**

| Token | Hex | Use |
|---|---|---|
| `--el-ink` | `#1E1D1C` | Primary text |
| `--el-body` | `#55524E` | Body copy |
| `--el-mid` | `#6D675D` | Metadata, captions |
| `--el-light` | `#B5AEA3` | Muted labels |
| `--el-rule` | `#CCC5B5` | Hairlines |

**Navy** (`--el-navy #14233F`) is a text and accent color — section prefixes, emphasis, small UI. **Never** a background surface.

**Gold accent (signature):** `--el-gold #B9913F`. Used on section prefixes, slide numerals, gold rules, single-point accents.

**Two logo-sourced accents** — used sparingly, **never near the logo**:
- `--el-amber #E8B84C` — yellow-amber from the EL gradient
- `--el-peach #E89968` — peachy-orange from the EL gradient

**Accent usage rule.** Reserve amber/peach for:
1. SVG motifs (orbital gradients, dune washes, gradient-wave backgrounds).
2. Data-viz second/third colours.
3. One or two intentional accent moments per slide.

Cap at ~2 accent moments per slide. Do **not** use either accent on any slide where the EL logo is prominent.

**Forest/sage greens** (`--el-forest`, `--el-sage` family) are reserved for charts and data-viz accents only.

**Anti-pattern:** any cool grey, pure white, blue-other-than-navy-accent, green outside of data-viz, red, purple.

### Typography

- **Header / display → Source Serif 4** (Adobe via Google Fonts). Clean bracketed serifs with an optical-size axis. Variable weight 200–900. Used for titles, sublines, slide numerals, statement slides.
- **Body / UI → DM Sans** (Google Fonts, optical-size variable). Used for body copy, captions, in-card text.
- **Eyebrow / tag / metadata → JetBrains Mono** (Google Fonts). Used for section prefixes, all-caps eyebrows, metadata labels, technical numerals.
- **Open Sans → legacy only.** Self-hosted variable .ttfs (`fonts/`) retained for PPTX round-trip. **Never invoked in HTML.**

**Sizing — slide canvas (960 × 540 px @ 96 dpi):**

| Role | Token | Size |
|---|---|---|
| Eyebrow / mono label | `--el-fs-eyebrow` | 12.5pt |
| Section prefix | `--el-fs-section-prefix` | 14pt |
| Body | `--el-fs-body` | 11pt |
| Subline | `--el-fs-subline` | 13pt |
| Caption | `--el-fs-caption` | 8.5pt |
| Slide title (serif) | `--el-fs-title` | 29pt |
| Big-statement (serif) | `--el-fs-statement` | 53pt |
| Mega numeral (serif) | `--el-fs-mega` | 120pt |
| Slide numeral (serif) | `--el-fs-slide-num` | 27pt |

No body text below 8.5pt anywhere. No `font-weight: 100`. Slide titles are Source Serif 4 **Regular**, not Light.

### Iconography

**Tabler Icons** ([github.com/tabler/tabler-icons](https://github.com/tabler/tabler-icons), MIT). A curated set lives in `assets/icons/` at brand stroke weight (2px, 24×24 viewBox, `currentColor`). Use them at 16–24px, recoloured to `--el-ink` or `--el-gold`.

**Gradient icon-circles** — used on the Why Envision Lab slide: 38px circles with `linear-gradient(135deg, #FDE7C8 0%, #F7CFC1 100%)` background, `#C5675F` icon stroke, 1px `#F7DDC9` border. Centres a 20px SVG icon.

**The numeral is still the primary icon.** Across cards (commitments, frameworks, stages, roles), a small two-digit gold numeral (`01`, `02`, `03`) in JetBrains Mono is the visual anchor. Tabler icons are secondary.

**Forbidden.** No Office defaults. No emoji. No Unicode pictographs. No clip-art. No mixing icon families.

### Motif library

SVG motifs in `assets/motifs/`, organised by slide type:

| Category | Used on |
|---|---|
| **Architectural geometry** (mashrabiya, arch-frame) | Section openers, TOC, thank-you |
| **Topographic flow** (dune contours) | Timeline, programme arc |
| **Editorial marks** (asterisk, corner arrows, brackets) | Content slides (small-scale, accent only) |
| **Orbital gradients** (atmosphere) | Cover, statement slides, transitions |

The **gradient-wave background** (`slide-bg-gradient-waves.png`) is the primary content-slide atmosphere. Applied at low opacity via CSS multi-background layering.

Motifs use `currentColor` where possible. Render at low opacity (0.05–0.18) so they read as atmosphere, not decoration. **Never** place a motif inside a card or content block.

### Imagery

**Three patterns. Honour the size — over-large imagery breaks professional expectations for proposals.**

1. **Full-bleed with overlay** — Cover only. Photo + cream gradient overlay + serif title.
2. **Half-split** — Thank-you and transitions only. Photo occupies 35–45% of canvas; cream gradient wash reveals the content side.
3. **Small accent** — Everywhere else. Maximum 25% of canvas area. Most content slides have **no imagery**; the design carries itself.

**Hard ban.** No staged corporate stock, no handshakes, no AI-generated imagery, no glowing brains, no abstract networks.

### Geometry & layout

- **Slide canvas:** 960 × 540 px @ 96 dpi. Honour exactly.
- **Outer slide margin:** ~56px (0.58") typical.
- **Vertical rhythm:** ~28pt baseline (`--el-baseline`).
- **Whitespace:** generous. Do not pack edge-to-edge.
- **Corner radii:** `--el-radius-md` (8px) for cards and image frames. Never larger than `--el-radius-lg` (12px). No pills or capsules.

### Borders and rules

- **Hairlines:** `1px solid var(--el-rule)` (`#CCC5B5`).
- **Gold rules:** `1.5px solid var(--el-gold)`. Used to mark major transitions.
- **Card borders:** `1px solid var(--el-peach-soft)` for facilitator/team cards. `1px solid var(--el-gold-25)` for dividers between columns.

### Shadows, depth, blur, animation

**None.** No drop shadows, no glows, no 3D, no bevels. No frosted glass. No motion on slides intended for export.

### Logo sourcing rule

Use real logos wherever possible — certifications (KHDA, Dubai SME, ISO marks), client logos, key frameworks (WHO ICOPE, ADDIE, Kirkpatrick). Real logos carry visual authority.

**If you cannot find a high-quality version:** use an `[INSERT:]` placeholder. A `[INSERT: KHDA logo — high-res PNG with transparent bg]` is better than a bad logo or a recreated mark.

---

## Caveats

1. **Source Serif 4, DM Sans, JetBrains Mono** are loaded from Google Fonts CDN. For offline export, request `.ttf` bundles and self-host.
2. **No vector EL logo.** The rasterised PNG (`assets/envision-lab-logo.png`) is sufficient at screen resolution but will soften at large print sizes. Request original SVG/EPS/AI.
3. **Photography is a starter bank.** Real client engagements should commission proper photography.
4. **Sample-client logos are not bundled.** Client logos slot in per project via `[INSERT: client logo]` placeholders.
5. **Documents (`one-pager.html`, `proposal-long-form.html`) are still on an earlier system.** Refresh pending a separate pass.
