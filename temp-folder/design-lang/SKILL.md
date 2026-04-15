Apply Zoho's ODS visual language — composition, motion, cinematic spacing, warm palette, graphic elements, illustration, photography direction, and aesthetic craft — to pages that feel premium, editorial, and human. Use this skill whenever someone asks for a Zoho landing page, marketing page, or banner to "feel premium", "feel human", "look world-class", "use illustration", "add photography", "use warm colors", "use beige", "add texture", "add patterns", or "not look AI-generated". This skill governs HOW things are arranged, colored, illustrated, and animated — always using exact ODS tokens. Never override brand tokens.


# ODS Visual Language Skill

**The mandate:** Pages that feel like a senior human designer made them —
using *only* ODS brand tokens. The craft is in restraint, spatial rhythm,
typographic courage, and motion that earns its place.

---

## NON-NEGOTIABLE: ODS Brand Lock

These are **never** changed for visual style reasons:

| Token | Value | Rule |
|-------|-------|------|
| Font | `'Zoho Puvi', sans-serif` | No substitution ever |
| Primary | `#0047FF` (blue-500) | No other blue shades as primary |
| Body text | `#262626` (grey-900) | No custom dark colors |
| Subtle text | `#595959` (grey-500) | No custom mid-tones |
| Surface | `#F5F5F5` (grey-50) | No custom off-whites |
| Accent | `#09ABFF` (lightBlue-500) | Only for accents |
| Border radius | 2 / 4 / 8 / 16 / 160px | No arbitrary values |
| Btn radius | 4px always | Never pill, never 0 |

**What this skill changes:** composition, spacing scale, how type is sized
within ODS scale, motion, section rhythm, depth — not the tokens themselves.

---

## Part 1 — ODS Typography Used With Courage

The ODS type scale is large. Most pages undersell it. Premium pages use
the scale's full range — the H1 (88px) actually dominates the viewport.

### Exact ODS Tracking Values (from Figma — use these precisely)

| Size | Line-height | Tracking | Weight use |
|------|-------------|----------|------------|
| 88px (H1) | 96px | `-4%` = `-3.52px` | 500 or 700 |
| 80px (H2) | 88px | `-4%` = `-3.2px` | 500 |
| 72px (H3) | 80px | `-4%` = `-2.88px` | 500 |
| 64px (H4) | 72px | `-4%` = `-2.56px` | 600 |
| 56px (H5) | 64px | `-4%` = `-2.24px` | 500 |
| 48px (H6) | 56px | `-3%` = `-1.44px` | 500 |
| 40px (para/lg) | 48px | `-4%` = `-1.6px` | 400 |
| 24px (para/reg) | 32px | `-2%` = `-0.48px` | 400 |
| 20px (para/sm) | 28px | `-2%` = `-0.4px` | 400 |
| 16px (label) | 24px | `-2%` = `-0.32px` | 500 |

> Tracking in ODS is expressed as % of font-size. Convert: `88 × -0.04 = -3.52px`.

### Column Discipline — What Makes Type Feel Editorial
**Constraining headlines to a column width forces expressive line breaks.**
Even at 88px, a headline constrained to `max-width: 12–14ch` forces expressive
line breaks. Without this, even the right font size feels generic.

```css
/* Hero headline — ODS H1 with column control */
.hero-h1 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 88px;
  line-height: 96px;
  letter-spacing: -3.52px;      /* ODS exact: -4% of 88px */
  font-weight: 500;
  color: #262626;               /* ODS grey-900 */
  max-width: 14ch;              /* force meaningful line breaks */
}

/* Section headline — H2 with restraint */
.section-h2 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 80px;
  line-height: 88px;
  letter-spacing: -3.2px;       /* ODS -4% of 80px */
  font-weight: 500;
  color: #262626;
  max-width: 16ch;
}

/* Supporting body — never wider than 60ch */
.body-text {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 24px;
  line-height: 32px;
  letter-spacing: -0.48px;      /* ODS -2% of 24px */
  font-weight: 400;
  color: #595959;               /* ODS grey-500 */
  max-width: 60ch;
}

/* Eyebrow — premium signal above headlines */
.eyebrow {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.08em;       /* wide tracking on small label = premium */
  font-weight: 600;
  text-transform: uppercase;
  color: #0047FF;               /* ODS blue-500 */
}
```

### Type Hierarchy That Feels Human (not template)
- **ONE H1 per page.** Never more. It must dominate.
- **Eyebrow → H1 → body → CTA** is the sacred sequence. Don't skip levels.
- **Center-align headlines only** — body copy is always left-aligned.
- **Never float body copy at full container width** — `max-width: 60ch` always.

---

## Part 2 — Spatial Rhythm (The ODS Grid, Used Generously)

ODS grid has 40px margins at all breakpoints. The craft is in section padding
and vertical rhythm — this is where world-class pages feel different.

```css
:root {
  /* Section vertical padding — generous, cinematic */
  --section-xl:  160px;   /* hero, cinematic sections */
  --section-lg:  120px;   /* standard feature sections */
  --section-md:   80px;   /* tighter supporting sections */
  --section-sm:   56px;   /* compact bands (stats, logos) */

  /* Within-section vertical stack — using ODS spacing tokens */
  --stack-eyebrow-to-h1:  24px;   /* ODS Md-1 */
  --stack-h1-to-body:     40px;   /* ODS Md-3 */
  --stack-body-to-cta:    48px;   /* ODS Md-4 */
  --stack-cta-to-visual:  80px;   /* ODS Lg-2 */
}

.section { padding-block: var(--section-lg); }
.section-hero { padding-block: var(--section-xl); }

@media (max-width: 992px) {
  :root { --section-xl: 120px; --section-lg: 80px; }
}
@media (max-width: 768px) {
  :root { --section-xl: 80px; --section-lg: 56px; }
}
```

### The "Breathe" Test
When layout feels complete → add one more level of padding. Ask: does it feel
like it has room? The best pages are 60–80% empty by area. The content lands
harder because it's not competing with noise.

---

## Part 3 — Section Rhythm (The Page Has Chapters)

Alternating section backgrounds create contrast rhythm — each section feels
distinct. Use this exact sequence:

```
Hero        → white (#FFFFFF) — open, premier
Feature 1   → grey-50 (#F5F5F5) — grounded
Feature 2   → white (#FFFFFF) — return
Dark beat   → black (#000000) or blue-950 (#000719) — impact
Testimonial → white (#FFFFFF) — recovery, trust
CTA band    → blue-500 (#0047FF) — conversion close
Footer      → grey-50 (#F5F5F5) — grounded end
```

**Dark sections are not dark mode** — they're deliberate contrast beats.
One or two per page maximum. They make the surrounding white sections feel brighter.

```css
/* Dark beat section — premium moment */
.section-dark {
  background: #000000;          /* pure black = maximum contrast */
  color: #FFFFFF;
}
/* or softer navy for enterprise tone */
.section-dark-navy {
  background: #000719;          /* ODS blue-950 */
  color: #FFFFFF;
}

.section-dark h2 { color: #FFFFFF; }
.section-dark p  { color: rgba(255, 255, 255, 0.65); } /* NOT pure white — harsh */
.section-dark .eyebrow { color: #09ABFF; }             /* ODS lightBlue-500 on dark */

/* Dark glass card — enterprise/developer aesthetic */
.dark-card {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 8px;           /* ODS radius/md */
  padding: 40px;                /* ODS Md-3 */
  backdrop-filter: blur(8px);
  transition: background 300ms ease, border-color 300ms ease;
}
.dark-card:hover {
  background: rgba(255, 255, 255, 0.07);
  border-color: rgba(0, 71, 255, 0.4);   /* ODS blue-500 at 40% */
}
```

---

## Part 4 — The Cinematic Moment

Every page needs ONE section that stops the user cold. Choose one technique —
never combine. This is the section that feels hand-crafted.

### Technique A: Type Fills the Viewport
ODS H1 at full scale, centered on dark background. No illustration needed.
```css
.cinematic-type-section {
  min-height: 100vh;
  background: #000000;
  display: flex;
  align-items: center;
  justify-content: center;
  padding-inline: 40px;          /* ODS Br/Margin */
}
.cinematic-type-section h2 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 88px;               /* ODS H1 — maximum ODS scale */
  line-height: 96px;
  letter-spacing: -3.52px;       /* ODS -4% tracking */
  font-weight: 700;
  color: #FFFFFF;
  text-align: center;
  max-width: 14ch;
  /* Optional: gradient gives dimensional quality */
  background: linear-gradient(160deg, #FFFFFF 40%, #9AB6FF 100%); /* blue-200 */
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

### Technique B: Full-Bleed Visual + Anchored Text
Real product screenshot bleeds edge-to-edge. Text floats anchored bottom-left.
```css
.cinematic-bleed {
  position: relative;
  min-height: 80vh;
  overflow: hidden;
  border-radius: 0;              /* intentionally no radius at viewport edge */
}
.cinematic-bleed img {
  width: 100%; height: 100%;
  object-fit: cover;
  object-position: center top;
}
.cinematic-bleed .text-anchor {
  position: absolute;
  bottom: 64px; left: 64px;
  color: #FFFFFF;
  max-width: 480px;
  z-index: 2;
}
.cinematic-bleed::after {        /* scrim — darkens image bottom for text legibility */
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.65) 0%, transparent 55%);
}
```

### Technique C: Sticky Scroll Narrative
Visual stays fixed while feature copy scrolls past it. Most powerful for
multi-feature products. Requires JS to swap the visual per scroll-step.
```css
.sticky-narrative {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: start;
}
.sticky-panel {
  position: sticky;
  top: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px;
}
.scroll-steps { padding-block: 200px; }
.scroll-step {
  min-height: 70vh;
  display: flex;
  align-items: center;
  padding: 64px 48px;
}
```

### Technique D: Kinetic Marquee Strip
Running text strip between two sections — brand rhythm, not content.
```css
.marquee-strip {
  background: #0047FF;           /* ODS blue-500 */
  padding-block: 20px;
  overflow: hidden;
  white-space: nowrap;
}
.marquee-inner {
  display: inline-flex;
  gap: 80px;
  animation: marquee 22s linear infinite;
}
.marquee-inner span {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 20px;               /* ODS para/sm */
  font-weight: 600;
  color: #FFFFFF;
  letter-spacing: 0.04em;
}
@keyframes marquee {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}
```

### Technique E: Oversized Stat Escaping the Grid
One number so large it intentionally breaks out of its column. Creates tension.
```css
.stat-giant {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 88px;               /* ODS H1 */
  line-height: 96px;
  letter-spacing: -3.52px;
  font-weight: 700;
  color: #0047FF;                /* ODS blue-500 */
  margin-left: -24px;            /* intentional escape from column */
  display: block;
}
.stat-label {
  font-size: 20px;               /* ODS para/sm */
  line-height: 28px;
  color: #595959;                /* ODS grey-500 */
  margin-top: 12px;              /* ODS Sm-3 */
}
```

---

## Part 5 — Motion Principles

Motion must reveal, not decorate. Every animation should make content feel
*earned* when it appears — as if it arrived for a reason.

```css
:root {
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);  /* fast decel — cinematic feel */
  --ease-spring:   cubic-bezier(0.34, 1.56, 0.64, 1); /* subtle overshoot */
}

/* 1. Scroll reveal — standard for all content sections */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 700ms var(--ease-out-expo),
              transform 700ms var(--ease-out-expo);
}
.reveal.in-view { opacity: 1; transform: translateY(0); }

/* Stagger children — 80ms between each item */
.reveal-group > *:nth-child(1) { transition-delay:   0ms; }
.reveal-group > *:nth-child(2) { transition-delay:  80ms; }
.reveal-group > *:nth-child(3) { transition-delay: 160ms; }
.reveal-group > *:nth-child(4) { transition-delay: 240ms; }
.reveal-group > *:nth-child(5) { transition-delay: 320ms; }

/* 2. Card hover lift — uses ODS elevation/large shadow */
.card-lift {
  transition: transform 300ms var(--ease-out-expo),
              box-shadow 300ms var(--ease-out-expo);
  will-change: transform;
}
.card-lift:hover {
  transform: translateY(-6px);
  box-shadow: 0px 40px 80px -16px rgba(0, 0, 0, 0.16); /* ODS Elevation/large */
}

/* 3. ODS button press feel */
.btn { transition: transform 100ms ease, background-color 150ms ease; }
.btn:active { transform: scale(0.97); }

/* 4. Underline draw on text links */
.link-draw {
  background: linear-gradient(#0047FF, #0047FF) bottom / 0% 2px no-repeat;
  transition: background-size 250ms var(--ease-out-expo);
  padding-bottom: 2px;
}
.link-draw:hover { background-size: 100% 2px; }
```

```javascript
// Scroll reveal — activate .reveal elements as they enter viewport
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) entry.target.classList.add('in-view');
  });
}, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' });
document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));
```

### Motion Rules
- Scroll reveals only — no animations on page load
- All reveals travel **upward** (`translateY(40px)` → `0`) — never sideways or zoom
- `700ms` for content reveals — long decel feels cinematic, never rushed
- `300ms` for hover — fast enough to feel responsive
- Stagger at **80ms** per item — synchronised = PowerPoint, staggered = choreography
- **One cinematic technique per page** — chose from Part 4 and commit

---

## Part 6 — Layout Depth Tricks

These are composition techniques — no new colors or fonts introduced.

### The Bleed — makes pages feel bigger than the grid
```css
/* Screenshot overflows right edge of the viewport */
.bleed-right {
  margin-right: calc(-1 * (100vw - 100%) / 2);
  border-radius: 8px 0 0 8px;     /* ODS radius/md only on left side */
}

/* Visual overlaps into the next section */
.bleed-bottom {
  margin-bottom: -80px;            /* ODS Lg-2 — but negative */
  position: relative;
  z-index: 2;
}
```

### The Card Stack — depth illusion using CSS only
```css
.card-stack { position: relative; }
.card-stack::after {
  content: ''; position: absolute;
  inset: -8px -8px auto auto;      /* ODS Sm-2 */
  width: 100%; height: 100%;
  background: #FFFFFF;
  border-radius: 8px;              /* ODS radius/md */
  border: 1px solid #D1D1D1;      /* ODS grey-200 */
  z-index: -1; opacity: 0.6;
}
.card-stack::before {
  content: ''; position: absolute;
  inset: -16px -16px auto auto;   /* ODS Sm-4 */
  width: 100%; height: 100%;
  background: #FFFFFF;
  border-radius: 8px;
  border: 1px solid #D1D1D1;
  z-index: -2; opacity: 0.3;
}
```

### Stats Grid — editorial, structured
```css
.stats-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border-top: 1px solid #D1D1D1;  /* ODS grey-200 */
}
.stat-item {
  padding: 64px 48px;             /* ODS Md-6 / Md-4 */
  border-right: 1px solid #D1D1D1;
}
.stat-item:last-child { border-right: none; }
```

### Background Textures (max 5% opacity — never compete with content)
```css
/* Dot pattern — precision/enterprise feel */
.bg-dots {
  background-image: radial-gradient(circle, rgba(0,71,255,0.06) 1px, transparent 1px);
  background-size: 24px 24px;
}
/* Grid lines — structured, analytical */
.bg-grid {
  background-image:
    linear-gradient(rgba(0,71,255,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,71,255,0.04) 1px, transparent 1px);
  background-size: 48px 48px;
}
/* Radial glow — warmth for hero sections */
.bg-radial-blue {
  background:
    radial-gradient(ellipse 80% 60% at 65% 40%, #E4EDFF 0%, #FFFFFF 65%),
    radial-gradient(ellipse 40% 50% at 10% 80%, #E5F7FF 0%, transparent 60%);
  /* Uses ODS blue-50 and lightBlue-50 only */
}
```

---

## Part 7 — ODS Blue: Signal, Not Wallpaper

`#0047FF` is the most powerful element on the page. Use it like a highlighter —
the moment you deploy it becomes the most important thing the eye goes to.

| Correct use | Incorrect use |
|-------------|---------------|
| One word in a dark headline | Full headline in blue |
| Eyebrow label above H1 | Subtext paragraph in blue |
| Primary CTA button | Multiple blue elements competing |
| Full-width CTA band (once per page) | Multiple sections with blue bg |
| One icon in a feature group | All icons in blue |
| Left border on a testimonial card | Blue card backgrounds |

---

## Part 8 — What Makes It Look AI-Generated (Avoid These)

❌ H1 at 48px or less — ODS has 88px, use it  
❌ All sections the same padding height — alternate section-xl / section-lg / section-sm  
❌ Body copy centered at full container width — always `max-width: 60ch`, left-aligned  
❌ 3 equal-width cards repeated on every feature section — break the grid  
❌ Generic blue-to-purple gradients — only ODS blue-50 tints as backgrounds  
❌ Icons on every feature — sometimes numbers `01 / 02 / 03` are more editorial  
❌ Animations on page load — scroll reveal only, always  
❌ Placeholder illustrations — real product UI screenshots or real photos only  
❌ Two CTAs of identical visual weight — one primary, one ghost/secondary always  
❌ More than one cinematic technique per page — pick one and fully commit  

---

## Part 9 — Dark Cosmic + Glassmorphism Aesthetic

This pattern set captures a specific visual register: **dark atmospheric backgrounds,
glowing radial orbs, frosted glass product UI cards, and confident punchy headlines**.
All implemented using ODS tokens only — no new colors introduced.

### When to Use This Register
- AI-powered product pages
- Enterprise/SaaS product suites
- Sections where the product UI is the hero visual
- Pages targeting technical or enterprise buyers

---

### 9a — Cosmic Dark Hero

Dark hero where product UI floats inside a glowing atmospheric space.

```css
.hero-cosmic {
  background: #000719;               /* ODS blue-950 — deepest dark */
  position: relative;
  overflow: hidden;
  padding-block: 160px 0;
  padding-inline: 40px;
}

/* Radial glow orbs — using ODS blue palette only */
.hero-cosmic::before {
  content: '';
  position: absolute;
  width: 900px; height: 600px;
  top: -100px; left: 50%;
  transform: translateX(-50%);
  background:
    radial-gradient(ellipse 60% 50% at 30% 50%, rgba(0,71,255,0.35) 0%, transparent 70%),
    radial-gradient(ellipse 50% 40% at 70% 40%, rgba(9,171,255,0.2) 0%, transparent 65%);
  /* ODS blue-500 + lightBlue-500 at low opacity */
  pointer-events: none;
  z-index: 0;
}

.hero-cosmic-content {
  position: relative;
  z-index: 1;
  text-align: center;
  max-width: 900px;
  margin-inline: auto;
}

/* Badge pill — floats above headline */
.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;                           /* ODS Sm-2 */
  background: rgba(0,71,255,0.15);    /* ODS blue-500 at 15% */
  border: 1px solid rgba(0,71,255,0.3);
  border-radius: 160px;               /* ODS radius/round */
  padding: 8px 16px;                  /* ODS Sm-2 / Sm-4 */
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 16px;
  font-weight: 500;
  color: #9AB6FF;                     /* ODS blue-200 — soft on dark */
  margin-bottom: 32px;
}

/* Multi-statement headline — alternating bright/dim lines */
.hero-cosmic h1 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 80px;                    /* ODS H2 — slightly smaller for multi-line */
  line-height: 88px;
  letter-spacing: -3.2px;            /* ODS -4% of 80px */
  font-weight: 600;
  color: #FFFFFF;
  max-width: 14ch;
  margin-inline: auto;
}

/* Each statement line separated — not one run-on */
.hero-cosmic h1 .line-dim {
  color: rgba(255,255,255,0.45);     /* dimmed lines create rhythm */
}

.hero-cosmic p {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 24px;
  line-height: 32px;
  letter-spacing: -0.48px;           /* ODS -2% of 24px */
  color: rgba(255,255,255,0.6);
  max-width: 56ch;
  margin-inline: auto;
  margin-top: 32px;
}
```

**Headline pattern** — alternating bright / dim lines creates a statement rhythm:
```html
<h1>
  <span class="line-bright">The #1 AI platform.</span>
  <span class="line-dim">The next-gen workspace.</span>
  <span class="line-bright">One seamless suite.</span>
</h1>
```

---

### 9b — Floating Product UI in Dark Space

Product screenshot floats above the dark hero — slightly luminous, with a glow halo.

```css
.hero-product-float {
  position: relative;
  margin-top: 80px;
  z-index: 1;
  border-radius: 8px 8px 0 0;        /* ODS radius/md — only top corners */
  overflow: hidden;

  /* Luminous glow behind the product — ODS blue-500 at low opacity */
  filter: drop-shadow(0 0 80px rgba(0,71,255,0.25))
          drop-shadow(0 40px 80px rgba(0,0,0,0.6));
}

.hero-product-float img {
  width: 100%;
  display: block;
  border-radius: 8px 8px 0 0;
}

/* Frosted edge — product fades into the hero bg at bottom */
.hero-product-float::after {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 120px;
  background: linear-gradient(to bottom, transparent, #000719);
}
```

---

### 9c — Dark Glass Feature Card

Cards that feel like frosted glass floating in dark space. For feature grids on dark bg.

```css
.glass-card-dark {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 8px;                 /* ODS radius/md */
  padding: 40px;                      /* ODS Md-3 */
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(12px);
  transition: border-color 300ms ease, background 300ms ease;
}

/* Subtle top-edge glow on hover */
.glass-card-dark:hover {
  border-color: rgba(0,71,255,0.35);  /* ODS blue-500 */
  background: rgba(255,255,255,0.06);
}
.glass-card-dark::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg,
    transparent,
    rgba(0,71,255,0.5) 50%,           /* ODS blue-500 */
    transparent
  );
  opacity: 0;
  transition: opacity 300ms ease;
}
.glass-card-dark:hover::before { opacity: 1; }

.glass-card-dark .card-icon {
  width: 48px; height: 48px;
  background: rgba(0,71,255,0.15);    /* ODS blue-500 tint */
  border-radius: 8px;
  display: flex; align-items: center; justify-content: center;
  margin-bottom: 24px;
}
.glass-card-dark .card-label {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #09ABFF;                     /* ODS lightBlue-500 */
  margin-bottom: 12px;
}
.glass-card-dark h3 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 24px;
  line-height: 32px;
  letter-spacing: -0.48px;
  font-weight: 600;
  color: #FFFFFF;
  margin-bottom: 16px;
}
.glass-card-dark p {
  font-size: 20px;
  line-height: 28px;
  color: rgba(255,255,255,0.55);
}
```

---

### 9d — Tabbed Feature Section

One product visual area, tabs switch the feature shown. The most characteristic
section pattern — communicates depth without overwhelming the user.

```css
.feature-tabs-section {
  padding-block: 120px;
}

.tab-nav {
  display: flex;
  gap: 4px;
  margin-bottom: 48px;
  border-bottom: 1px solid #D1D1D1;   /* ODS grey-200 */
  padding-bottom: 0;
}

.tab-btn {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 16px;
  font-weight: 500;
  color: #595959;                     /* ODS grey-500 */
  background: none;
  border: none;
  padding: 12px 24px;
  cursor: pointer;
  position: relative;
  border-bottom: 2px solid transparent;
  margin-bottom: -1px;
  transition: color 200ms ease;
}
.tab-btn.active {
  color: #0047FF;                     /* ODS blue-500 */
  border-bottom-color: #0047FF;
}
.tab-btn:hover:not(.active) {
  color: #262626;                     /* ODS grey-900 */
}

.tab-panel { display: none; }
.tab-panel.active { display: grid; grid-template-columns: 5fr 7fr; gap: 80px; align-items: center; }

/* Dark variant — same structure, dark bg */
.feature-tabs-dark .tab-nav {
  border-bottom-color: rgba(255,255,255,0.1);
}
.feature-tabs-dark .tab-btn       { color: rgba(255,255,255,0.4); }
.feature-tabs-dark .tab-btn.active { color: #FFFFFF; border-bottom-color: #0047FF; }
.feature-tabs-dark .tab-btn:hover:not(.active) { color: rgba(255,255,255,0.7); }
```

---

### 9e — Inline Testimonial (No Card Border)

Testimonial presented as pure typography — no card, no box. More editorial, more trusted.

```css
.testimonial-inline {
  padding-block: 80px;
  max-width: 800px;
  margin-inline: auto;
  text-align: center;
}
.testimonial-inline blockquote {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 32px;
  line-height: 40px;
  letter-spacing: -0.96px;           /* ODS -3% of 32px */
  font-weight: 400;
  color: #262626;                    /* ODS grey-900 */
  margin: 0 0 32px;
}
/* On dark sections */
.section-dark .testimonial-inline blockquote {
  color: #FFFFFF;
}
.testimonial-author {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
.testimonial-author img {
  width: 48px; height: 48px;
  border-radius: 160px;              /* ODS radius/round */
  object-fit: cover;
}
.testimonial-author-name {
  font-size: 16px;
  font-weight: 600;
  color: #262626;
  letter-spacing: -0.32px;
}
.testimonial-author-role {
  font-size: 16px;
  font-weight: 400;
  color: #595959;                    /* ODS grey-500 */
}
```

---

### 9f — Competitor Comparison Bar

Horizontal bar chart comparing metrics. Use for competitive ranking or stat comparisons.

```css
.compare-bars {
  display: flex;
  flex-direction: column;
  gap: 24px;
  max-width: 600px;
}
.compare-row {
  display: grid;
  grid-template-columns: 120px 1fr 48px;
  align-items: center;
  gap: 16px;
}
.compare-label {
  font-size: 16px;
  font-weight: 500;
  color: #262626;
  text-align: right;
}
.compare-bar-track {
  height: 8px;
  background: #EBEBEB;               /* ODS grey-100 */
  border-radius: 160px;              /* ODS radius/round */
  overflow: hidden;
}
.compare-bar-fill {
  height: 100%;
  border-radius: 160px;
  background: #0047FF;               /* ODS blue-500 — our brand */
  transition: width 800ms cubic-bezier(0.16, 1, 0.3, 1);
}
.compare-bar-fill.competitor {
  background: #D1D1D1;               /* ODS grey-200 — muted for competitors */
}
.compare-value {
  font-size: 16px;
  font-weight: 600;
  color: #0047FF;
}
.compare-value.competitor { color: #595959; }
```

---

### 9g — Section Banner Image (Atmospheric Divider)

Full-width atmospheric image used as a section opener — not hero, not background.
Use between major content sections to create visual breathing room.

```css
.section-banner {
  width: 100%;
  aspect-ratio: 16/5;                /* wide cinematic crop */
  overflow: hidden;
  border-radius: 16px;               /* ODS radius/lg */
  margin-block: 80px;
}
.section-banner img {
  width: 100%; height: 100%;
  object-fit: cover;
  object-position: center;
}

/* Optional: subtle dark overlay for text legibility if copy floats over it */
.section-banner-overlay {
  position: relative;
}
.section-banner-overlay::after {
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(to right,
    rgba(0,7,25,0.7) 0%,             /* ODS blue-950 */
    rgba(0,7,25,0.2) 50%,
    transparent 100%
  );
  border-radius: 16px;
}
```

---

### 9h — Dark + Light Section Rhythm

Dark atmospheric sections alternating with clean white sections — more
dramatic than the standard grey-50 / white flip:

```
Hero         → blue-950 (#000719) — cosmic dark, glowing
"Built to work together" → white — clean contrast recovery  
Helpdesk     → grey-50 (#F5F5F5) — structured, enterprise  
Fin AI       → blue-950 (#000719) — dark again — product drama  
One Suite    → white — trust, convergence  
CTA          → blue-500 (#0047FF) — conversion  
```

**Key rule:** Dark sections open with a **full-width atmospheric banner image**,
then content below. White sections lead directly with type. Never the opposite.

---

## Part 10 — Page-Level Layout Structures

These are complete **page structure blueprints** — how sections stack, how grids
split, how the eye travels top to bottom. Each is drawn from a distinct visual
register. Use one blueprint per page and build every section within it.

---

### Blueprint A — Product Homepage

**Rhythm:** Bold split hero → category selector → horizontal product strip →
alternating feature rows → social proof → full-width CTA

```
┌─────────────────────────────────────────────────────────────────┐
│  NAV — logo left, links center, CTA right                       │
├──────────────────────────────┬──────────────────────────────────┤
│                              │                                  │
│  HERO TEXT                   │  HERO VISUAL (photography        │
│  [eyebrow]                   │  collage or product photo)       │
│  H1 88px bold                │                                  │
│  left-aligned, max 10ch      │  Real photography — NOT UI       │
│  [body 24px, 48ch max]       │  screenshots. Lifestyle imagery. │
│  [Primary CTA] [Ghost CTA]   │                                  │
│                              │  Slightly larger than 50% col.   │
│  cols: 5 text | 7 visual     │                                  │
├──────────────────────────────┴──────────────────────────────────┤
│  CATEGORY SELECTOR — horizontal pill nav                        │
│  [Food & Bev] [Retail] [Services] [Beauty]  ← click to swap    │
│  Content area below swaps per selected category                 │
├─────────────────────────────────────────────────────────────────┤
│  PRODUCT STRIP — horizontal scroll                              │
│  [Product 1] [Product 2] [Product 3] [Product 4]  → scroll →   │
│  Each card: product image top, name + price below               │
├─────────────────────────────────────────────────────────────────┤
│  FEATURE ROW A — text left, visual right (7:5)                  │
├─────────────────────────────────────────────────────────────────┤
│  FEATURE ROW B — visual left, text right (5:7)  grey-50 bg      │
├─────────────────────────────────────────────────────────────────┤
│  STATS BAND — 3–4 oversized numbers, white bg, grey-200 borders │
├─────────────────────────────────────────────────────────────────┤
│  TESTIMONIALS — 2-col quote cards, grey-50 bg                   │
├─────────────────────────────────────────────────────────────────┤
│  FULL-WIDTH CTA BAND — blue-500 bg, white type                  │
├─────────────────────────────────────────────────────────────────┤
│  FOOTER — grey-50 bg                                            │
└─────────────────────────────────────────────────────────────────┘
```

**Key CSS — Category Selector**
```css
.category-nav {
  display: flex;
  gap: 8px;                          /* ODS Sm-2 */
  flex-wrap: wrap;
  margin-bottom: 48px;               /* ODS Md-4 */
}
.category-pill {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 16px;
  font-weight: 500;
  color: #595959;                    /* ODS grey-500 */
  background: #F5F5F5;               /* ODS grey-50 */
  border: 1px solid #D1D1D1;        /* ODS grey-200 */
  border-radius: 160px;              /* ODS radius/round */
  padding: 12px 24px;                /* ODS Sm-3 / Md-1 */
  cursor: pointer;
  transition: all 200ms ease;
}
.category-pill.active,
.category-pill:hover {
  background: #0047FF;               /* ODS blue-500 */
  color: #FFFFFF;
  border-color: #0047FF;
}

.category-panel { display: none; }
.category-panel.active { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
```

**Key CSS — Horizontal Product Scroll Strip**
```css
.product-strip {
  display: flex;
  gap: 24px;                         /* ODS Md-1 */
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
  padding-block: 8px;
  scrollbar-width: none;
}
.product-strip::-webkit-scrollbar { display: none; }

.product-card {
  flex: 0 0 280px;
  scroll-snap-align: start;
  background: #FFFFFF;
  border: 1px solid #EBEBEB;         /* ODS grey-100 */
  border-radius: 8px;                /* ODS radius/md */
  padding: 24px;                     /* ODS Md-1 */
  transition: box-shadow 250ms ease;
}
.product-card:hover {
  box-shadow: 0px 16px 24px -4px rgba(0,0,0,0.25); /* ODS Elevation/small */
}
.product-card img { width: 100%; aspect-ratio: 1/1; object-fit: contain; margin-bottom: 16px; }
.product-card-name { font-size: 20px; font-weight: 600; color: #262626; }
.product-card-desc { font-size: 16px; color: #595959; margin-top: 8px; }
```

---

### Blueprint B — Product Suite Page

**Rhythm:** Dark cosmic hero → clean white "how it works" → dark feature section →
tabbed product deep-dive → social proof → second dark product section → white CTA

```
┌─────────────────────────────────────────────────────────────────┐
│  NAV — transparent on dark hero, sticky                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  COSMIC HERO — blue-950 bg, radial glows                        │
│  [badge pill]                                                   │
│  H1 multi-line, centered, bright/dim alternation               │
│  [subtext 24px, 56ch, rgba white 0.6]                          │
│  [Primary CTA] [Ghost CTA]                                      │
│                                                                 │
│  Product UI screenshot floating below — glowing, bleed bottom  │
│                                                                 │
├─────────────────────────────────────────────────────────────────┤
│  "HOW IT WORKS" — white bg                                      │
│  H2 centered, then 3-col explanation grid                       │
│  Each col: icon + short H5 + body-sm                            │
├─────────────────────────────────────────────────────────────────┤
│  SECTION BANNER — full-width atmospheric image, radius/lg       │
├─────────────────────────────────────────────────────────────────┤
│  TABBED FEATURE DEEP-DIVE — grey-50 bg                          │
│  H2 left + body left + tab nav                                  │
│  Tab panel: label + H3 + body + link | product screenshot right │
├─────────────────────────────────────────────────────────────────┤
│  STATS + SOCIAL PROOF — white bg                                │
│  Comparison bars left | testimonial inline right                │
├─────────────────────────────────────────────────────────────────┤
│  DARK FEATURE SECTION — blue-950 bg                             │
│  Section banner image → glass cards grid below                  │
├─────────────────────────────────────────────────────────────────┤
│  "ONE PLATFORM" CTA — white bg                                  │
│  H2 centered, subtext, two CTAs                                 │
├─────────────────────────────────────────────────────────────────┤
│  FOOTER — grey-50                                               │
└─────────────────────────────────────────────────────────────────┘
```

**Key CSS — Transparent Sticky Nav**
```css
.nav-suite {
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 20px 40px;
  transition: background 300ms ease, box-shadow 300ms ease;
}
.nav-suite.on-dark {
  background: transparent;
  color: #FFFFFF;
}
.nav-suite.scrolled {
  background: rgba(0, 7, 25, 0.9);   /* ODS blue-950 at 90% */
  backdrop-filter: blur(12px);
  box-shadow: 0 1px 0 rgba(255,255,255,0.08);
}
/* JS: add .scrolled when window.scrollY > 60 */
```

---

### Blueprint C — Single Product Page

**Rhythm:** Product identity hero → horizontal highlight carousel → sticky product nav →
individual feature sections (one feature per section, full-screen) → spec grid → buy CTA

```
┌─────────────────────────────────────────────────────────────────┐
│  STICKY NAV — product name left, anchor links center, buy right │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  PRODUCT IDENTITY HERO                                          │
│  Product category (small, grey-500)                             │
│  Product name (H1 88px, centered, tight tracking)               │
│  Tagline (H5 56px, centered, grey-500)                          │
│  [CTA] below tagline                                            │
│                                                                 │
│  Full-bleed product photo BELOW text — edge-to-edge            │
│  Product centered, no border, no shadow on white bg             │
│                                                                 │
├─────────────────────────────────────────────────────────────────┤
│  HIGHLIGHTS CAROUSEL — "Get the highlights"                     │
│  Scroll tabs: [Feature 1] [Feature 2] [Feature 3]...            │
│  Below: scrollable card panels (scroll-snap, horizontal)        │
│  Each card: large visual top, short copy bottom                 │
├─────────────────────────────────────────────────────────────────┤
│  FEATURE SECTION 1 — full viewport height                       │
│  H2 centered + subtext → visual below (full-bleed photo)        │
│  Background alternates: white → black → white → black           │
├─────────────────────────────────────────────────────────────────┤
│  FEATURE SECTION 2 — split (text + large detail visual)         │
├─────────────────────────────────────────────────────────────────┤
│  SPEC HIGHLIGHTS — white bg                                     │
│  Clean number grid: 4 specs in a row                            │
│  [number large] [unit small] [label below]                      │
├─────────────────────────────────────────────────────────────────┤
│  BUY SECTION — product photo + name + price + CTA button        │
├─────────────────────────────────────────────────────────────────┤
│  FOOTER                                                         │
└─────────────────────────────────────────────────────────────────┘
```

**Key CSS — Product Identity Hero**
```css
.hero-product-identity {
  padding-top: 80px;
  padding-inline: 40px;             /* ODS Br/Margin */
  text-align: center;
  background: #FFFFFF;
}
.hero-product-identity .product-category {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 20px;
  line-height: 28px;
  letter-spacing: -0.4px;
  font-weight: 500;
  color: #595959;                   /* ODS grey-500 */
  margin-bottom: 8px;
}
.hero-product-identity h1 {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 88px;
  line-height: 96px;
  letter-spacing: -3.52px;         /* ODS -4% of 88px */
  font-weight: 600;
  color: #262626;
  margin-bottom: 16px;
}
.hero-product-identity .tagline {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 56px;
  line-height: 64px;
  letter-spacing: -2.24px;         /* ODS -4% of 56px */
  font-weight: 500;
  color: #595959;                  /* ODS grey-500 — tagline is always quieter */
  max-width: 18ch;
  margin-inline: auto;
  margin-bottom: 40px;
}
.hero-product-identity .hero-image {
  width: 100vw;
  margin-left: calc(-50vw + 50%);  /* full bleed from centered container */
  margin-top: 64px;
  display: block;
}
```

**Key CSS — Highlight Scroll Carousel**
```css
.highlights-section { padding-block: 80px 0; }
.highlights-section > h2 {
  font-size: 64px;                  /* ODS H4 */
  line-height: 72px;
  letter-spacing: -2.56px;
  font-weight: 500;
  text-align: center;
  margin-bottom: 40px;
}
.highlights-tab-nav {
  display: flex;
  gap: 0;
  overflow-x: auto;
  border-bottom: 1px solid #D1D1D1; /* ODS grey-200 */
  scrollbar-width: none;
}
.highlights-tab-nav::-webkit-scrollbar { display: none; }
.highlights-tab {
  flex: 0 0 auto;
  font-size: 16px;
  font-weight: 500;
  color: #595959;
  padding: 12px 24px;
  white-space: nowrap;
  border-bottom: 2px solid transparent;
  cursor: pointer;
  transition: all 200ms ease;
}
.highlights-tab.active {
  color: #0047FF;                   /* ODS blue-500 */
  border-bottom-color: #0047FF;
}
/* Scroll panels */
.highlights-panels {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scrollbar-width: none;
  gap: 0;
}
.highlights-panels::-webkit-scrollbar { display: none; }
.highlight-panel {
  flex: 0 0 100%;
  scroll-snap-align: start;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
  padding: 80px 40px;
}
.highlight-panel .panel-visual img {
  width: 100%;
  border-radius: 8px;               /* ODS radius/md */
}
```

**Key CSS — Individual Feature Sections (full viewport, alternating bg)**
```css
.feature-section-full {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-block: 120px;
  padding-inline: 40px;
  text-align: center;
}
.feature-section-full.on-white { background: #FFFFFF; }
.feature-section-full.on-black {
  background: #000000;
  color: #FFFFFF;
}
.feature-section-full.on-black h2 { color: #FFFFFF; }
.feature-section-full.on-black p  { color: rgba(255,255,255,0.65); }

.feature-section-full h2 {
  font-size: 72px;                  /* ODS H3 */
  line-height: 80px;
  letter-spacing: -2.88px;         /* ODS -4% of 72px */
  font-weight: 500;
  max-width: 16ch;
  margin-inline: auto;
  margin-bottom: 24px;
}
.feature-section-full .feature-visual {
  width: 100%;
  max-width: 1200px;
  margin-top: 64px;
  border-radius: 8px;               /* ODS radius/md */
  overflow: hidden;
}
```

**Key CSS — Spec Highlights Grid**
```css
.spec-highlights {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0;
  border-top: 1px solid #D1D1D1;   /* ODS grey-200 */
  border-bottom: 1px solid #D1D1D1;
  padding-block: 64px;
}
.spec-item {
  text-align: center;
  padding-inline: 40px;
  border-right: 1px solid #D1D1D1;
}
.spec-item:last-child { border-right: none; }
.spec-number {
  font-size: 64px;                  /* ODS H4 */
  line-height: 72px;
  letter-spacing: -2.56px;
  font-weight: 700;
  color: #262626;
}
.spec-unit {
  font-size: 32px;
  letter-spacing: -0.96px;
  font-weight: 500;
  color: #262626;
  vertical-align: super;
}
.spec-label {
  font-size: 16px;
  line-height: 24px;
  color: #595959;
  margin-top: 8px;
}
```

---

### Blueprint D — Sticky Product Sub-Nav

Used in all three pages. Product page anchor nav that sticks below the main nav.

```css
.product-subnav {
  position: sticky;
  top: 0;
  z-index: 90;
  background: rgba(255,255,255,0.9);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid #EBEBEB; /* ODS grey-100 */
  padding: 0 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.product-subnav-links {
  display: flex;
  gap: 0;
}
.product-subnav-link {
  font-family: 'Zoho Puvi', sans-serif;
  font-size: 16px;
  font-weight: 500;
  color: #595959;
  padding: 20px 24px;
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: color 200ms ease, border-color 200ms ease;
}
.product-subnav-link:hover,
.product-subnav-link.active {
  color: #262626;
  border-bottom-color: #262626;
}
.product-subnav-cta {
  /* Uses ODS btn-primary, size sm */
}
/* On dark hero: invert */
.product-subnav.on-dark {
  background: rgba(0,7,25,0.85);    /* ODS blue-950 */
  border-bottom-color: rgba(255,255,255,0.08);
}
.product-subnav.on-dark .product-subnav-link { color: rgba(255,255,255,0.6); }
.product-subnav.on-dark .product-subnav-link:hover { color: #FFFFFF; border-bottom-color: #FFFFFF; }
```

---

### Choosing the Right Blueprint

| Your page type | Use Blueprint |
|---|---|
| Company homepage / product overview | A — Product Homepage |
| Multi-product suite / platform page | B — Product Suite |
| Single product feature page | C — Product Page |
| Any page with scroll navigation | D — Sticky Sub-Nav |

**Blueprints can mix sections** — e.g. Blueprint C can use the dark cosmic hero from
Blueprint B, or the category selector from Blueprint A as a feature switcher.

---

## Part 11 — Extended Warm Palette (Beyond White/Grey/Blue)

ODS contains warm tokens that most pages never use. These are permitted for
**section backgrounds and surface tints only** — never for text, borders on
interactive elements, or brand touchpoints. They create the "warm, human,
editorial" register that pure grey/white pages lack.

### Approved Warm Surface Tokens (from ODS Figma)

| Token | Hex | Name | Use |
|-------|-----|------|-----|
| `Orange/50` | `#FFF5E5` | Warm Sand | Warm section bg, hero tint |
| `Orange/100` | `#FFEBCB` | Deep Sand | Prominent warm section |
| `Yellow/50` | `#FFFCEB` | Warm Cream | Subtle warm surface |
| `DeepOrange/50` | `#FFEEE5` | Warm Blush | Editorial accent sections |
| `Yellow/100` | `#FFF9DB` | Rich Cream | Testimonial / quote bg |
| `Orange/200` | `#FFD99E` | Amber Tint | Decorative / illustration bg only |

> **Rule:** Warm surfaces are for backgrounds only. All text on them uses
> `Grey/900 #262626` or `Grey/500 #595959`. Never put `#0047FF` primary
> on a warm bg — use `Grey/900` or `Blue/950` instead for CTAs.

---

### Warm Palette Section Rhythm

Mix warm, cool, and neutral sections to create temperature contrast — the
same way dark/light contrast creates visual drama:

```
Hero           → White or Blue/950 (cool anchor)
"How it works" → Orange/50 #FFF5E5 (warm sand — human, approachable)
Feature rows   → White (reset)
Deep-dive      → Yellow/50 #FFFCEB (warm cream — editorial)
Social proof   → White or Grey/50
CTA band       → Blue/500 #0047FF (cool, high-energy conversion)
Footer         → Grey/900 #262626 (dark neutral close)
```

**Never** place two warm sections back to back — always separate with white or grey/50.

---

### CSS: Warm Section Backgrounds

```css
/* Section: Warm Sand */
.section-warm-sand {
  background: #FFF5E5;               /* ODS Orange/50 */
}

/* Section: Warm Cream */
.section-warm-cream {
  background: #FFFCEB;               /* ODS Yellow/50 */
}

/* Section: Deep Sand — stronger warmth */
.section-warm-deep {
  background: #FFEBCB;               /* ODS Orange/100 */
}

/* Warm blush — editorial / testimonial use */
.section-warm-blush {
  background: #FFEEE5;               /* ODS DeepOrange/50 */
}

/* Warm card on warm bg — slightly deeper tint */
.card-on-warm {
  background: rgba(255, 245, 229, 0.6); /* Orange/50 at 60% on white */
  border: 1px solid #FFD99E;            /* ODS Orange/200 */
  border-radius: 8px;                   /* ODS radius/md */
}
```

---

### Warm Gradient Backgrounds (section hero tints)

These use only ODS warm tokens — never custom hex values:

```css
/* Warm radial — like a soft morning light, for product hero sections */
.bg-warm-radial {
  background:
    radial-gradient(ellipse 70% 55% at 60% 30%, #FFF5E5 0%, #FFFFFF 70%),
    radial-gradient(ellipse 40% 40% at 10% 80%, #FFFCEB 0%, transparent 65%);
  /* Orange/50 + Yellow/50 */
}

/* Warm + cool merge — brand energy with human warmth */
.bg-warm-cool-merge {
  background:
    radial-gradient(ellipse 50% 60% at 80% 20%, #E4EDFF 0%, transparent 60%),  /* Blue/50 */
    radial-gradient(ellipse 60% 50% at 20% 70%, #FFF5E5 0%, transparent 60%),  /* Orange/50 */
    #FFFFFF;
}

/* Warm amber — rich editorial, use sparingly */
.bg-warm-amber {
  background: linear-gradient(160deg, #FFEBCB 0%, #FFF5E5 50%, #FFFFFF 100%);
  /* Orange/100 → Orange/50 → white */
}
```

---

## Part 12 — Graphic Elements: Illustrations, Patterns, SVG Shapes

These are **CSS-native or inline SVG** graphic elements — no image dependencies.
They add visual richness without photography and without generic AI stock art.

---

### 12a — Abstract Organic Blob (Painterly Background Shape)

Soft, irregular blob shapes that feel hand-drawn. Used as section background
decoration, positioned behind product UI or text.

```css
/* Blob — pure CSS using border-radius morph technique */
.blob {
  position: absolute;
  border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  opacity: 0.18;
  pointer-events: none;
  animation: blob-morph 12s ease-in-out infinite;
}

/* Warm blob — for use on white or warm sections */
.blob-warm {
  background: #FFD99E;               /* ODS Orange/200 */
  width: 600px;
  height: 480px;
}

/* Blue blob — for use on white or dark sections */
.blob-blue {
  background: #9AB6FF;               /* ODS Blue/200 */
  width: 500px;
  height: 420px;
}

/* Cool accent blob */
.blob-lightblue {
  background: #6BCEFF;               /* ODS Lightblue/300 */
  width: 400px;
  height: 360px;
}

@keyframes blob-morph {
  0%,100% { border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%; }
  25%      { border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%; }
  50%      { border-radius: 50% 60% 30% 40% / 40% 50% 70% 60%; }
  75%      { border-radius: 40% 30% 60% 70% / 60% 40% 50% 30%; }
}

/* Usage: position behind content */
.section-with-blob {
  position: relative;
  overflow: hidden;
}
.blob-top-right {
  top: -80px;
  right: -120px;
}
.blob-bottom-left {
  bottom: -60px;
  left: -100px;
}
```

---

### 12b — SVG Painterly Stroke (Underline / Highlight)

Hand-drawn SVG underline or circle to highlight a key word in a headline.
Editorial feel — feels human, not mechanical.

```html
<!-- Squiggly underline under a key word -->
<h2>
  The smarter way to
  <span class="highlight-word">
    connect
    <svg class="word-underline" viewBox="0 0 120 12" preserveAspectRatio="none">
      <path d="M2,9 C20,3 40,11 60,5 C80,0 100,10 118,6"
        fill="none"
        stroke="#0047FF"
        stroke-width="3"
        stroke-linecap="round"/>
    </svg>
  </span>
  with customers.
</h2>
```

```css
.highlight-word {
  position: relative;
  display: inline-block;
}
.word-underline {
  position: absolute;
  bottom: -6px;
  left: 0;
  width: 100%;
  height: 12px;
  overflow: visible;
}

/* Animated draw-in on scroll reveal */
.word-underline path {
  stroke-dasharray: 150;
  stroke-dashoffset: 150;
  transition: stroke-dashoffset 600ms cubic-bezier(0.16, 1, 0.3, 1) 400ms;
}
.revealed .word-underline path {
  stroke-dashoffset: 0;
}

/* Warm variant — on warm bg sections */
.word-underline-warm path { stroke: #FF9E08; } /* ODS Orange/500 */
```

---

### 12c — SVG Background Patterns

Pure SVG patterns as section backgrounds. Subtle, geometric, editorial.
Always ≤5% opacity so they don't compete with content.

```css
/* ① Dot grid — classic, works on any bg */
.pattern-dots {
  background-image: radial-gradient(circle, #D1D1D1 1.5px, transparent 1.5px);
  /* ODS Grey/200 */
  background-size: 28px 28px;
}
/* On dark sections */
.pattern-dots-dark {
  background-image: radial-gradient(circle, rgba(255,255,255,0.12) 1.5px, transparent 1.5px);
  background-size: 28px 28px;
}

/* ② Line grid — technical, data-forward pages */
.pattern-grid {
  background-image:
    linear-gradient(rgba(209,209,209,0.4) 1px, transparent 1px),
    linear-gradient(90deg, rgba(209,209,209,0.4) 1px, transparent 1px);
  /* ODS Grey/200 */
  background-size: 40px 40px;
}

/* ③ Diagonal stripe — energetic, CTA sections */
.pattern-diagonal {
  background-image: repeating-linear-gradient(
    45deg,
    transparent,
    transparent 18px,
    rgba(0,71,255,0.04) 18px,     /* ODS Blue/500 at 4% */
    rgba(0,71,255,0.04) 20px
  );
}

/* ④ Warm dot grid — for Orange/50 sections */
.pattern-dots-warm {
  background-image: radial-gradient(circle, #FFD99E 1.5px, transparent 1.5px);
  /* ODS Orange/200 */
  background-size: 28px 28px;
  opacity: 0.5;
}

/* ⑤ Concentric rings — hero depth, centered on focal point */
.pattern-rings {
  background-image:
    radial-gradient(circle, transparent 20%, transparent 21%, rgba(0,71,255,0.03) 21.5%, transparent 22%),
    radial-gradient(circle, transparent 35%, transparent 36%, rgba(0,71,255,0.03) 36.5%, transparent 37%),
    radial-gradient(circle, transparent 50%, transparent 51%, rgba(0,71,255,0.03) 51.5%, transparent 52%);
  background-size: 600px 600px;
  background-position: center;
}
```

---

### 12d — Illustrated Section Dividers (SVG wave / torn edge)

SVG shapes that create organic transitions between sections instead of flat edges.

```html
<!-- Wave divider — placed at bottom of a section to transition into next -->
<div class="section-divider-wave">
  <svg viewBox="0 0 1440 80" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <!-- Fill with the NEXT section's background color -->
    <path d="M0,40 C240,80 480,0 720,40 C960,80 1200,0 1440,40 L1440,80 L0,80 Z"
      fill="#FFF5E5"/>
    <!-- ODS Orange/50 — if next section is warm sand -->
  </svg>
</div>
```

```css
.section-divider-wave {
  position: absolute;
  bottom: -1px;
  left: 0;
  width: 100%;
  line-height: 0;
  overflow: hidden;
}
.section-divider-wave svg {
  display: block;
  width: 100%;
  height: 80px;
}
```

**Color map for divider fill:**
| Transitioning into | Fill color |
|---|---|
| White section | `#FFFFFF` |
| Warm sand section | `#FFF5E5` (Orange/50) |
| Warm cream section | `#FFFCEB` (Yellow/50) |
| Grey surface section | `#F5F5F5` (Grey/50) |
| Dark section | `#000719` (Blue/950) |

---

### 12e — Floating Illustration Cards (Abstract + Product UI Mix)

Editorial cards that mix abstract geometric shapes with product UI. Used in
feature grids on warm-section backgrounds.

```css
.illustration-card {
  background: #FFFFFF;
  border-radius: 16px;               /* ODS radius/lg */
  padding: 40px;                     /* ODS Md-3 */
  position: relative;
  overflow: hidden;
  box-shadow: 0px 16px 24px -4px rgba(0,0,0,0.08); /* ODS Elevation/small at 8% */
}

/* Decorative blob behind the card illustration */
.illustration-card .card-blob {
  position: absolute;
  width: 200px;
  height: 200px;
  border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  top: -40px;
  right: -40px;
  opacity: 0.15;
  pointer-events: none;
}
.illustration-card .card-blob-warm { background: #FFD99E; } /* Orange/200 */
.illustration-card .card-blob-blue { background: #9AB6FF; } /* Blue/200 */

/* Abstract geometric shape inside card */
.card-geo {
  width: 80px;
  height: 80px;
  border-radius: 8px;                /* ODS radius/md */
  margin-bottom: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.card-geo-warm { background: #FFF5E5; } /* Orange/50 */
.card-geo-blue { background: #E4EDFF; } /* Blue/50 */
```

---

## Part 13 — Photography Direction

Photography makes or breaks the "human" quality of a page. These rules define
which types of stock photography fit the visual register and how to use them.

---

### 13a — Photography Categories by Section Type

| Section | Photography type | What to avoid |
|---|---|---|
| Hero | Environmental / workspace — real place, real light | Studio white bg, generic handshakes |
| Feature row | In-context product use — person using the software | Posed smiling faces only, stock clichés |
| Testimonial | Head-and-shoulders portrait, natural light, slight bg blur | Tiny thumbnail, dark/harsh light |
| "Team / culture" | Real office spaces, candid moments, group energy | Perfect symmetry, stock agency faces |
| CTA band | Abstract close-up texture / material — fabric, concrete, light | Generic blue sky, stock business |
| Dark section | Dramatic cinematic portrait or aerial — high contrast | Bright cheerful stock photos |

---

### 13b — Photography Framing Rules

**Warm sections (Orange/50 bg):**
- Use warm-lit photography — golden hour, indoor ambient, wooden surfaces
- Subject should face or angle toward the text, not away
- Leave 40% of the image as low-detail space for text overlay

**Dark sections (Blue/950 bg):**
- Photography in dark sections must have dark tone — no bright cheerful imagery
- Use a `mix-blend-mode: luminosity` + dark overlay to desaturate bright photos
- Apply an ODS blue-950 overlay at 40–60% opacity to unify photography with section bg

**White / neutral sections:**
- Photography should have neutral or cool light — daylight, overcast
- Avoid warm-tinted photography on white bg — the colour temperature conflict reads as an accident

---

### 13c — CSS: Photography Treatments

```css
/* Standard editorial treatment — slight desaturate + contrast lift */
.photo-editorial {
  filter: contrast(1.05) saturate(0.9);
  border-radius: 8px;                /* ODS radius/md */
  object-fit: cover;
}

/* Dark section treatment — luminosity blend over dark bg */
.photo-on-dark {
  mix-blend-mode: luminosity;
  opacity: 0.7;
  filter: contrast(1.1);
}

/* Warm treatment — slight warmth tint via sepia hint */
.photo-warm {
  filter: contrast(1.02) saturate(1.05) sepia(0.06);
}

/* Overlay for dark sections — applied via ::after on wrapper */
.photo-dark-overlay {
  position: relative;
  border-radius: 8px;
  overflow: hidden;
}
.photo-dark-overlay::after {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 7, 25, 0.45);  /* ODS Blue/950 at 45% */
  border-radius: 8px;
}

/* Warm overlay — for landing on warm sections */
.photo-warm-overlay::after {
  background: rgba(255, 235, 203, 0.25); /* ODS Orange/100 at 25% */
}

/* Split image — left half sharp, right half bleeds to edge */
.photo-bleed-right {
  width: calc(100% + 40px);          /* overflows ODS margin */
  margin-right: -40px;
  border-radius: 8px 0 0 8px;        /* ODS radius/md — left side only */
}
```

---

### 13d — Photography Aspect Ratios by Use

```css
/* Hero photo — landscape, cinematic */
.photo-hero    { aspect-ratio: 16 / 9; }

/* Feature row visual — square or slightly taller */
.photo-feature { aspect-ratio: 4 / 3; }

/* Portrait testimonial */
.photo-avatar  { aspect-ratio: 1 / 1; border-radius: 160px; } /* ODS radius/round */

/* Section banner — very wide, cinematic strip */
.photo-banner  { aspect-ratio: 21 / 6; }

/* Card photo — consistent across card grids */
.photo-card    { aspect-ratio: 3 / 2; }

/* Full viewport — hero image background */
.photo-fullvp  {
  width: 100%; height: 100vh;
  object-fit: cover;
  object-position: center 30%;       /* slightly above center for people shots */
}
```

---

### 13e — Combining Illustration + Photography

The most premium pages mix real photography with abstract graphic elements —
photography for humanity, illustration for brand voice.

**Pattern: Photo + Blob overlay**
```css
/* Photo card with decorative blob behind it — creates depth */
.photo-with-blob {
  position: relative;
  display: inline-block;
}
.photo-with-blob .blob {
  position: absolute;
  z-index: -1;
  transform: translate(24px, 24px); /* offset behind photo */
}
.photo-with-blob img {
  position: relative;
  z-index: 1;
  border-radius: 8px;                /* ODS radius/md */
}
```

**Pattern: Illustration frame around product UI screenshot**
```css
/* Product UI sits on a warm gradient card, with SVG deco in corner */
.ui-illustration-frame {
  background: linear-gradient(135deg, #FFF5E5 0%, #FFFFFF 60%);
  /* Orange/50 → white */
  border-radius: 16px;               /* ODS radius/lg */
  padding: 40px;
  position: relative;
  overflow: hidden;
}
.ui-illustration-frame .deco-circle {
  position: absolute;
  width: 160px;
  height: 160px;
  border-radius: 160px;              /* ODS radius/round */
  background: #E4EDFF;               /* ODS Blue/50 */
  opacity: 0.6;
  top: -40px;
  right: -40px;
}
.ui-illustration-frame img {
  width: 100%;
  border-radius: 8px;                /* ODS radius/md */
  box-shadow: 0px 16px 24px -4px rgba(0,0,0,0.15);
}
```

---

## Skill Relationships

- **Exact token values** (hex, px, weights) → `ods-design-system` skill
- **Button / input component CSS** → `ods-design-system` skill
- **Full page templates with all sections** → `zoho-webpage-design` skill

**This skill = visual craft decisions. All tokens come from ODS. Never override brand.**