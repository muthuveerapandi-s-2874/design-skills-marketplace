---
name: shift-visual-language
description: >
  Visual language for the Zoho Shift product — covers marketing website
  (zoho.com/shifts), product UI, landing pages, and any Shift-branded surface.
  Covers colour system, typography, patterns, banners, dark theme, screenshot
  rules, spacing, radius, CTA, structure, dropdown, icons, accents, imagery
  rules, logo, animation, WCAG 2.1 AA, and flowcharts. Triggers on explicit
  naming only: "Shift visual language", "Shifts design", "Shifts brand
  guideline", "Shifts website", "Shifts landing page", or similar. Does NOT
  trigger on generic "Zoho" work or other products.
---

# Shift Visual Language

**The product:** Zoho Shift — employee scheduling and time-tracking software
for SMBs. Use cases: shift scheduling, time clock, shift swapping, team
messaging, leave management. The marketing website lives at zoho.com/shifts.

**Scope:** Shift's full visual language — applies to the marketing website
(home, product, pricing, docs, blog), product UI, landing pages, and any
other Shift-branded surface. One visual language across all page types.

**Relationship to ODS:**

This skill sits on top of the ODS design system. It does **not** redefine
components, tokens, or accessibility rules — those all come from ODS.

**This skill reads from:**
- `design-system/components/*.json` — buttons, inputs, cards (use as-is)
- `design-system/tokens/spacing/spacing.json` — spacing scale
- `design-system/tokens/radius/elevation-radius.json` — radius + elevation
- `design-system/tokens/typography/typography.json` — type scale
- `design-system/themes/shift.json` — Shift's colour palette
- `design-system/accessibility/rules.md` — WCAG 2.1 AA base rules
- `skills/ods-design-system/products/shift.md` — Shift product guardrails

**This skill owns** (Shift-specific marketing craft — not covered by ODS):
visual aesthetic, page composition, colour proportions on the page, banner
rules, dark-theme section rhythm, screenshot conventions, page structure
library, dropdown mega-menu, accent usage, imagery rules, logo usage,
animation character, flowchart styles.

**The rule:** when this skill and ODS disagree, ODS wins.

---

## 1. Visual Aesthetic & Creative

**The feeling:** Warm and human — built for real teams. Scheduling is a messy, people-heavy problem (servers swapping Saturday night, a manager covering a call-out at 6am). The site should feel like it was made by someone who understands that — not a generic SaaS marketing machine.

**The creative register:** Restrained. Quiet craft, never loud. Confidence comes from typography, spacing, and real product UI — not from decorative flourish, oversized gradients, or "look at me" animation. If a section is catching your eye because of its decoration, it's wrong. It should catch your eye because the content is sitting right.

**The lead principle:** Real product UI, not illustrations. Every time the page needs a visual, the first move is a real product screenshot — a real shift card with Alex on Saturday 10–6, a real time-clock reading 09:02, a real swap request. Illustrations and AI imagery are fallbacks, not defaults. This is the single biggest thing that separates a Shifts page from generic SaaS. (See §9 Screenshot Rules.)

**The three-part test — every page must pass all three:**

1. Does it feel made for real teams, not for a pitch deck? (warm & human)
2. Is every visual element doing work, or is some of it decoration for its own sake? (restrained)
3. Would a shift manager recognize the product from the screenshots alone? (real UI first)

---

## 2. Senior Web Designer

**The bar:** Every page must read as the work of a senior web designer — someone with ten years of restraint, taste, and instinct for what to leave out. Not someone competent. Someone who's built enough to know what not to do.

**The six traits every page must show:**

1. **Intentionality.** Every element is there on purpose. If you can't say *why* a card, divider, or icon exists, it doesn't exist. Senior designers cut first, add second.
2. **Balance.** Type, color, whitespace, and imagery are in harmony across every section. No section visually outweighs the next unless the hierarchy calls for it. The page has a center of gravity.
3. **Restraint.** One idea per section. One primary CTA per viewport. One accent tile per card. When in doubt, subtract. Decoration without a job is the first tell of amateur work.
4. **Rhythm.** Sections don't all look alike and they don't all compete. The eye moves down the page through varied-but-related beats — text, visual, text, dark, visual, CTA. Spacing and structure carry the rhythm, not color changes.
5. **Craft in the details.** Radii on scale. Spacing on scale. Type weights pick from two (not five). Shadows soft, not dramatic. Icon tiles aligned to the grid. The little stuff is where senior shows up.
6. **Editorial confidence.** Headlines aren't hedged. Copy is direct. The page doesn't over-explain itself with badges, labels, tooltips, or "learn more" links everywhere. It says its thing and trusts the reader.

**The single ship test:** *"Can this page sit next to zoho.com/en-in/erp/ on the same domain without looking worse?"* If the answer is "probably fine" — rebuild it. The answer has to be an unambiguous yes.

**What makes a page look amateur (the #1 tell):** Templated, over-decorated, generic SaaS. You've seen the look — three feature cards with icon tiles, a gradient hero, a stats strip, a testimonial slider, a CTA. Everything is present. Nothing is chosen. Every time a page looks like it could belong to any SaaS product with the logo swapped, it fails this section. The fix is almost always: subtract decoration, increase spacing, commit to one idea per section.

### Vibrancy principle

Zoho pages should feel **bright, fresh, and confident** — not washed out, not apologetic, not corporate-bland.

1. **Use accent base colors (500) at full saturation.** When an accent appears — a cyan icon tile, a sky badge, a royal blue chip — it uses the base 500 hex at full opacity. Never dim with alpha or tint with grey.
2. **Status colors read vibrant.** Green `#05B488`, orange `#E14F06`, red `#BA0530` appear on pills and dots at full strength. Soft pastel versions exist only as paired backgrounds (`success-bg`, `warning-bg`, `error-bg`) with the dark text variant on top.
3. **Multiple accent icon tiles per page are encouraged** (within the 2-accent max rule) — they add color life across the page. A page of white cards with grey icons is wrong.
4. **Shadows stay soft but cards stay bright.** Elevation comes from shadow, not from dimming card content.
5. **Whitespace is the brightener.** A cramped page feels dim regardless of the colors. Follow the ODS spacing scale (§5) — generous padding keeps the page feeling airy and vibrant. **When something feels off, add spacing before adding color.**

### Screenshot / product UI rules

When the page includes product screenshots or UI fragments:

1. **Show only what's needed** — one specific moment; strip chrome, menus, sidebars unless directly relevant.
2. **No decorative annotations on the screenshot** — no arrows, no "click here" labels, no callouts overlaid on the UI.
3. **Real, plausible data** — `09:02`, `Alex`, `42 shifts`. Never `Lorem ipsum` or `Item 1 / Item 2`.
4. **No extra decoration around the screenshot** — soft shadow is enough. No glow rings, sparkles, or badges unless the composition explicitly calls for one status pill.
5. **Crop tight** — if UI needs room to breathe, increase container padding, not the image's internal whitespace.

### No stock imagery — non-negotiable

**Stock photos and stock illustrations are forbidden. No exceptions.** Stock kills the "senior designer" quality bar and makes pages feel templated.

**Fallback order when content needs a visual:**

1. **HTML/CSS UI mocks first.** If the content describes a shift calendar, time clock, chat thread, conflict alert, or dashboard, build it as real markup using the skill's cards, tokens, and status colors. This is the default — what produces the feature-page UI fragments.
2. **Read the content; make the visual match it.** If the copy says "Jordan requested a swap for Saturday 10–6," the visual shows a card with Jordan's name, Saturday, and those exact times. Never a generic person, never a generic calendar.
3. **AI-generated imagery only when HTML/CSS can't carry it** (hero illustrations, abstract concepts). Direct the generation to match the skill aesthetic — warm neutral canvas, soft editorial lighting, primary blue accents. Never generic corporate-SaaS output.
4. **People → initials avatars**, never photos. Use accent-palette fills — `AL` on cyan `#00B4D2`, `JO` on sky `#5A8CFF`, `MO` on royal blue `#2264DC`. Never stock headshots or AI-generated photorealistic faces. If a real face is genuinely needed, comment `needs real customer photography` and leave a placeholder.

**Forbidden explicitly:** Unsplash, Pexels, Pixabay, Shutterstock, iStock, Getty, Adobe Stock, any stock library; generic office/handshake/laptop/team photography; isometric SaaS illustrations ("people at desks," "floating dashboards," "hands holding phones"); placeholder services (placeholder.com, picsum.photos) even as mockup.

**The test:** If the visual could appear on any other SaaS site unchanged, it fails. Every Zoho Shifts visual should look specifically like it belongs to Zoho Shifts.

---

## 3. Colour

**The palette is tight on purpose.** Four colors carry the whole system: one primary, one secondary (used as the dark theme), a light gradient, and white. Everything else — accents, status colors, text tokens — comes from the ODS Zoho Shifts branding and is documented where it's used (accents in §Use of Accent Colours, text tokens in §Typography, status colors in §Screenshot Rules for shift states).

### Core palette

Shift's colours come from `design-system/themes/shift.json`. Marketing pages
use this tight four-surface subset:

| Token | Source | Hex | Role |
|---|---|---|---|
| `--primary` | `themes/shift.json → colors.primary.500` | `#3940D0` | Brand primary. Solid banners, primary CTA fills, active states, links. |
| `--light-gradient` | `themes/shift.json → colors.primary.200 → primary.50` | `#B4BCEE → #EEF0FB` | Light theme gradient — banner alternative to solid primary. |
| `--canvas` | ODS `colors.json → white.500` | `#FFFFFF` | Page background. Default for every section. |
| `--secondary` | Inline — not yet in `themes/shift.json` | `#161B63` | **Dark theme colour.** Dark-theme sections and headline text on light backgrounds. If this becomes formalised, it would be `primary.850` (between 800 and 900). |

### Hard rules

1. **White is the default.** Every content section is white unless it's explicitly a banner or a dark section. No grey fills, no tints, no off-whites. When in doubt — white.
2. **Primary `#3940D0` always appears at full saturation.** Never `rgba(57, 64, 208, 0.x)`. If a softer blue feel is needed, use the light gradient — not a dimmed primary.
3. **Dark theme `#161B63` is solid only.** No gradient on dark. No pattern on dark. No image background on dark. Flat confident surface.
4. **Minimum 2 dark-theme sections per page.** Not one, not zero. Two at least, placed between content beats (typical spots: after the opening deep-dives, and before the final CTA). If the content doesn't naturally fill two dark beats, write one — a manifesto statement, a stat strip, a customer quote, a logo band.
5. **The light gradient is banner-only.** Not a section background, not a card fill, not a hover state. Banners can be either solid `#3940D0` *or* the light gradient — designer picks per page based on the page's tone. Never use both flavors on the same page.
6. **No other background colors exist on-page.** No warm greys, no pastels, no tinted surfaces. White, solid primary banner, light gradient banner, solid dark. That's it.

### Proportions — how the page reads by color

A well-built Shifts page breaks down roughly like this:

- **~65–75% white** — content sections, screenshot zones, feature grids, copy blocks. White carries the page.
- **~15–20% dark `#161B63`** — two dark sections, each full-bleed. This is the contrast rhythm; without it the page feels flat.
- **~10–15% banner** (solid primary or light gradient) — hero at the top, CTA near the bottom. Bookends only.

If dark sections are under 15% of the page's scroll length, add another or make one taller. If white is under 60%, the page is over-decorated and needs to be cut back.

### The "if you remember one thing"

**Four surfaces: white, solid primary, light gradient, solid dark.** Every background on every page is one of those four. The moment you find yourself reaching for a fifth, stop — something else is wrong.

### Foreground text tokens (reference — full use in §4 Typography, §21 WCAG)

| Token | Value | Use |
|---|---|---|
| `--fg-primary` | `#161B63` | Headlines, labels, strong text |
| `--fg-secondary` | `#343A66` | Sub-headlines, secondary text |
| `--fg-tertiary` | `#55597A` | Body paragraphs |
| `--fg-muted` | `#969BC0` | **Decorative/disabled only** — fails 4.5:1 on white. Never use for readable text; use `--fg-tertiary` instead. |

### Status tokens (reference — full use in §9 Screenshot Rules for shift states)

| Token | Value | Use |
|---|---|---|
| `--success` | `#05B488` | Shift confirmed, clocked in, approved |
| `--warning` | `#E14F06` | Pending approval, late clock-in |
| `--error` | `#BA0530` | Conflict, missed shift, rejected |
| `--info` | `#3940D0` | In progress, active, info callouts |

Status colors are for scheduling UI state only (shift badges, clock states, approval pills). Never use them decoratively. Never mix with accents (§17).

### Borders & lines (reference — full use in §9 Screenshot Rules, §22 Flow Chart)

| Token | Value | Use |
|---|---|---|
| `--line` | `#D4D4D8` | Card borders, inactive connectors, neutral strokes |
| `--line-active` | `#3940D0` | Active flow paths, active connectors |

---

## 4. Typography

**One family, two weights.** Puvi — the ODS typeface — carries the entire site. Two weights only: **Regular 400** for body, **Medium 500** for every heading. No Semibold, no Bold. If a headline needs more emphasis, go up in size — never up in weight.

**Source of truth:** font family, weights, sizes, line-heights, and letter-spacing live in `design-system/tokens/typography/typography.json`. This skill does not redefine them. What this skill adds is Shift's **usage discipline** — two-weight rule, how type pairs with surfaces, and headline colour on light vs dark sections.

### Type scale

| Role | Size | Weight | Line-height | Letter-spacing |
|---|---|---|---|---|
| H1 | 64px | 500 Medium | 1.1 | -0.02em |
| H2 | 40px | 500 Medium | 1.1 | -0.02em |
| H3 | 28px | 500 Medium | 1.1 | -0.01em |
| H4 | 20px | 500 Medium | 1.1 | -0.01em |
| Body | 16px | 400 Regular | 1.5 | 0 |
| Small | 14px | 400 Regular | 1.5 | 0 |

### Hard rules

1. **Puvi only.** No system stack fallbacks shown as the primary, no Inter, no mono font. The ODS import handles fallbacks for load failures — don't override it.
2. **Two weights only: 400 and 500.** Weights 300, 600, 700, 800, 900 don't exist in this system. For emphasis in body copy use `<strong>` which maps to 500 — don't introduce a bolder weight.
3. **Headings are always Medium 500.** H1 through H4. Headings never appear at Regular 400.
4. **Body is always Regular 400.** Paragraph text never appears at Medium. If a paragraph needs to "stand out," it's probably a pulled quote or a feature subheading — use H3 or H4.
5. **H1 is 64px on desktop. Don't dial it down.** A 48px or 40px H1 "because it felt big" is the fastest way to make a page look junior. 64px is the point. Scale down only on mobile per the ODS responsive scale.
6. **Headings tight, body comfortable.** Headings use 1.1 line-height and -0.01 to -0.02em letter-spacing so they feel confident and editorial. Body uses 1.5 line-height and default letter-spacing so it reads well for paragraphs. Never swap these.
7. **One H1 per page.** H2s structure sections. H3s structure within sections. H4s are for small labels, card titles. Don't skip levels (no H1 → H3).
8. **Color comes from the text tokens, not arbitrary hex.** Headlines = `--fg-primary` `#161B63`. Sub-heads = `--fg-secondary` `#343A66`. Body = `--fg-tertiary` `#55597A`. Never `color: #000` and never `color: grey`.

### Implementation shape

```css
.h1    { font: 500 64px/1.1 'Puvi', sans-serif; letter-spacing: -0.02em; color: #161B63; }
.h2    { font: 500 40px/1.1 'Puvi', sans-serif; letter-spacing: -0.02em; color: #161B63; }
.h3    { font: 500 28px/1.1 'Puvi', sans-serif; letter-spacing: -0.01em; color: #161B63; }
.h4    { font: 500 20px/1.1 'Puvi', sans-serif; letter-spacing: -0.01em; color: #161B63; }
.body  { font: 400 16px/1.5 'Puvi', sans-serif; color: #55597A; max-width: 60ch; }
.small { font: 400 14px/1.5 'Puvi', sans-serif; color: #55597A; }
```

### The "if you remember one thing"

**Puvi, two weights, six sizes.** That's the entire type system. Emphasis comes from size and space, not from piling on weights or colors.

---

## 5. Pattern

**Two patterns carry the whole system: Dotted and Grid.** The old Hatch pattern is retired. One pattern per section — never layered.

Both patterns come from ODS tokens — opacity, line weight, and color are defined there, not re-declared in the skill. Use the ODS token; don't hand-tune the `rgba()` value.

### Pattern A — Dotted

**Where it goes:**
1. **Behind every product screenshot** — as the radial-fade zone that frames the UI mock (see §Screenshot Rules). The screenshot sits on the page, the dots fade in around it. No container box, no border.
2. **On dark-theme `#161B63` sections** — the dots appear at low opacity over the dark surface, giving the dark beat a subtle texture. Stops the dark section from feeling like a flat void.

**Where it does NOT go:**
- Not on plain white content sections (those stay clean white).
- Not on banners (dotted on banners reads as noise — banners use grid).
- Not on footers.
- Not inside cards or icon tiles.

```css
/* Reference shape — use ODS tokens for color + opacity */
.bg-dots {
  background-image: radial-gradient(circle, var(--pattern-dot-color) 1px, transparent 1px);
  background-size: 24px 24px;
}
```

### Pattern B — Grid

**Where it goes:** Wherever you want, as editorial softening — most commonly:
1. **Banners** (both solid primary and light gradient) — white or tinted grid lines at low opacity.
2. **Footer** — dark grid lines on the footer surface.
3. **Any content section** where a plain-white expanse needs a touch of structure (rare — default is plain white).

**Where it does NOT go:**
- Not behind screenshots (that's dotted territory).
- Not on dark `#161B63` sections (that's dotted territory).
- Not stacked with dotted on the same surface.

```css
/* Reference shape — use ODS tokens for color + opacity */
.bg-grid {
  background-image:
    linear-gradient(to right, var(--pattern-grid-color) 0.5px, transparent 0.5px),
    linear-gradient(to bottom, var(--pattern-grid-color) 0.5px, transparent 0.5px);
  background-size: 40px 40px;
}
```

### Hard rules

1. **Dotted = screenshots + dark sections. Grid = banners, footer, optional editorial use.** Getting this backwards (grid behind a screenshot, dotted on a banner) is a signature of an amateur page.
2. **One pattern per section. Never combine.** No dotted overlaid on grid. No grid on a dark section with dots. A section has one pattern or zero patterns — never two.
3. **Plain white (no pattern) is the default** for every content section that isn't a screenshot zone. When in doubt — no pattern.
4. **Opacity comes from ODS tokens.** Don't invent values. If a pattern feels too strong or too faint, check that the ODS token is being applied — don't override it with an arbitrary `rgba()`.
5. **Hatch is retired.** Don't introduce a third pattern. If a section needs something extra, it probably needs more whitespace — not another pattern.

### Typical page pattern sequence

| Section | Pattern |
|---|---|
| Hero banner (solid primary or light gradient) | Grid |
| Hero screenshot (on white) | Dotted radial-fade around the screenshot |
| Intro text section | Plain white |
| Deep-dive screenshot | Dotted radial-fade around the screenshot |
| Deep-dive text section | Plain white |
| **Dark section 1** | Dotted (low opacity over `#161B63`) |
| Feature grid | Plain white |
| **Dark section 2** | Dotted (low opacity over `#161B63`) |
| CTA banner | Grid |
| Footer | Grid |

### The "if you remember one thing"

**Dots behind UI, grid behind banners.** Everything else is plain white.

Goal: considered rhythm, not wallpaper.

---

## 6. Banner Colour

**Two banner flavors. Pick one per page — never mix.**

- **Solid `#3940D0`** — for home, landing pages, marketing campaigns. Confident, saturated, brand-forward.
- **Light gradient `linear-gradient(180deg, #B4BCEE 0%, #EEF0FB 100%)`** — for inner product pages, feature pages, docs landing, pricing. Softer, more editorial, lets the content lead.

The whole page commits to one flavor. If the hero is solid primary, the CTA banner at the bottom is also solid primary. If the hero is gradient, the CTA banner is gradient. No page has both.

### Solid primary banner

| Element | Treatment |
|---|---|
| Background | Solid `#3940D0` |
| Pattern | Grid overlay at low opacity, white/tinted lines (per §5 Pattern) |
| H1 | White `#FFFFFF`, 100% opacity |
| Body / subhead | White `#FFFFFF`, 75% opacity |
| Eyebrow label (optional) | White `#FFFFFF`, 60% opacity, uppercase, 14px |
| Focus ring | White `#FFFFFF` |

```css
.banner--primary {
  position: relative;
  background:
    linear-gradient(to right, rgba(255,255,255,0.08) 0.5px, transparent 0.5px) 0 0 / 48px 48px,
    linear-gradient(to bottom, rgba(255,255,255,0.08) 0.5px, transparent 0.5px) 0 0 / 48px 48px,
    #3940D0;
  color: #FFFFFF;
}
.banner--primary h1, .banner--primary h2 { color: #FFFFFF; }
.banner--primary p { color: rgba(255,255,255,0.75); }  /* 4.90:1 on #3940D0 — passes AA */
.banner--primary :focus-visible { outline-color: #FFFFFF; }
```

### Light gradient banner

| Element | Treatment |
|---|---|
| Background | `linear-gradient(180deg, #B4BCEE 0%, #EEF0FB 100%)` — darker at top |
| Pattern | Grid overlay at low opacity, tinted lines (per §5 Pattern) |
| H1 | `#161B63` |
| Body / subhead | `#55597A` |
| Eyebrow label (optional) | `#343A66`, uppercase, 14px |
| Focus ring | `#3940D0` |

```css
.banner--gradient {
  position: relative;
  background:
    linear-gradient(to right, rgba(22,27,99,0.06) 0.5px, transparent 0.5px) 0 0 / 48px 48px,
    linear-gradient(to bottom, rgba(22,27,99,0.06) 0.5px, transparent 0.5px) 0 0 / 48px 48px,
    linear-gradient(180deg, #B4BCEE 0%, #EEF0FB 100%);
  color: #161B63;
}
.banner--gradient h1, .banner--gradient h2 { color: #161B63; }
.banner--gradient p { color: #55597A; }
.banner--gradient :focus-visible { outline-color: #3940D0; }
```

### Primary CTA on banners

Designer picks per page — the banner's job is to look right, and the CTA follows. The only rule is that the CTA must have **4.5:1 contrast** against the banner surface it sits on (WCAG AA). See §12 CTA for the full button spec.

On solid primary the CTA is often a white button with primary text. On the light gradient the CTA is often solid `#3940D0` with white text. But neither is forced — if a different treatment reads better for a specific page, use it, as long as the contrast ratio passes.

### Hard rules

1. **One flavor per page.** Solid primary hero = solid primary CTA banner. Light gradient hero = light gradient CTA banner. Mixing flavors inside one page looks amateurish — the page loses its color identity.
2. **Home and landing pages use solid primary.** This is the confident, brand-forward surface. If you're reaching for gradient on a home page, you're probably under-committing.
3. **Inner product / feature / docs / pricing pages use the light gradient.** These pages are about content — the gradient is softer so the feature UI, tables, and copy lead the composition.
4. **Light gradient direction is fixed: top-to-bottom, `#B4BCEE → #EEF0FB`.** Darker at top. Never diagonal, never reversed.
5. **Banner text is dictated by banner flavor, not by designer taste.** Solid primary → white text (100 / 75). Light gradient → dark text (`#161B63` / `#55597A`). Don't put dark text on solid primary or white text on the light gradient — both fail contrast.
6. **Grid pattern sits on both flavors** at low opacity (per §5 Pattern). Never dotted, never plain.
7. **Banners bookend the page only** — hero at the top, CTA near the bottom. Banners don't appear mid-page as section accents. If a mid-page section wants emphasis, use a dark `#161B63` section instead.
8. **No transition strip between banner and next section.** The banner ends, the next section starts clean. No fade, no gradient softening band.

### The "if you remember one thing"

**Home = solid primary, inner pages = light gradient. Pick one, commit to it, white text on primary, dark text on gradient.**

---

## 7. Dark theme

**Dark = solid `#161B63`, always.** No gradient, no tint, no photo background. Flat, confident, indigo-navy. Dark sections are the page's moments of contrast — without them the page reads as a flat white slab.

**Required on every page: minimum 2 dark-theme sections.** Not one. Not zero. Two or more.

### Surface

| Element | Treatment |
|---|---|
| Background | Solid `#161B63` |
| Pattern | Dotted at low opacity (per §5 Pattern). Grid is not allowed on dark. |
| Padding | Same ODS spacing scale as any other section (e.g. `--section-lg` vertical). Dark is not taller than content — it earns its weight through color, not size. |

### Text on dark

| Element | Color |
|---|---|
| H1 / H2 / headline | White `#FFFFFF`, 100% opacity |
| Body / subhead | White `rgba(255,255,255,0.75)` — 75% opacity (7.11:1 on `#161B63`, passes AA) |
| Eyebrow label (optional) | White `rgba(255,255,255,0.6)`, uppercase, 14px |
| Links | White underlined, or light primary `#B4BCEE` |
| Focus ring | White `#FFFFFF` |

Never drop body below 75% white — 65% fails 4.5:1. Never use `#161B63` headline text on a `#161B63` surface (invisible). Never use a colored H1 on dark (e.g. cyan headline) — headlines stay pure white.

```css
.dark-section {
  background: #161B63;
  color: #FFFFFF;
  padding-block: var(--section-lg);
}
.dark-section h1, .dark-section h2 { color: #FFFFFF; }
.dark-section p { color: rgba(255,255,255,0.75); }  /* 7.11:1 on #161B63 — passes AA */
.dark-section :focus-visible { outline-color: #FFFFFF; }
```

### Content on dark — designer picks

Dark sections are not restricted to editorial beats. Any content type is allowed:

- **Manifesto** — single bold statement, short supporting line.
- **Stat strip** — 3–4 large numbers with labels.
- **Featured testimonial** — single customer quote in large type.
- **Logo band** — "Used by..." customer logos in white at 60% opacity.
- **Comparison beat** — "With Shifts / Without Shifts" two-column contrast.
- **Feature highlight with UI** — product screenshot on dark, dotted pattern behind it.
- **Feature grid** — cards on dark (white-on-dark inverse of the light card).
- **Deep-dive section** — split text + visual, same structure as on white.

Designer picks. If it works as a content type on white, it works on dark — just apply the dark color tokens.

### Placement of the 2+ dark sections

**Designer picks — but the dark sections must be spaced apart, never adjacent.** Two dark sections back-to-back collapse into one visual moment and waste the contrast. A white (or screenshot) section must sit between them.

Good cadence on a typical page:

```
Hero banner → content → content → DARK → content → content → DARK → CTA banner
```

Bad cadence:

```
Hero banner → DARK → DARK → content → CTA     ← dark sections collide, contrast lost
Hero banner → content → content → DARK → CTA  ← only one dark section, rule violated
```

### Hard rules

1. **Minimum 2 dark sections per page.** Not one. If you can't find two natural content moments for it, write one (a manifesto statement or a stat strip will always fit).
2. **Solid `#161B63` only.** No gradient on dark. No tint. No photo background. Flat.
3. **Dark sections are never adjacent.** A non-dark section must separate them — otherwise they merge into one visual beat and the contrast rhythm dies.
4. **Dark sections are not at the very top or very bottom.** Top = hero banner. Bottom = CTA banner + footer. Dark lives in the middle of the page between content.
5. **Text on dark is white only** — headline 100%, body 75%. Never colored headlines on dark. Never below 75% body.
6. **Pattern on dark is dotted only** (low opacity). No grid on dark.
7. **Inverted components on dark keep the same shape.** A card on dark has the same radius, padding, and type treatment as on white — just with the dark color tokens applied. Don't invent new card layouts for dark.
8. **Same spacing scale as content.** Dark sections use the same ODS spacing scale as white sections — they don't get extra padding to feel "more important."

### The "if you remember one thing"

**Two dark sections, minimum. Solid `#161B63`. White text 100/75. Spaced apart, in the middle of the page.**

---

## 8. Light Gradient theme

**→ See §6 Banner Colour.**

The light gradient `linear-gradient(180deg, #B4BCEE 0%, #EEF0FB 100%)` is the skill's "light theme" surface, and it appears **as a banner flavor only**. It is not a separate theme, not a section background, and not a page variant. The full spec — direction, text color, pattern, placement, flavor-per-page rule — lives in §6.

**Quick recap of the hard rules:**

1. Banner-only — never a section background, card fill, or hover state.
2. Direction fixed: top-to-bottom, `#B4BCEE` at top → `#EEF0FB` at bottom.
3. Used for inner product / feature / docs / pricing pages (home and landing use solid primary instead).
4. Text on the gradient is dark: H1 `#161B63`, body `#55597A`. White text on this surface fails contrast.
5. Grid pattern overlay at low opacity (per §5 Pattern). Never dotted.

---

## 9. Screenshot Rules

**Source: real product screenshots only.** Captured from the actual Zoho Shifts app. No HTML/CSS UI mocks presented as product UI, no AI-generated app interfaces, no Figma comps used as hero images. If the screenshot you need doesn't exist in the product yet, that's a product request — not a design shortcut.

**Why this is non-negotiable:** a Shifts page's credibility comes from "this is what you actually see when you use the product." A convincingly-mocked UI is the fastest way to ship a page that feels dishonest. Real screenshots also force the design to fit the product — not the other way around.

### Main-level pages show the product dashboard

**On home and the main product landing page, the hero screenshot is the product dashboard — specifically the main scheduling / week-view calendar.** This is the "this is Zoho Shifts" image. Every visitor's first impression of the product is the week-view calendar, so it's the first thing they see on the page.

**On inner pages** — feature pages, pricing, docs, integrations, blog — screenshots show the **specific feature or flow** the page is about (the clock-in screen on the time-clock page, the swap request view on the swap page, the leave request modal on the leave page). **Do not default to the dashboard on inner pages** — using the dashboard everywhere makes inner pages feel generic.

| Page type | Hero screenshot |
|---|---|
| Home page | Main scheduling week-view calendar (dashboard) |
| Main product landing page (`/shifts`) | Main scheduling week-view calendar (dashboard) |
| Feature page (time clock, swaps, leave, messaging…) | That specific feature's main screen |
| Pricing | Plan comparison UI or no screenshot hero |
| Docs landing | Search / nav or no screenshot hero |
| Integrations / blog / customers | Page-specific — pick the clearest representative screen |

### Framing — radial-fade dotted zone

Screenshots sit directly on the page surface. **No container, no border card, no background fill.** A dotted pattern appears in a zone behind the screenshot and fades radially outward into the background — so the screenshot feels anchored but not boxed in.

The screenshot itself gets three treatments: a **corner radius** (4px or 12px based on section), a **1px stroke** (subtle border), and a **shadow** (calibrated to the surface it sits on).

```css
.screenshot-zone {
  position: relative;
  padding: var(--space-6) var(--space-4);   /* 96px 40px */
  background-color: transparent;
  background-image:
    radial-gradient(circle, var(--pattern-dot-color) 1px, transparent 1px);
  background-size: 24px 24px;
  -webkit-mask-image: radial-gradient(ellipse at center,
    rgba(0,0,0,1) 0%, rgba(0,0,0,0.9) 40%,
    rgba(0,0,0,0.4) 75%, rgba(0,0,0,0) 100%);
          mask-image: radial-gradient(ellipse at center,
    rgba(0,0,0,1) 0%, rgba(0,0,0,0.9) 40%,
    rgba(0,0,0,0.4) 75%, rgba(0,0,0,0) 100%);
}

/* The screenshot image itself */
.screenshot-zone img {
  display: block;
  max-width: 100%;
  border-radius: 12px;                              /* default — see radius rules below */
  border: 1px solid rgba(22,27,99,0.08);            /* 1px stroke on light surface */
  box-shadow: 0 24px 40px -16px rgba(22,27,99,0.14); /* soft bottom-edge shadow */
}

/* On dark #161B63 sections — stroke flips white, shadow deepens */
.dark-section .screenshot-zone img {
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 32px 56px -20px rgba(0,0,0,0.45);
}

/* Tight/compact screenshots — smaller radius */
.screenshot-zone img.compact {
  border-radius: 4px;
}
```

### Radius — 4px or 12px, picked by section

| Context | Radius |
|---|---|
| Normal content sections (deep-dives, feature spotlights, mid-page product moments) | **12px** — matches the card radius |
| Tight / compact spots (hero close-ups, inline mini-mocks, small cropped UI fragments) | **4px** — feels more precise when the image is small or tightly framed |

Nothing between 4 and 12. Nothing above 12. If you're unsure — 12px.

### Stroke — 1px solid, always

Every screenshot gets a 1px stroke. Without it, the edge of the UI fades into the page and the image can read as "unfinished" on certain screens. The stroke color flips with the surface:

| Surface | Stroke |
|---|---|
| White / light gradient section | `1px solid rgba(22,27,99,0.08)` |
| Dark `#161B63` section | `1px solid rgba(255,255,255,0.08)` |

Use the ODS border token where the system provides one; these `rgba()` values are the fallback spec.

### Shadow — section-aware

| Surface | Shadow |
|---|---|
| White / light gradient section | `box-shadow: 0 24px 40px -16px rgba(22,27,99,0.14)` — soft bottom-edge |
| Dark `#161B63` section | `box-shadow: 0 32px 56px -20px rgba(0,0,0,0.45)` — deeper, larger spread |
| Banner (hero / CTA) | **No shadow.** Screenshots don't appear on banners — the rule is here to make that unambiguous. |

All shadows are single-direction (negative y-offset, large blur, negative spread) so the glow only appears below the image — never wraps around the sides or top.

### Placement on the page

- **White content sections** — the default. Dotted radial-fade zone around the screenshot, 1px light stroke, soft bottom shadow.
- **Dark-theme `#161B63` sections** — same radial-fade treatment with the dotted pattern visible over the dark surface. Stroke flips to white-8%, shadow deepens.
- **Not on banners** (hero or CTA). The screenshot sits in the section immediately below the hero, not on it.
- **Not inside cards.** A feature needing a screenshot gets its own section.
- **Not in the footer.**

### Data inside the screenshot

**Real, plausible data — and it must match the page's narrative.** If the copy says "Jordan requested a swap for Saturday 10–6," the screenshot shows Jordan's name, Saturday, and exactly those times. The image and the words confirm each other.

- **Names** — plausible first names (Alex, Jordan, Priya, Maria, Chen, Sam). No "User 1" or "Test Employee."
- **Times** — realistic shift times (`09:02`, `14:30 → 22:00`). No `00:00` or `12:34:56`.
- **Counts** — plausible team sizes (`8 servers`, `42 shifts this week`). No round debug numbers.
- **No Lorem ipsum. No "Item 1 / Item 2."**

### Cropping and content rules

1. **Show only what's needed.** Crop to the specific moment the page is describing — one shift card, one clock-in row, one conflict alert. Strip unrelated chrome.
2. **No decorative annotations.** No arrows, no "click here" labels, no highlight circles, no callout tooltips overlaid on the UI.
3. **No glow rings, sparkles, or badges around the screenshot.** Stroke + shadow is all the framing it gets. One status pill floating beside the screenshot as a composition element is allowed — more is not.
4. **Crop tight.** If the UI needs breathing room, increase the zone's padding — don't pad the image's internal whitespace.
5. **2x / retina export.** No JPEG artifacts on UI text. PNG or optimized WebP.

### Hard rules

1. **Real product screenshots only.** No HTML/CSS mocks passed off as product UI. No AI-generated app screens. No Figma comps.
2. **Home + main product landing page hero = the dashboard (week-view calendar).** Inner pages show the specific feature, not the dashboard.
3. **Radial-fade dotted zone is the framing — nothing else.** No bordered container card, no background fill behind the image.
4. **Every screenshot gets a 1px stroke** — light on light surfaces, white-alpha on dark.
5. **Radius is 4px or 12px, picked by section** — 12px in normal sections, 4px in tight/compact spots. Nothing else.
6. **Shadow is section-aware** — soft on white, deeper on dark, none on banners. Always single-direction (bottom edge only).
7. **Data matches the page's narrative** — names, times, and counts confirm the copy.
8. **No decorative overlays** — arrows, labels, sparkles, glows.
9. **Screenshots on white and dark sections only.** Never on banners, never inside cards, never in the footer.

### The "if you remember one thing"

**Main-level page = dashboard. Inner page = specific feature. Real product, real data, dotted zone, 1px stroke, bottom-edge shadow. Radius 4 or 12. Nothing else touches it.**

---

## 9.1 Asset Library — the canonical Figma source

**All product screenshots used on the website come from a single Figma file** — the Product UI library. This is the authoritative source. Do not hunt for screenshots elsewhere, do not screen-record the app yourself, do not use old decks. One library, one source of truth.

**File:** [Shifts Product UI — Figma](https://www.figma.com/design/3ftuJOLJC0McvUPlBXrLgo/Product-UI?node-id=0-1&m=dev)
**File key:** `3ftuJOLJC0McvUPlBXrLgo`

**These are production product UI** — not comps, not marketing mocks. They satisfy the §9 "real product screenshots only" rule. The §9 ban on "Figma comps used as hero images" is specifically about *marketing comps* — invented UI drawn to make a page look good. The library below is the shipped product rendered in Figma as the export format, which is different and allowed.

### How to pick the right screenshot for a piece of content

Read the content the page is about, then pick the screenshot that shows *that specific feature*. Never default to the dashboard on an inner page.

**Web / desktop screens**

| Page / section topic | Use this screen | Node ID |
|---|---|---|
| Home hero, `/shifts` main landing hero | Dashboard Admin (or Dashboard Admin with Time Clock Widget) | `1:2294` / `1:2137` |
| Scheduling, week-view calendar, drag-to-schedule | Schedule Screen | `1:8048` |
| Creating a shift, shift builder, publishing shifts | Shift Creation 1 or Shift Creation 2 | `1:10148` / `1:10568` |
| Editing an existing shift, edit shift modal, breaks | Edit Shift | `1:10345` |
| Time off, leave requests, PTO flow | Request Time Off | `1:12160` |
| Team messaging, chat, channels | Chats | `1:12986` |

**Mobile / kiosk screens**

| Page / section topic | Use this screen | Node ID |
|---|---|---|
| Mobile app for employees (iOS) — home, clock in from phone | IOS Home Mobile App | `1:21915` |
| Mobile app for employees (Android) — home | Android Home Mobile App | `1:21928` |
| Kiosk clock-in (Android tablet mounted on wall) | Android Kiosk Clock In | `1:21936` |
| Kiosk clock-in (iPad) | Ipad Kiosk Clock In | `1:21950` |
| Admin approving a clock-in from phone | Admin → Clock In | `1:21964` |
| Timesheets on Android phone | Android Timesheets Mobile App | `1:25995` |
| Timesheets on iOS phone | IOS Timesheets Mobile App | `1:26030` |

### When multiple screens could work — the tiebreakers

1. **Match the narrative exactly.** Copy says "manage swaps from your phone"? → mobile app screen, not desktop. Copy says "see the full week at a glance"? → Schedule Screen, not Dashboard.
2. **Prefer the newest variant when two exist.** `Dashboard Admin (New Time Clock Widget)` is newer than `Dashboard Admin` — use the new one on the home hero. `Shift Creation 2` is the later iteration of `Shift Creation 1` — use 2 unless the copy specifically shows the earlier step.
3. **On the mobile section of a page, show the platform the copy mentions.** If copy is platform-neutral, pick iOS (broader market recognition); put Android alongside only if the section is specifically about cross-platform.
4. **On feature pages, never open with the dashboard.** The feature's own screen is the hero — that's the whole §9 inner-page rule.

### Fetching a screenshot

Use the Figma MCP `get_design_context` with the file key `3ftuJOLJC0McvUPlBXrLgo` and the node ID from the tables above. If the Figma MCP is not available in the session, tell the user exactly which node to export from the Figma file (e.g. "please export node `1:8048` as 2x PNG"). Do not substitute an HTML/CSS mock.

### Hard rules specific to the library

1. **The library is the only source.** If a needed screen isn't in it, stop and flag it — that's a library gap to raise, not a reason to mock something up.
2. **One screen per concept per page.** Do not show the same dashboard twice on one page because the file has two dashboard variants. Pick one.
3. **Do not edit the screens in the library before exporting** (renaming users, changing times, recoloring). The §9 "real, plausible data" rule is already met by the library's native data. If the narrative truly needs different data, that's a product/library request — raise it, don't edit locally.
4. **Node IDs above are pinned to today's library.** If a node ID 404s on fetch, re-run `get_metadata` on the file to get the current ID, and update this table.

---

## 10. Spacings

**Spacing is owned by ODS.** Source: `design-system/tokens/spacing/spacing.json`. This skill does not invent a scale — every margin, padding, and gap on every page snaps to an ODS token.

No arbitrary values. No `padding: 18px`. No `margin: 26px`. If a value isn't in the ODS scale, it doesn't exist in the system.

### Scale source

- **Element-level spacing** — `--space-*` tokens from ODS, 8-based (8, 16, 24, 40, 64, 96, etc.). Used for gaps between items, card internal padding, button padding, stack spacing.
- **Section-level padding** — ODS section tokens (e.g. `--section-sm`, `--section-md`, `--section-lg`, `--section-xl`). Used for the vertical padding of full-width sections.
- **Container width** — content is capped at **1200px centered** on desktop. Never full-bleed text, never a 1440px wall of copy. The 1200px cap is what gives the page its editorial center of gravity.

If the ODS system provides a named token, use it. Don't hardcode `padding: 96px` when `padding-block: var(--section-md)` is available.

### Container rule

```css
.container {
  max-width: 1200px;
  margin-inline: auto;
  padding-inline: var(--space-4);   /* 40px gutter on desktop, tightens on mobile */
}
```

Every full-width section is the section's background (white, dark, banner, gradient) with a `.container` inside it holding the content. Background goes edge-to-edge; content stays within 1200px.

### Section padding rhythm

Sections use ODS section tokens for vertical padding. The typical page breaks down roughly like this:

| Section type | Vertical padding |
|---|---|
| Hero banner | `--section-xl` (tallest — the opening moment needs room) |
| Content section (deep-dive, feature group, screenshot zone) | `--section-md` or `--section-lg` |
| Dark-theme section | `--section-md` — same as content, not taller (dark earns weight from color, not size — see §7) |
| CTA banner | `--section-lg` |
| Footer | `--section-md` |

Final values come from ODS — if ODS says `--section-md` is 96px, it's 96px. Don't override.

### Hard rules

1. **Every spacing value comes from an ODS token.** No arbitrary values. `padding: 18px` or `margin: 32px` is a violation — pick the nearest token.
2. **Use named tokens, not raw values.** `padding-block: var(--section-md)` — not `padding-block: 96px`. Raw values drift over time; tokens stay in sync with ODS updates.
3. **1200px max content width.** Every `.container` caps at 1200px and centers. Full-bleed only for section backgrounds, never for content.
4. **Section vertical padding is never less than `--section-sm`.** If a section feels tight, increase vertical padding before adjusting anything else.
5. **Gutters scale on mobile.** Desktop `--space-4` (40px) side padding → mobile `--space-2` or `--space-3` (16–24px). Use ODS responsive tokens if provided.
6. **When in doubt, add space.** A page that feels cramped is almost never fixed by color or decoration — it's fixed by moving up one step on the spacing scale.

### The "if you remember one thing"

**ODS tokens only. 1200px centered container. When something feels off, add space before adding anything else.**

---

## 11. Radius

**Radius is owned by ODS.** Source: `design-system/tokens/radius/elevation-radius.json`. Shift marketing pages use a tight subset — 0, 4, 8, 12, 999 — and don't introduce other values.

**Five radius values in the whole system: 0, 4, 8, 12, 999.** Nothing else. No 2, no 6, no 14, no 20, no 24. If a shape isn't one of these five values, it doesn't belong in the system.

### The scale

| Radius | Token | Use |
|---|---|---|
| **0** | — | Section rectangles only (full-bleed edges: hero banner, dark section, CTA banner, footer). Not for interactive elements. |
| **4** | `--radius-xs` | Buttons (all buttons, everywhere — tight CTA shape). Dark-section cards and containers. Tight/compact screenshots. |
| **8** | `--radius-sm` | Inputs, selects, textareas. Small icon tiles. |
| **12** | `--radius-md` | **Default for cards.** Feature cards, pricing cards, content cards. Normal-section screenshots. |
| **999** | `--radius-full` | Pills — status pills, shift pills, badges, chips, tags, avatars. Full-radius circle/stadium. |

### Component-to-radius mapping

| Component | Radius |
|---|---|
| Section (full-bleed edges) | 0 |
| Button (primary, secondary, ghost — everywhere) | 4 |
| Dark-section card / container | 4 |
| Screenshot in a tight / compact spot | 4 |
| Input, select, textarea | 8 |
| Small icon tile | 8 |
| Card (default) | 12 |
| Screenshot in a normal content section | 12 |
| Pill / badge / chip / tag | 999 |
| Avatar (circle) | 999 |

If a component isn't listed, it's either an edge case (ask the designer) or it's being invented for no reason (don't invent it).

### Hard rules

1. **Five values only: 0, 4, 8, 12, 999.** Anything else is a violation — no `border-radius: 6px`, no `border-radius: 14px`, no `border-radius: 20px`.
2. **Ceiling is 16px.** Nothing in the system uses 16px or above. The 16px value that existed in earlier versions is retired.
3. **Floor is 4px** for interactive elements. Sections are the only thing that use 0.
4. **Buttons are 4px everywhere.** Not 8, not 12. The tight corner is what gives the Shifts button its crisp, confident shape — on solid primary banners, on white content sections, on dark sections, same radius.
5. **Cards are 12px by default, 4px only on dark sections.** Cards on white/light surfaces use 12. When a card sits on a `#161B63` dark section, drop to 4 — the tighter corner reads more precise against the dark surface and avoids the "bubble on dark" feel.
6. **Pills are 999 (full-radius).** Never 8, never 12. A pill with a 12px radius is a rectangle with rounded corners — not a pill.
7. **Never use a non-scale value.** If you're typing `border-radius: 10px`, stop — pick 8 or 12. If you're typing `border-radius: 20px`, you're off the scale entirely.
8. **Use named tokens, not raw values.** `border-radius: var(--radius-md)` — not `border-radius: 12px`. Keeps the system in sync if values ever adjust.

### The "if you remember one thing"

**Cards 12. Buttons 4. Inputs 8. Pills 999. Dark cards 4. Sections 0. Nothing else exists.**

---
## 12. CTA

**All CTAs use `design-system/components/cta.json` as-is.** Colour, radius,
size, border, typography, states — every property comes from the component
spec. No overrides, no variants, no surface-based flipping.

- Do not change the CTA's background colour based on which section it's in.
- Do not swap to white fill on primary banners.
- Do not use Shift's `#3940D0` on CTA fills — the CTA primary fill is
  whatever `cta.json` says.
- `--primary` (Shift indigo, from §3) is for section backgrounds and
  accents, **not** for CTAs.

If a design calls for a button treatment `cta.json` doesn't support, the
answer is to either pick a variant that does, or raise it with the ODS
team — never fork the component here.

---
## 13. Structure Library

**Where it lives:** `references/structure-library.md` — a curated set of **20 proven section patterns (S1–S20)**. Each structure documents a proven composition: column split, element order, visual treatment, recommended use cases.

**What it's for:** a menu of compositions the designer can reach for when building a page. Faster than freestyling, and the patterns are battle-tested across Zoho marketing pages — so pages built from the library already feel on-brand before anything is tuned.

**How to use it:**

1. **List the page's content beats** — hero, feature group A, deep-dives, feature group B, dark sections, CTA. Write them down.
2. **Open `references/structure-library.md`** and browse the 20 structures. Pick one that fits each beat.
3. **Build the section using the structure's documented layout** — element order, column split, visual treatment.
4. **Vary structure types across a page** to keep rhythm. Don't use the same structure three times in a row unless it's deliberate (e.g. a run of alternating deep-dives).

### Hard rules

1. **Use the library when it helps — not because you have to.** The structure library is a tool for the designer, not an audit gate. No required structure-map comment at the top of HTML output. No rebuild-on-failure rule.
2. **If nothing fits perfectly, adapt the closest one** rather than building from scratch. The library is built from what works — inventing a new layout usually produces something worse than the closest library fit.
3. **Don't repeat the same structure ID three times in a row** unless the rhythm is intentional. Variation across the page is how structures compose into a whole.
4. **When two structures both fit, pick the simpler one.** A hero with a single visual (S1) beats a hero with a media duo (S2) when the content doesn't justify two visuals.

### The "if you remember one thing"

**The Structure Library is a menu, not a gate. Open it when you're building a page — not because a rule says to, but because the answer is probably already in there.**

---
## 14. Dropdown Menu

**Scope:** the top-level nav dropdown on zoho.com/shifts — the mega-menu that opens below a nav label (Platform, Solutions, Resources, etc). This is the only dropdown the skill documents. Form selects and product-UI menus are out of scope.

### Pattern

A multi-column mega-menu that drops below the nav bar as one continuous panel. **2 to 4 columns** based on content — a small menu like "Resources" might be 2 columns; a big one like "Platform" can fill 4. Columns don't have to be equal widths — the content decides.

Each column is a group. Each group has an **uppercase eyebrow label** ("Ecosystem", "Main Features", "Resources") above a stack of items.

Each item is a single row: **icon tile (left) + title + one-line description**.

### Surface

| Element | Treatment |
|---|---|
| Background | White `#FFFFFF` |
| Radius | 12px (`--radius-md`) |
| Stroke | 1px solid `rgba(22,27,99,0.08)` |
| Shadow | `0 16px 40px -12px rgba(22,27,99,0.12)` — soft drop from above |
| Padding | `--space-5` (64px) top/bottom, `--space-4` (40px) left/right |
| Max width | 1200px (matches container), centered under the nav |

### Item row

```
┌──────┐  Title                       ← 16px / 500 / #161B63
│ icon │  One-line description         ← 14px / 400 / #55597A
└──────┘
```

| Element | Treatment |
|---|---|
| Icon tile | 40px square, 8px radius, accent-colored fill at full saturation (see §17 Accents) |
| Icon inside tile | 20px, stroke style, white or accent-text color |
| Title | 16px, 500 Medium, `#161B63`, single line |
| Description | 14px, 400 Regular, `#55597A`, max one line (truncate if longer) |
| Gap (icon → text) | 12px |
| Row internal padding | `--space-2` (16px) all around |
| Row gap (between items in a column) | `--space-1` (8px) |

### Group eyebrow label

`Ecosystem` / `Main Features` / `Resources` — uppercase, 12px, 500 Medium, `#55597A`, letter-spacing 0.04em. Sits directly above the first item in each column, spaced `--space-2` (16px) above the first row.

### Hover state — full row

Items get a full-row tinted background on hover (matches the references). Use `rgba(57,64,208,0.04)` as the hover fill — a very faint primary tint. The icon tile and text don't change; only the row background.

An optional trailing arrow (12px `→`) can appear on hover — lives on the right edge of the row, translates 4px right on hover like the CTA arrow rule (§12).

### Footer strip

Every dropdown ends with a **footer strip** running across the bottom — separated from the items by a 1px top border in `rgba(22,27,99,0.06)`. Holds **2–3 quieter ghost-style links** like "View demo", "Contact sales", "See pricing". Treatment:

- Font: 14px, 500 Medium, `#3940D0`
- No underline until hover; underline appears on hover
- Separated by a `|` divider at 50% opacity or by 32px gap — pick one and stick with it across all dropdowns
- Padding: `--space-3` (24px) vertical, `--space-4` (40px) horizontal

### Active nav label indicator

When a dropdown is open, the nav label that opened it needs a clear active state. **Pick one indicator and apply it consistently across every nav item on the site.** The three viable options:

| Option | Treatment |
|---|---|
| Underline | 2px solid `#3940D0` under the label, sits 6px below the text |
| Tinted pill | `rgba(57,64,208,0.08)` pill behind the label, 8px radius, matches label padding |
| Chevron rotate | Chevron next to label rotates 180° when open |

The skill doesn't mandate which one — but once picked, it's the same on every nav label on every page. Don't mix.

### Open/close interaction

- **Click to open on desktop.** Hover-to-open is unreliable and fails keyboard users.
- **Click outside or Esc to close.**
- **Tab through items** — first tab enters the first column's first item, arrow keys move within the menu.
- **The nav label is a `<button aria-expanded="…">`** — not a hover-triggered div.

On mobile, the nav collapses to a hamburger, and each top-level label expands inline (not as a floating panel) — showing the same columns stacked vertically with the same eyebrow labels and item rows. Open/close is handled by a chevron on each label row.

### Code reference

```css
.dropdown {
  position: absolute;
  top: 100%;
  left: 50%; transform: translateX(-50%);
  background: #FFFFFF;
  border: 1px solid rgba(22,27,99,0.08);
  border-radius: 12px;
  box-shadow: 0 16px 40px -12px rgba(22,27,99,0.12);
  padding: var(--space-5) var(--space-4);
  max-width: 1200px; width: max-content;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: var(--space-5);
}

.dropdown-group { display: flex; flex-direction: column; }
.dropdown-eyebrow {
  font-size: 12px; font-weight: 500; color: #55597A;
  text-transform: uppercase; letter-spacing: 0.04em;
  margin-bottom: var(--space-2);
}

.dropdown-item {
  display: flex; align-items: flex-start; gap: 12px;
  padding: var(--space-2);
  border-radius: 8px;
  transition: background 0.15s ease;
}
.dropdown-item:hover { background: rgba(57,64,208,0.04); }
.dropdown-item .icon-tile {
  flex-shrink: 0;
  width: 40px; height: 40px;
  border-radius: 8px;
  display: grid; place-items: center;
  /* accent fill picked from §17 */
}
.dropdown-item .title {
  font: 500 16px/1.4 'Puvi', sans-serif; color: #161B63;
}
.dropdown-item .desc {
  font: 400 14px/1.4 'Puvi', sans-serif; color: #55597A;
}

.dropdown-footer {
  margin-top: var(--space-3);
  padding-top: var(--space-3);
  border-top: 1px solid rgba(22,27,99,0.06);
  display: flex; gap: var(--space-5);
}
.dropdown-footer a {
  font: 500 14px/1 'Puvi', sans-serif; color: #3940D0;
  text-decoration: none;
}
.dropdown-footer a:hover { text-decoration: underline; }
```

### Hard rules

1. **2 to 4 columns, never more.** Wider menus stop reading as a menu and start reading as a page section.
2. **Every item is icon + title + description.** No icon-less items, no title-only items.
3. **Every column has an uppercase eyebrow label.** Even a one-column dropdown gets a label.
4. **White surface, 12px radius, 1px stroke, soft shadow.** No dark dropdowns, no gradient panels, no borderless floating menus.
5. **Hover = full-row tinted background.** Not just the text color change. The hover fill is the primary tint at 4% opacity.
6. **Footer strip is present on every dropdown.** Minimum 2 quieter links; maximum 3.
7. **One active-nav-label indicator across the whole site.** Pick underline, pill, or chevron — apply the same one everywhere. Don't mix.
8. **Click to open, never hover.** Keyboard accessibility first.
9. **Mobile: stacked columns with the same eyebrow labels and item rows.** Not a redesigned mobile menu pattern.

### The "if you remember one thing"

**White mega-menu, 2–4 columns, each column = eyebrow label + icon/title/description rows, footer strip with quieter links, click to open.**

---
## 15. Reference Websites

The skill uses two tiers of references, and they do different jobs.

### Tier 1 — Zoho benchmarks (the quality bar)

These are the pages every Shifts page must measure up to. They sit on the same domain, under the same brand, and reading as worse than them is what "fails the ship test" means (see §2 Senior Web Designer).

1. **[zoho.com/en-in/erp](https://www.zoho.com/en-in/erp/)** — **primary benchmark**. If the output can't sit next to this page on zoho.com without looking worse, it's not done.
2. **[zoho.com/in/payroll](https://www.zoho.com/in/payroll/)** — reference for product-page layout, feature grids, screenshot rhythm. The closest analog to Shifts in terms of product type (HR-adjacent, SMB-oriented).
3. **[zoho.com](https://www.zoho.com/)** — reference for overall Zoho tone, editorial balance, section spacing at the corporate level.

**How to use them:** when you're stuck on a decision (section rhythm, type size in context, spacing between groups, how a dark section sits between two white ones), open zoho.com/erp and see how that page solved the same problem. Match the craft level. Reach for the primary benchmark first, then the others.

**What this doesn't mean:** copy the ERP layout verbatim. The benchmark is the *feel* — the restraint, spacing, type confidence — not the literal section arrangement. Shifts has its own content and its own structures; the quality of the craft is what needs to match.

### Tier 2 — Non-Zoho inspiration (the craft bar)

These sites aren't the benchmark, but they're useful when the Zoho references don't cover a situation — a novel component, a micro-interaction, a way of treating whitespace that Zoho hasn't built yet. Learn from these; don't copy them.

1. **[Linear](https://linear.app)** — restraint, type confidence, dark-mode craft, micro-interactions. The closest non-Zoho reference for "quiet craft."
2. **[Stripe](https://stripe.com)** — editorial rigor, technical-product communication, docs quality, section rhythm over long pages.
3. **[Notion](https://notion.so)** — warmth, human tone, feature pages that stay readable instead of becoming feature-card walls.
4. **[Webflow](https://webflow.com)** — editorial craft at marketing-site scale, typographic confidence, big-moment sections that don't feel overdesigned.

**How to use them:** when you want to know how a great SaaS marketing team would approach a specific problem — a hero animation, a pricing comparison, a docs landing page — these are the reference points. Study *why* a choice works and then re-solve the problem in the Zoho Shifts visual language. Never copy a layout or a color system directly.

### Hard rules

1. **Zoho references are the quality bar. Non-Zoho references are inspiration only.** A Shifts page is judged against Zoho — not against Linear.
2. **Primary benchmark is zoho.com/en-in/erp/.** When a detail decision needs a sanity check, this is the first place to look.
3. **Non-Zoho references never drive decisions on color, type, pattern, banner treatment, or component style.** Those come from ODS and the rest of this skill. Non-Zoho references are for *compositional* and *craft* inspiration only — how whitespace is handled, how a tricky interaction flows, how a long page is paced.
4. **Don't reference a page that itself looks templated.** If the Zoho page you're benchmarking against is one of the weaker pages on the site, skip it and use zoho.com/erp instead.

### The "if you remember one thing"

**zoho.com/en-in/erp is the benchmark. Linear, Stripe, Notion, Webflow are inspiration — never the benchmark.**

---
## 16. Icons

**Library:** [Iconex](https://www.figma.com/design/1AoH3qZqIgyrSM0kY99vAf/Iconex---Freebie-icons--Community-?node-id=0-1) — a stroke-style icon set from the Figma Community. The whole site uses this one library. No mixing — not Lucide, not Phosphor, not Material, not custom one-offs. One library keeps every icon in visual agreement across the page.

If an icon doesn't exist in Iconex, either pick the closest match or request it — don't grab a substitute from another library, because stroke weight and proportions won't line up and the inconsistency shows.

### Style

**Stroke (outline) only.** No filled icons, no duotone, no 2-color. The outline style is what reads as "classic SaaS restraint" — consistent with the skill's warm-and-human register (§1) and the restrained quality bar (§2).

### Stroke weight

**2px everywhere.** Not 1px, not 1.5px. One weight across all sizes and contexts — nav, cards, CTAs, pills, dropdowns, product mocks. Don't mix weights within a page.

The 2px weight gives icons enough visual presence to hold their own next to the skill's bold headline typography and generous spacing — thinner weights read as timid against the page's confidence.

If you scale an icon up or down, keep the stroke visually at 2px — don't let it scale proportionally and get thicker at 32px or thinner at 16px. Use `vector-effect: non-scaling-stroke` on the SVG if needed. If Iconex ships at a different default weight, re-stroke the icons to 2px before using — don't ship them at the library default.

### Sizes

Four sizes — 16, 20, 24, 32 — picked by context, not by personal taste.

| Size | Use |
|---|---|
| **16px** | Inline with body text (trailing arrow in CTAs per §12, inline info icons in running text, small status indicators) |
| **20px** | Inside 40px icon tiles (dropdown items per §14, feature cards, nav items with icons) |
| **24px** | Standalone icons in content (feature callout icons, section-opener icons, slightly larger nav icons) |
| **32px** | Hero moments only (a single prominent icon in a hero feature card, or inside a 56–64px tile for a bold accent block). Rare. |

Nothing in between — no 18px, no 22px, no 28px. If a size doesn't fit one of the four, the surrounding component is probably wrong, not the icon.

### Color

**Single dark color only — `--secondary` `#161B63`.** Every icon on the site uses this one color. No blacks, no greys, no accent-colored icons, no "designer picks per icon" flexibility. One color, everywhere.

This matches the headline color used throughout the site (§3 Colour), so icons visually belong to the same family as the type — they read as part of the same typographic system rather than a separate decorative layer.

**The three exceptions** — narrow, specific, non-negotiable:

1. **On dark `#161B63` sections** — the icon can't be the same color as the background. Flip to `#FFFFFF` (white) on these sections. No other color is acceptable on dark.
2. **Status/state icons inside the product UI only** — inside a product screenshot, icons reflecting a state (green check for success, orange for warning, red for error) stay their status color, because they're part of the product, not the marketing page.
3. **CTA trailing arrow** — matches the CTA's text color per §12 (white on primary button, `#3940D0` on secondary/ghost). This is a CTA rule, not an icon rule; it's listed here so the two systems don't contradict.

**Not allowed as icon colors** — greys, blacks, `#000`, `--fg-tertiary`, accent colors (cyan, sky, royal blue, deep indigo), or any hex picked for a specific icon's "feel." The rule is absolute: `#161B63` on light, `#FFFFFF` on dark, status colors only inside the product, done.

**Icons inside accent-colored tiles** — the tile fill is the accent color; the icon inside stays `#FFFFFF` on a full-saturation tile, or `#161B63` on a light-fill tile. The icon itself never takes an accent color.

### Hard rules

1. **Iconex only.** No Lucide, Phosphor, Material, Heroicons, or custom icons. One library, one visual language.
2. **Stroke style only.** No filled icons, no duotone.
3. **2px stroke weight everywhere.** Don't let icons get visually heavier at larger sizes or thinner at smaller sizes — use `vector-effect: non-scaling-stroke` if needed. Re-stroke library icons to 2px if they ship at a different default.
4. **Four sizes: 16, 20, 24, 32.** Nothing else. Pick the size that matches the context, not the one that "feels right."
5. **Single icon color — `#161B63` on light surfaces, `#FFFFFF` on dark.** No greys, no accents, no per-icon color choices. Exceptions only for status icons inside product screenshots and for the CTA trailing arrow (which follows the CTA color rule, not the icon rule).
6. **Icons inside tiles are centered with equal padding.** A 20px icon in a 40px tile leaves 10px of padding on every side. Off-center icons are a tell of rushed work.
7. **Decorative icons get `aria-hidden="true"`.** Only icons that convey meaning (status, navigation, action) get a label. See §21 WCAG for the full accessibility rule.

### The "if you remember one thing"

**Iconex, stroke 2px, single color `#161B63` (white on dark). Four sizes: 16/20/24/32.**

---
## 17. Use of Accent Colours

**Four accents, sourced from ODS Shifts brand.** Everything about them — base hex, light-fill variant, text-on-light variant — comes from the ODS color system. Don't hand-roll accent tints.

### The four accents

| Accent | Name | Base 500 | Light 50 | Text 700 |
|---|---|---|---|---|
| `--accent-sharing` | **Cyan** | `#00B4D2` | `#E0F8FC` | `#007286` |
| `--accent-knowledge` | **Sky** | `#5A8CFF` | `#EEF3FF` | `#2A56BC` |
| `--accent-experience` | **Royal Blue** | `#2264DC` | `#E7EEFB` | `#144294` |
| `--accent-tech` | **Deep Indigo** | `#0A0046` | `#ECE9F6` | `#06002E` |

Full 11-stop scales (50 → 950) exist in the ODS system for each accent. The three above cover the common cases (light fill, base, text-on-light-fill) — reach for intermediates only when a specific pattern calls for them.

### What accents are for

**Both categorical and decorative.** Accents don't need to "mean something" to be used — they're a free tool for the designer to add color life across a page.

- **Categorical use** — when sections or cards represent different types of content (e.g. four features in a grid, each with its own icon tile color). Good: the accent reinforces the distinction. The designer can also reuse the same accent for the same feature across the site (Team/Messaging → Cyan on every page it appears) — this is helpful for recognition but not required.
- **Decorative use** — when a page just needs warmth and visual rhythm. A single accent tile beside a feature name, an accent-colored pull quote, an accent pattern behind a hero — all fine, even if the accent isn't "standing for" a category.

### No per-page cap

The old "max 2 accents per page" rule is gone. Designer picks per page. Common patterns:

- **A feature grid with 4 cards** can use all 4 accents — one per card tile. Not a rainbow, not amateur — it's the accents doing exactly what they're for.
- **A simple page** might use just one accent for an icon tile and nothing else. Also fine.
- **A busy page** that already has a lot of product UI visible might use zero accents — the UI's own colors carry the color life.

The test isn't a count — it's whether the page still reads as restrained (§2). If accents feel like noise, subtract; if the page feels monochrome and cold, add.

### Icon-tile pattern (surface-aware)

The most common accent use is inside 40px icon tiles (feature cards, dropdown items per §14, nav items). The tile treatment changes with the surface it sits on:

| Surface | Tile fill | Icon color |
|---|---|---|
| White / light gradient section | Light 50 (e.g. `#E0F8FC` for Cyan) | Base 500 (e.g. `#00B4D2` for Cyan) |
| Dark `#161B63` section | Base 500 (e.g. `#00B4D2` for Cyan) | White `#FFFFFF` |

On light surfaces, the tile is the soft fill and the icon carries the saturated color. On dark surfaces, the tile carries the saturated color (so it reads against the dark bg) and the icon flips to white. Don't use light-50 tiles on dark — they almost disappear.

### Other accent patterns

- **Accent pills/badges** — Base 500 fill + white text, or Light 50 fill + Text 700 text. Both are valid; pick one per page and stay with it.
- **Accent underline/highlight** — a 3px Base 500 underline below an H2 or callout header.
- **Accent pull quote** — Text 700 for the quote body, Base 500 for the quotation-mark glyph.
- **Accent section divider** — accents can replace primary blue on section dividers if the page's narrative calls for it.

### What accents never do

1. **Never replace Primary `#3940D0` on a CTA.** Primary CTAs stay `#3940D0`, full stop. Accents are not CTA fills.
2. **Never replace status colors.** Success/warning/error/info live in their own token set. An accent-colored "success" pill is wrong.
3. **Never mixed with status colors in the same card.** A card's icon tile is either an accent or a status — never both side-by-side.
4. **Never dimmed with alpha.** Accents appear at full saturation of their 500 value. No `rgba(0, 180, 210, 0.6)`. If a softer feel is wanted, use the Light 50 variant — don't tint the base.

### Hard rules

1. **Four accents — Cyan, Sky, Royal Blue, Deep Indigo.** No fifth accent. No "highlight" color.
2. **ODS tokens only.** `var(--accent-sharing)` — not a raw hex.
3. **Icon tiles change with surface** — light-50/icon-500 on white, base-500/white-icon on dark.
4. **Base 500 always at full saturation.** Never dimmed with alpha.
5. **Accents never replace primary or status colors.** They're a separate categorical/decorative layer.
6. **No per-page cap.** But still ask "does this page feel restrained?" — if not, subtract.
7. **Consistency across a page.** If you pick Cyan for the team-collaboration feature in the hero, use Cyan for that feature everywhere it appears on that page.

### The "if you remember one thing"

**Cyan, Sky, Royal Blue, Deep Indigo. Light fill on white, base fill on dark. Never as a CTA. No per-page cap — but stay restrained.**

---
## 18. Stock Image Rules

**Stock photography and stock illustrations are forbidden. No exceptions.** Stock kills the senior-designer quality bar and makes pages feel templated (§2). The moment a visual could appear on another SaaS site unchanged, the page is wrong.

This rule sits next to §9 Screenshot Rules — that item covers product UI (real product screenshots only), this item covers everything *else*: hero illustrations, customer stories, blog imagery, people, abstract concepts.

### What's forbidden, explicitly

- **All stock libraries:** Unsplash, Pexels, Pixabay, Shutterstock, iStock, Getty, Adobe Stock, Envato, 123RF, Depositphotos, freepik — any of them, any license tier, paid or free.
- **Generic SaaS photography** — "team around a laptop," "handshake," "smiling person at desk," "diverse group in bright office," "hands holding phone with app." You've seen all of them.
- **Isometric SaaS illustrations** — "people at desks with floating dashboards," "giant hand holding phone," "person with oversized chart next to them," cartoon coworkers in muted pastel palette.
- **Placeholder services** — placeholder.com, picsum.photos, lorempixel, even as temporary mockups. A production page should never ship with a placeholder URL, and testing pages shouldn't either.
- **Stock-looking AI** — AI-generated imagery that reproduces the generic-SaaS look (e.g. smiling AI coworkers, floating AI dashboards). The test is the same: if it could sit on another SaaS site unchanged, it fails.

### People — initials avatars only

Every person on a Shifts page — in a swap card, a shift assignment, a team list, a customer testimonial — is an **initials avatar**. Not a photo, not an AI face, not an illustration.

| Element | Treatment |
|---|---|
| Shape | 32px or 40px circle (999 radius per §11) |
| Fill | One of the four accent Base 500s (Cyan / Sky / Royal Blue / Deep Indigo) |
| Letters | Two uppercase initials, `#FFFFFF`, 500 Medium, centered |
| Size of letters | 14px in a 32px avatar, 16px in a 40px avatar |

Assign accent colors to avatars deliberately — a single swap card might have `AL` on Cyan and `JO` on Sky. Don't randomize. Don't reuse photos of people as placeholders. Initials only.

### When a page genuinely needs non-UI imagery

Some pages can't be carried by product screenshots alone — customer story pages, industry pages, brand storytelling. The allowed sources, in strict priority order:

1. **Real customer photography.** Brand team visits the customer's site (the restaurant, the retail store, the warehouse) and photographs real employees using the product. This is the default and the ideal.
2. **Brand-commissioned illustration.** An actual illustrator producing bespoke work in the Zoho Shifts visual language — warm palette, restrained, not generic-SaaS. Hire a real illustrator; don't describe "a flat-style illustration" to an AI and hope.
3. **AI-generated imagery** — only when neither of the above is possible, and only for specific situations:
   - Hero illustrations on product pages where a real photo doesn't exist yet.
   - Abstract-concept imagery in blog posts (e.g. "the future of work" — no real photo of that).
   - Background texture/mood images in editorial contexts.

   When AI is used, direct the generation to the skill aesthetic: warm tones, editorial lighting, restrained composition, primary blue as the single accent. Never generic corporate-SaaS prompts. Verify the output doesn't pass the "could be on any other SaaS site" test — if it could, regenerate or abandon.

### Photography direction (when it's real)

When real customer photography is commissioned, the direction:

- **Wide shots over close-ups** — show the environment (the restaurant floor, the warehouse aisle), not just a face.
- **Available light over studio light** — warm natural light is the aesthetic; hard flash kills it.
- **Real moments over posed shots** — a server mid-service, a manager on the floor — not a lineup facing camera.
- **Environmental context over generic office** — we're showing *their* workplace, not a Zoho office set.
- **No heavy retouching** — skin, hair, wrinkles stay human. Edited stock-photo polish reads as fake.

### The test

**"If the visual could appear on any other SaaS site unchanged, it fails."** Run this test on every image before it ships. If the answer is "yeah, it's pretty generic," the image is wrong — replace it, even if the page is otherwise done.

### Hard rules

1. **No stock libraries. No exceptions.** Unsplash, Pexels, Shutterstock, iStock, Getty, Adobe Stock, freepik, any of them.
2. **No generic SaaS photography or illustration.** Handshakes, office teams, isometric dashboards — none of it.
3. **No placeholder services** even in mockups or development. If content is pending, use a labeled `<div>` with `needs real imagery — commissioned by {date}`, not a placeholder URL.
4. **People = initials avatars on accent-colored circles.** Never photos of made-up people, never stock headshots, never AI faces.
5. **Real customer photography is the first choice for non-UI imagery.** Brand-commissioned illustration is second. AI is a last resort, tightly scoped.
6. **AI-generated imagery must pass the "unchanged on another SaaS site" test.** If it doesn't, regenerate or abandon.
7. **Every image gets meaningful alt text** (per §21 WCAG). "Stock photo of team" as alt text is both a stock violation and a WCAG violation.

### The "if you remember one thing"

**Stock is forbidden. People are initials avatars. Real customer photography first, commissioned illustration second, AI only as a tightly-scoped last resort.**

---
## 19. Logo

**The logo is the Zoho Shifts product wordmark** — the full "Zoho Shifts" text with the green + blue shield icon. Ships with this skill at `assets/logo.svg`.

This is the single approved product mark. Never re-type "Zoho Shifts" as plain text where a logo belongs, and never substitute a generic Zoho "Z" mark for it.

### Where the logo appears

| Location | Size |
|---|---|
| **Nav bar** (every page) — top-left, linked to `/shifts` | **28–32px** height |
| **Footer** — top of the footer block, above the link columns | **32–36px** height |
| **Docs sidebar header** — small variant, linked to `/shifts` | **24–28px** height |
| **Open Graph / social preview image** — centered on the solid primary banner with grid overlay | Context-sized |

That's it. The logo doesn't appear anywhere else on the site.

### Where the logo is NOT used

1. **Not inside hero H1 copy.** Hero headlines are editorial statements about scheduling, time tracking, etc. The logo already sits in the nav above; repeating it in the H1 is amateur.
2. **Not on the customer logo band.** The customer logo band shows *other companies* that use Shifts (e.g. brand logos at 60% opacity on dark `#161B63`). Never include the Shifts logo there.
3. **Not as a decorative element inside content sections.** Don't scatter the logo as a watermark, background pattern, or section divider. It only appears in chrome (nav, footer, docs sidebar, social meta).
4. **Not re-colored, rotated, stretched, or re-kerned.** The SVG ships in correct proportions — use it as-is.

### Implementation

Copy `assets/logo.svg` into the project's static asset folder (e.g. `public/images/shifts-logo.svg`). Reference with a standard `<img>` tag plus meaningful alt text:

```html
<!-- Nav bar -->
<a href="/shifts" class="nav-logo" aria-label="Zoho Shifts — home">
  <img src="/images/shifts-logo.svg" alt="Zoho Shifts" height="30">
</a>

<!-- Footer -->
<div class="footer-brand">
  <img src="/images/shifts-logo.svg" alt="Zoho Shifts" height="34">
</div>
```

Always render as SVG (not PNG) — vector scales cleanly. Set `height` explicitly and let `width` be auto so the wordmark never distorts. The supplied SVG is viewbox-correct at `0 0 780 296`.

### Dark surface treatment

The bundled logo is the dark wordmark on light backgrounds (nav on white, footer on light surface). When the logo needs to appear on a dark `#161B63` or `#3940D0` surface — social meta image, branded loading state, press kit — flip it with CSS:

```css
.logo-on-dark {
  filter: brightness(0) invert(1);
}
```

This flattens the green + blue icon to solid white along with the wordmark — that's the intended behavior for on-dark use. Don't hand-recolor the SVG.

### Favicon

The favicon (16×16, 32×32) is **not this logo**. The icon portion of the mark is handled separately in the Zoho Shifts favicon set — don't try to crop `assets/logo.svg` down to produce one. If a favicon is needed, use the dedicated favicon asset.

### Hard rules

1. **One approved logo: the product wordmark at `assets/logo.svg`.** No Zoho-generic "Z" substitution, no hand-typed "Zoho Shifts" text.
2. **SVG only, set `height` and let `width` auto.** Never PNG, never hand-scaled to arbitrary widths.
3. **Sizes:** nav 28–32px, footer 32–36px, docs sidebar 24–28px. Stay in-range.
4. **Never recolor, rotate, stretch, or re-kern.** Use the SVG as-is.
5. **Dark surfaces: flip via `filter: brightness(0) invert(1)`.** Don't edit the SVG.
6. **Chrome only:** nav, footer, docs sidebar, social meta. Never decoration, never in H1 copy, never on the customer logo band.
7. **Favicon is separate** — don't generate one by cropping the wordmark.
8. **Alt text:** `alt="Zoho Shifts"` on every instance (per §21 WCAG).

### The "if you remember one thing"

**Wordmark only, SVG only, nav 28–32 / footer 32–36, flip with CSS filter on dark. Chrome only.**

---
## 20. Animation & Hover

**Philosophy: quiet motion, two signature moments.** The default is no movement — pages sit still. Interaction triggers subtle state changes, and two specific spots on the site get slightly larger signature animations (the hero and the flowchart traveling-dash). Everything else is calm.

This matches the restrained creative register (§2) — animation is a finishing detail, never a headline.

### What moves, what doesn't

| Scope | Rule |
|---|---|
| Entrance / page load | **Nothing.** Content appears immediately. No fade-ups, no stagger, no scroll-triggered reveals. |
| Hover | Subtle state changes only. Covered below per component. |
| Active states | Instant (no transition needed). |
| Scroll | **No parallax, no pinned sections, no scroll-hijacking.** Page scrolls normally. |
| Signature moments | **Hero animation** (one per page, optional) and **flowchart traveling-dash** (on flowchart compositions only — see §22). |

### Hover rules by component

**Buttons (Primary / Secondary / Ghost)**
- Arrow icon translates 4px to the right, 200ms ease (§12).
- Background shifts slightly: primary `#3940D0 → #2C32A8`, secondary picks up a 6% primary tint fill, ghost gets an underline.
- No Y-translate on buttons.

**Cards (feature, pricing, content)**
- Background tint — a very faint primary fill (`rgba(57,64,208,0.04)`), 150ms ease.
- If the card has a trailing arrow, the arrow slides 4px right (same as buttons).
- **No Y-lift**, no shadow intensification, no border change. The tint is the entire hover treatment.

**Dropdown items** (§14)
- Full-row tint at `rgba(57,64,208,0.04)`, 150ms ease.
- Optional trailing arrow translates 4px right if present.

**Links (inline text links, footer links)**
- Underline appears on hover, color stays the same.
- 100ms ease on the underline.

**Icons that are buttons** (close button, menu toggle)
- Background circle fades in at `rgba(22,27,99,0.06)`, 150ms ease.
- Icon itself doesn't move.

### Signature moment 1 — Hero animation (optional, one per page)

If the hero includes a hero visual that benefits from life — a subtle float on the central product screenshot, a gentle opacity pulse on a highlighted data point — that's allowed. **One animated element maximum per hero.** Not three floating cards. Not a whole composition breathing.

```css
/* Example: a single product-UI element floats subtly */
@keyframes hero-float {
  0%, 100% { transform: translateY(0); }
  50%      { transform: translateY(-4px); }
}
.hero-float { animation: hero-float 4s ease-in-out infinite; }
```

Rules for the hero animation:
- 3–5 second cycle.
- Max 4px of displacement.
- Ease-in-out, infinite loop.
- Never more than one animated element in the hero.

### Signature moment 2 — Flowchart traveling dash (§22)

On flowchart compositions, one active connector line carries a traveling-dash animation to indicate "the flow is moving through here." Full spec lives in §22 Flow Chart Reference — not repeated here.

### What's forbidden

1. **No entrance animations on page load or scroll.** No "fade-up on scroll," no staggered section reveals, no scroll-triggered word-by-word text. These are the #1 tell of AI-written pages that want to look designed.
2. **No parallax, pinned sections, or scroll-hijacking.** The page scrolls at scroll speed.
3. **No rotation, scale, or color-cycling effects anywhere.** A card that rotates 2° on hover, an icon that scales 1.05 on hover, a background that pulses through hues — all wrong.
4. **No "shimmer" skeleton loaders styled as animations.** If a loader is needed it's a calm pulse, not a lens-flare animation.
5. **No wiggle, bounce, or spring easing.** Ease-in-out or linear only. No `cubic-bezier` with overshoot.

### Accessibility — `prefers-reduced-motion`

**Every animation must be wrapped in a reduced-motion guard.** Users who set `prefers-reduced-motion: reduce` at the OS level get no animation at all — not "less" animation, not "slower" animation. None.

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

This is non-negotiable — see §21 WCAG.

### Timing tokens

Four durations. Don't invent in-betweens.

| Duration | Use |
|---|---|
| 100ms | Link underlines, small color shifts |
| 150ms | Card/row hover tints, background changes |
| 200ms | Button/arrow translate |
| 400ms | Modal/dropdown open-close (rare) |

All use `ease` or `ease-in-out` — no overshoot, no bounce.

### Hard rules

1. **No entrance / scroll-triggered animations. Ever.** Pages appear instantly.
2. **Hover = background tint + arrow slide.** No lift, no shadow, no scale, no rotation.
3. **One animated element maximum in the hero.** Zero is fine. Two is wrong.
4. **Flowchart traveling-dash is the only line-animation in the system** and only in flowchart contexts (§22).
5. **Timing from the four-value scale (100/150/200/400ms).** No 300ms, no 500ms.
6. **Ease-in-out or ease — no overshoot, no spring.**
7. **`prefers-reduced-motion: reduce` kills all animation.** This is a WCAG requirement, not a preference.

### The "if you remember one thing"

**Pages don't animate on load. Hovers do a tint and slide. One hero animation max. Nothing else moves.**

---
## 21. WCAG Guidelines

**Base rules from ODS.** WCAG 2.1 AA requirements — contrast thresholds, focus states, keyboard accessibility, semantic HTML, error states with more than colour — are defined in `design-system/accessibility/rules.md`. This skill does not redefine them.

**Every page must pass WCAG 2.1 Level AA before shipping. No exceptions.**

Accessibility is non-negotiable and baked into the skill's tokens — the primary CTA (`#3940D0` on white), the three foreground text tokens (`--fg-primary`, `--fg-secondary`, `--fg-tertiary`), white text on solid primary at 75% opacity, and white text on dark `#161B63` at 75% opacity all pass 4.5:1 by default.

**One exception to watch:** `--fg-muted #969BC0` fails 4.5:1 on white. Use it only for decorative metadata or disabled states — never for readable text. Readable body copy uses `--fg-tertiary #55597A`.

### Full spec lives in `references/accessibility.md`

The reference file covers the 11 concern areas every page must address. The top-line rule of each, here, is enough to catch most issues at build time:

1. **Contrast** — ≥ 4.5:1 for body text, ≥ 3:1 for large text (≥24px) and for UI components (buttons, form borders, icons conveying meaning).
2. **Keyboard navigation** — every interactive element reachable by Tab, in a logical order. No keyboard traps. Dropdowns, modals, tabs all operable without a mouse.
3. **Focus states** — visible focus rings on every interactive element. Never `outline: none` without a replacement. Rings switch to white on primary/dark surfaces.
4. **Semantic HTML** — native elements first (`<button>`, `<a href>`, `<details>`, `<label>`). One `<h1>` per page, sequential heading hierarchy (no H1 → H3 jumps).
5. **ARIA** — only when native HTML can't express the pattern. `aria-label` on icon-only buttons, `aria-hidden="true"` on decorative SVGs, `aria-expanded` on disclosure toggles.
6. **Images and media** — alt text on every image (empty `alt=""` only for truly decorative). Captions for any video or animated content that conveys information.
7. **Motion** — `prefers-reduced-motion: reduce` respected on every animation (see §20). No auto-playing animations over 5 seconds without a pause control.
8. **Touch targets** — ≥ 44×44px on every tappable element. Spacing between tappable elements ≥ 8px so fingers don't hit the wrong one.
9. **Forms** — visible labels bound to inputs (`<label for="…">`). Error messages associated via `aria-describedby`. Required fields marked in a way that doesn't rely on color alone.
10. **Zoom and responsive** — content must reflow at 400% zoom without horizontal scroll. Text must resize to 200% without loss of content or function.
11. **Pre-ship testing** — keyboard-only walkthrough, screen-reader spot check (VoiceOver or NVDA on the hero and one product section), automated axe/Lighthouse scan, color-contrast verification on any hand-colored element.

**Read `references/accessibility.md` for the full spec** when building any new interactive component, form, modal, tab set, or surface treatment. It includes the pre-ship testing checklist — run it before calling the page done.

### Hard rules

1. **WCAG 2.1 AA is the baseline for every page.** AAA is welcome where easy; AA is required.
2. **Never `outline: none` without an immediate visible replacement.** The focus indicator must be at least as visible as the browser default.
3. **Never use color alone to convey meaning.** Status colors (success/warning/error) pair with an icon, label, or shape so colorblind users get the same signal.
4. **Never use `--fg-muted #969BC0` for readable text** on white. Fails 4.5:1. Use `--fg-tertiary` instead.
5. **Every interactive element ≥ 44×44px tap target.** Even if the icon looks 16px, the hit area wraps a 44px square.
6. **Every animation respects `prefers-reduced-motion`** (see §20).
7. **Every image has meaningful alt text** (per §18 Stock Image Rules — "stock photo of team" fails both accessibility and stock rules).
8. **Run the testing checklist in `references/accessibility.md` before shipping.** Ship-time, not build-time.

### The "if you remember one thing"

**WCAG 2.1 AA on every page. `references/accessibility.md` for the full spec. `--fg-muted` is decorative only — never for readable text.**

---
## 22. Flow Chart Reference

**Two flowchart styles exist.** Both are sequential — the user follows a path from start to end — but the visual treatment differs based on what the flow is *about*.

| Style | When to use it |
|---|---|
| **Style A — Screenshot flow** | User-facing flows: clock-in, shift swap request, leave approval, check-in sequence. The flow is about what happens in the product UI, so the steps are real product screenshots. |
| **Style B — Pill-node diagram** | System / conceptual flows: how Shifts connects to your existing stack, data flow between modules, integration architecture. Steps are labeled pill nodes, not UI screens. |

Pages don't mix the two styles in one flowchart. If the content shifts from "here's what the user sees" to "here's how the system works," that's two separate flowcharts.

---

### Style A — Screenshot Flow

**Nodes:** real product screenshots (per §9 Screenshot Rules). Each step shows the actual UI the user is looking at for that step of the flow. One screenshot per step, kept tight and cropped to just the relevant moment.

**Layout:** left-to-right horizontal sequence. Four steps max (Step 1 → Step 2 → Step 3 → Step 4). More than four gets cluttered — if the flow has more, split it into two flowcharts or rethink the narrative.

**Nodes treatment:** each screenshot follows §9 rules — radial-fade dotted zone around it (small version), 1px stroke, 4px radius (tight/compact per §9), bottom-edge shadow.

**Step labels:** a small text label above or below each screenshot — e.g. "Step 1 — Clock in", "Step 2 — GPS verify", "Step 3 — Confirmed" — 14px, 500 Medium, `--fg-secondary`. Keep labels short; no descriptions under them.

**Connectors:** see "Connectors" below.

**Active state:** one step in the flow is "current" — usually the moment the copy is describing ("When Alex clocks in at 09:02…"). The active screenshot gets a halo behind it:

```css
.flow-card--active {
  position: relative;
}
.flow-card--active::before {
  content: '';
  position: absolute; inset: -8px;
  border-radius: 12px;
  background: linear-gradient(135deg, #FFB3D9, #B3C9FF, #FFD4A3);
  opacity: 0.7;
  filter: blur(12px);
  z-index: -1;
}
```

One active card per flowchart — never two.

---

### Style B — Pill-Node Diagram

**Nodes:** pill-shaped labels (999 radius per §11). Each pill contains a 16px icon on the left + a short label. Pills can be single-line ("User", "API") or two-line ("Event Streaming Platform", "Real Time Inferences").

**Layout:** graph-style, not strictly linear. Nodes can branch above, below, or off to the side of the main row — wherever the system's shape calls for it. A "central" active node tends to sit right-of-center, with supporting nodes around it.

**Node treatment:** pull active/inactive states from ODS tokens.

- **Inactive pill** — transparent fill, 1px stroke (ODS neutral stroke token), label in `--fg-secondary`.
- **Active pill** — filled per ODS active-state tokens (typically a solid primary or light gradient fill), white or contrasted label.

Exact hex values come from the ODS Shifts brand system — don't hand-roll.

**Inline icon inside pill:** 16px, stroke style, 2px weight (per §16 Icons). Sits 12px from the left edge, 8px gap before the label starts.

**Pill sizing:**
- Height: 40px
- Padding: 12px left (with icon), 16px right
- Font: 14px, 500 Medium

**Line labels (optional):** small floating text next to a connector (e.g. "Activity" above the line from User → API). 12px, 400 Regular, `--fg-tertiary`. Use sparingly — one or two per diagram. More than three and the diagram becomes noisy.

---

### Connectors (both styles)

The line spec is the same across both styles:

| State | Treatment |
|---|---|
| Inactive connector | Solid 1px line, `#D4D4D8` |
| Active connector (one per flowchart) | Solid 1px line, `#3940D0` |
| Arrowheads | Small triangular arrowhead at the destination end, matching the line's color. 6px wide. |

Lines are solid (never dashed). Arrowheads are present on every connector — directed graphs only. No undirected lines.

**Corners on branching lines:** use an 8px rounded corner where the line changes direction. Not a sharp 90° angle.

```css
/* SVG connector — reference shape */
.flow-connector {
  stroke: #D4D4D8;
  stroke-width: 1;
  fill: none;
  stroke-linecap: round;
  stroke-linejoin: round;
}
.flow-connector--active {
  stroke: #3940D0;
}
```

---

### Animation (signature moment 2 — referenced from §20)

Only the **active edge** animates. Everything else is static.

**The traveling dash:** the active connector gets a moving dash pattern overlaid on its solid primary line — the dash travels from the source node toward the destination node on a loop, suggesting "the flow is moving through here."

```css
.flow-connector--active {
  stroke: #3940D0;
  stroke-width: 1;
  stroke-dasharray: 8 12;
  animation: flow-dash 3s linear infinite;
  fill: none;
}
@keyframes flow-dash {
  to { stroke-dashoffset: -100; }
}
```

**Optional status-dot pulse:** if the flow terminates in a status (green "Confirmed" dot on the active card, orange "Pending"), that dot pulses softly — 2s ease-in-out loop. Optional — not every flowchart needs it.

```css
@keyframes flow-pulse {
  0%, 100% { box-shadow: 0 0 0 0 rgba(5,180,136,0.45); }
  50%      { box-shadow: 0 0 0 7px rgba(5,180,136,0); }
}
.flow-dot--pulse { animation: flow-pulse 2s ease-in-out infinite; }
```

**Reduced motion:** per §20, all three animations (traveling dash, halo, pulse) are killed by `prefers-reduced-motion: reduce`. This is non-negotiable.

---

### Where flowcharts appear

- **Hero compositions** on product pages that explain how a specific feature works (how scheduling works, how clock-in works, how swaps are approved).
- **Explainer sections** mid-page — a dedicated flowchart section that walks through the process.
- **Integration pages** — Style B for system-level diagrams (Shifts + Payroll, Shifts + HR platform).

Flowcharts are not on every page. They're a specific tool for sequential/system content — when the page isn't about a process, don't force one.

---

### Hard rules

1. **Two styles only: Screenshot flow (A) and Pill-node diagram (B).** One style per flowchart.
2. **Style A** — real product screenshots per §9, 4-step max, left-to-right, 4px radius on each screenshot (tight).
3. **Style B** — pills with icon+label, 40px height, 999 radius, ODS tokens for active/inactive state. Lines can branch — not strictly linear.
4. **Connectors are solid lines with arrowheads.** Never dashed (until they animate). 1px, `#D4D4D8` inactive, `#3940D0` active.
5. **One active node per flowchart** — halo in Style A, ODS active-fill in Style B. Never two.
6. **Traveling-dash animation on the active edge only** — the signature flowchart animation. Never used anywhere else on the site (§20).
7. **`prefers-reduced-motion: reduce` kills all flowchart animation** — non-negotiable (§21).
8. **Rounded corners on branching lines** (8px radius on the turn). Not sharp 90° angles.

### The "if you remember one thing"

**Two styles: real screenshots for user flows, pill nodes for system diagrams. Solid 1px lines with arrowheads, grey inactive, primary active. One active node, one traveling dash. That's it.**

---