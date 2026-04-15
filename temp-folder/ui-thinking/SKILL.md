Apply bold, intentional design thinking before building any UI — Zoho or otherwise. Use this skill when asked to make a page, component, or interface that should feel distinctive, memorable, or "not like AI made it". Triggers on phrases like "make it bold", "give it a strong aesthetic", "make it unforgettable", "choose a design direction", "pick a style", "make it feel intentional", or "design thinking". Works alongside ods-visual-language (for ODS token enforcement) and frontend-design (for general UI craft). This skill answers the question: WHAT are we building, and WHY does it look the way it looks?

# UI Design Thinking Skill

**The mandate:** Before a single line of code, commit to a clear conceptual direction.
Bold maximalism and refined minimalism both work — the key is **intentionality, not
intensity.**

---

## Step 1 — Understand the Context

Answer these before designing:

| Question | Why it matters |
|---|---|
| **Purpose** | What problem does this interface solve? Who uses it? |
| **Audience** | Developer tool? Consumer product? Internal dashboard? B2B SaaS? |
| **Brand** | Zoho ODS? Custom brand? No brand (free expression)? |
| **Constraints** | Framework, accessibility, performance, screen sizes |

---

## Step 2 — Commit to a Tone

Pick ONE extreme and execute it with precision. Half-measures produce mediocre work.

| Aesthetic | Signals | Avoid pairing with |
|---|---|---|
| Brutally minimal | White space, 1 typeface, no decoration | Gradients, drop shadows |
| Maximalist / editorial | Layered type, dense grids, bold color blocks | Gentle pastels, rounded everything |
| Retro-futuristic | Monospace, scan-lines, terminal green, CRT glow | Friendly rounded corners |
| Organic / natural | Irregular shapes, warm earth tones, grain texture | Hard geometry, cold blues |
| Luxury / refined | Serif display, tight tracking, gold or cream, silence | Playfulness, motion overload |
| Playful / toy-like | Chunky rounded corners, bright primaries, bounce | Corporate seriousness |
| Editorial / magazine | Mixed type scales, overlapping elements, pull quotes | Boxy card grids |
| Brutalist / raw | Broken grid, unstyled borders, stark contrast | Softness of any kind |
| Art deco / geometric | Symmetry, ornamental lines, high contrast, gold | Organic curves |
| Soft / pastel | Muted tones, gentle shadows, airy spacing | High contrast, sharp angles |
| Industrial / utilitarian | Monospace, functional layout, no decoration | Decoration, illustration |

> **For Zoho ODS pages:** Tone governs composition, spacing density, motion character,
> and visual weight. It does NOT change brand tokens. Blue stays `#0047FF`. Font stays
> Zoho Puvi. See `ods-visual-language` skill for enforcement.

---

## Step 3 — Define the One Unforgettable Thing

Every great page has one moment that stops the user.

Ask: **"What's the one thing someone will remember after closing this tab?"**

Examples:
- A headline so large it fills the viewport
- A section background that shifts to pure black mid-scroll
- A product screenshot that bleeds to the edge of the screen
- A micro-animation that makes a button feel alive
- A color so confident it feels like a brand statement

**Choose one. Prototype it first. Build the rest of the page around it.**

---

## Step 4 — Validate Before Building

Quick checklist before writing code:

- [ ] I know the primary user and their context
- [ ] I've picked a single, named aesthetic tone
- [ ] I know the one unforgettable moment
- [ ] I know which constraints are non-negotiable
- [ ] I've rejected the "default AI aesthetic" (purple gradients, Inter font, card grid of 3)

---

## Skill Relationships

| Need | Use skill |
|---|---|
| ODS token values, typography, spacing, section rhythm | `ods-visual-language` |
| General frontend aesthetics, motion, color, layout craft | `frontend-design` |
| Full Zoho page templates with all sections | `zoho-webpage-design` |
| ODS component-level CSS (buttons, inputs) | `ods-design-system` |

**This skill = the thinking layer. The other skills = the execution layer.**