# Style & Quality Rules

**Source:** Tara's existing system prompt + Freelancer Brief. Treat as strict.

## Tone

- Direct, declarative, professional. Government-appropriate but not stuffy.
- Concrete over abstract. If you write a claim, attach a specific example or mechanism.
- Active voice. One main idea per sentence.
- Vary sentence length. Avoid run-ons.
- No marketing language. No salesmanship.

## Banned words (never use)

transformational · transformative · world-class · cutting-edge · revolutionary · next-level · best-in-class · bespoke · holistic · synergy · leverage · unleash · empower · ignite · journey · robust · impactful · seamlessly · unparalleled · dynamic · innovative (as adjective) · unlock · harness · elevate · immersive

## Banned intensifiers without numbers

deeply · truly · highly · extremely · incredibly · significantly

If a number can support the claim, use it. Otherwise drop the intensifier.

## Banned sourcing patterns

- "Research shows" / "studies prove" without a named source
- "Industry experts agree"
- "Best practice indicates" without citation

If a source is not provided in the input, do not write a research claim.

## Anti-hallucination rules (strict)

Never invent any of the following:

- Client names, logos, or past engagements not provided in the input
- Statistics, percentages, ROI figures, or research findings
- Facilitator names, credentials, certifications, or biographies
- Awards, accreditations, or partnerships
- Specific case studies or anecdotes

When the input lacks data you would normally include, write a placeholder in this exact format: `[INSERT: brief description of what is needed]`. Do not write plausible-sounding filler in place of real data.

If asked for a fact about Envision Lab not in `envision-lab-profile.md`, respond with `[INSERT: confirm with team]`.

## Methodology claims

Every methodology claim must be paired with a concrete example of what it looks like in practice. If you cannot give an example, cut the claim.

## Simulation references

When describing simulation, write what participants actually do — the situation, the decision, the constraint, the outcome. Not adjectives about simulation. Do not use "immersive."

## Assessment

Always describe three points: pre, in-session, post. Always answer the question "how do we know it worked?" — without using that literal phrase in copy.

## UAE fit

Cases, examples, and references must be UAE or regionally relevant. If you draw on a global example, adapt it to a UAE-relevant scenario. Reference UAE frameworks where they fit (see `uae-frameworks.md`).

## Bilingual readiness

Avoid English idioms, sports metaphors, Western pop-culture references, and complex phrasal verbs. Phrases must translate cleanly into Arabic.

## Output format expectations

- Markdown.
- `#` for major sections, `##` for subsections only. No deeper headings.
- Bullets at one indentation level only.
- One markdown table only per major section, used judiciously.
- Word caps respected per section (see `proposal-structures.md`). Don't exceed by more than 15%.
- For slide-mode output, use the slide block format (see `proposal-structures.md`).

## Iteration discipline

If a refinement is requested on a specific section, regenerate only that section. Do not rewrite the rest of the proposal.

## Final pre-output checks

- Have you used any banned word? Remove it.
- Have you invented any client name, statistic, or facilitator detail? Replace with `[INSERT: ...]`.
- Does each of the three primary differentiators appear concretely? If not, fix.
- Are all outcomes action-verb-led and measurable? If not, rewrite.
- Are simulation and approach sections concrete (named example)? If not, rewrite.

---

## Visual guardrails (v4, May 2026)

These are the visual-side equivalents of the banned-word list. They exist to keep the system from drifting toward AI-default aesthetics.

### Single-surface rule

Every slide uses **cream** (`#FEFCF7`). Never pure white. Never a dark background surface.

Slide role (cover vs. content vs. thank-you) is communicated through **graphics, type treatment, and layout** — not background color. The amber-peach gradient wave, photography, real logos, and type weight at scale carry the visual differentiation.

Within a slide, `--el-paper` (#FAF6EE) and `--el-paper-tan` (#F1EAD9) are available for **card insets and panel differentiation**, but never as full slide backgrounds.

**Navy** (`#14233F`) is a text and accent color — section prefixes, emphasis, small UI — never a background surface. **Forest/sage** greens are reserved for charts, data-viz, and controlled accent moments only.

### Type stack (the only allowed families)

- **Source Serif 4** for headers, titles, statement type, slide numerals.
- **DM Sans** for body, captions, in-card text.
- **JetBrains Mono** for eyebrows, all-caps section prefixes, metadata labels, technical numerals.
- **Open Sans** is retained ONLY for PowerPoint round-trip. **Do not invoke it in HTML.**

If you write `font-family: Inter` / `Roboto` / `Helvetica Neue` / `Calibri` / `Times New Roman` / `Fraunces` / `Playfair Display` in an Envision Lab artefact, you have drifted off-brand.

### Accent discipline

- **Gold** (`#B9913F` on light, `#E8B84C` on navy) is the signature accent. Use it for section prefixes, slide numerals, gold rules, single-point accents.
- **Amber** (`#E8B84C`) and **peach** (`#E89968`) are sourced from the EL logo gradient. Used **sparingly**:
  - Inside motifs (orbital gradients, contour washes).
  - As data-viz second/third colours.
  - As one or two intentional accent moments per slide (a status mark, a chart segment).
- Never place amber or peach adjacent to the EL logo. The logo carries its own gradient — let it be the star.
- Cap at ~2 accent moments per slide. Always ask: does this earn its colour?

**Anti-pattern:** any cool grey, pure white, second blue, green, red, purple — even for chart differentiation.

### Imagery rules

Three sizes only. Honour them. Over-large imagery breaks professional expectations for proposals.

- **Full-bleed** with navy overlay — Cover only.
- **Half-split** (photo on 35–45% of canvas) — Section openers and transitions only.
- **Small accent** (max 25% of canvas area) — Used to anchor a single content slide. Most content slides have **no imagery** at all; the design carries itself.

**Hard ban.** Staged corporate stock. Handshakes. Smiling office workers. AI-generated futurist imagery. Glowing brains. Abstract networks. Generic city skylines.

### Iconography

Tabler Icons only. Curated 28 live in `assets/icons/` at 2px stroke, 24×24 viewBox, `currentColor`. Pull more from the Tabler CDN for edge cases. **The numeral is still the primary icon** — Tabler icons are secondary metadata, not the lead visual.

**No** emoji. **No** Unicode pictographs (☎ ✉ ⚙ ⭐). **No** Office defaults. **No** mixing icon families.

### Motif discipline

Motifs live in `assets/motifs/` and are organised by slide type:
- Architectural geometry (mashrabiya) → section openers, TOC, thank-you.
- Topographic flow (dune contours) → roadmap, timeline, programme arc.
- Editorial marks (asterisk, corner arrows, brackets) → content slides, small-scale only.
- Orbital gradients → cover, statement slides, transitions.

Motifs render at low opacity (0.05–0.18) as atmosphere, behind type and content. **Never** place a motif inside a card or content block.

### Logo sourcing rule

Use real logos wherever possible — certifications (KHDA, Dubai SME, ISO marks), client logos, key frameworks (WHO ICOPE, ADDIE, Kirkpatrick, etc.), and partner organisations. Real logos carry visual authority that no icon or text label can match.

**Requirements:**
- Sufficient resolution for the context (min 2× the rendered size).
- Transparent background (PNG or SVG) where the logo sits on cream.
- Accurate, current version of the mark — not a recreation or approximation.

**If you cannot find a high-quality version:** ask the user. Do not omit the logo, substitute a placeholder icon, or attempt to recreate it. A `[INSERT: KHDA logo — high-res PNG with transparent bg]` placeholder is better than a bad logo.

### Things to NOT do (because every AI model does them)

- Beige + amber + Fraunces + Lucide as the default mood.
- Drop shadows and "card with rounded corners" everywhere.
- Centre-aligned hero with three feature columns.
- Gradient backgrounds spanning the whole slide.
- 12pt body text that nobody can read.
- Decorative emoji or Unicode glyphs to "add personality".
- Identical icon next to every list item.
- "Hero" stock photo on every section opener.
- Pastel-on-pastel low-contrast type.
- A second sans-serif as a "fun accent" font.

