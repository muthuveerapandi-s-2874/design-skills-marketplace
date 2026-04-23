---
title: "Shift Product Rules"
purpose: "Product-level guardrails for Shift — token scope and component authority"
---

# PRODUCT — Shift

> Shift-specific guardrails that extend the global ODS design system.
> This file defines **rules only** — what Shift is allowed to touch and
> what it must not override.
>
> For visual direction (composition, motion, feel, example layouts,
> marketing-website design), see the separate `shift-visual-language` skill.

---

## System Usage

Always load, in this order:

1. `design-system/DESIGN.md` (from the submodule at repo root)
2. `design-system/themes/shift.json` (Shift theme tokens)
3. This file (Shift product rules)

---

## What Shift Customizes

Shift is allowed to influence **only**:

- Page and section backgrounds (Shift surfaces from `themes/shift.json`)
- Layout density and spacing rhythm — within the ODS scale, no new values
- Ambient colour treatment (tints and gradients at low opacity) using
  tokens from `design-system/themes/shift.json`

---

## What Shift Does NOT Customize

Shift must **not** override any component. These come from
`design-system/components/*.json` and are untouchable:

- **CTAs and buttons** — use `components/cta.json` as-is. Primary fill,
  hover, active, border, radius, size, typography, states all come from
  the component spec. Shift's `#3940D0` primary colour is for section
  backgrounds and accents, **never** for CTA fills.
- Inputs, selects, checkboxes, toggles
- Cards (the component itself; the surface *behind* a card may be Shift-themed)
- Typography system (sizes, weights, line-heights, tracking)

Component styles are controlled by the ODS design system alone.

---

## Surface Tokens

- Surface and background colours use tokens from
  `design-system/themes/shift.json`.
- Corner radii always come from ODS radius tokens — never arbitrary values.

---

## Usage Instructions (AI)

When generating UI for Shift:

1. Load global system rules from `design-system/DESIGN.md`.
2. Load Shift theme tokens from `design-system/themes/shift.json`.
3. Apply Shift-specific scope rules from this file (what may be themed).
4. Use canonical components from `design-system/components/*.json`
   **without modification**. CTAs, inputs, cards — all from the component
   JSONs, no overrides.
5. For visual direction (composition, motion, feel), consult the
   `shift-visual-language` skill.

---

## Restrictions

- Do **NOT** redefine tokens
- Do **NOT** override component styles (buttons, CTAs, inputs, cards, etc.)
- Do **NOT** change CTA colours based on surface or section
- Do **NOT** override the typography system
- Do **NOT** introduce new spacing values
- Do **NOT** hardcode colours

If a required token or rule is missing → **ASK**, do not substitute.