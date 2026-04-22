---
title: "Shift Product Theme"
purpose: "Product behavior and UI direction for Shift"
---

# PRODUCT — Shift

> This file defines the behavior and visual direction for the Shift product.
> It extends the global ODS design system without overriding it.

---

## System Usage

Always load, in this order:

1. `design-system/DESIGN.md` (from the submodule at repo root)
2. `design-system/themes/shift.json` (Shift theme tokens)
3. This file (Shift product behavior)

---

## Theme Identity

- **Product:** Shift
- **Mode:** Dark
- **Tone:** Focused, minimal, productivity-driven
- **Visual Style:** Clean, low-noise interface

---

## UI Behavior

- Prefer **dark backgrounds** and deep surfaces
- Use the ODS **primary color for actions and highlights**
- Maintain **high contrast for readability**
- Reduce visual clutter and distractions

---

## Layout Guidelines

- Use spacious layouts with clear hierarchy
- Prioritize content over decoration
- Keep alignment strict and grid-based

---

## What Shift Customizes

Shift is allowed to influence **only**:

- Page and section backgrounds (Shift dark surfaces)
- Layout density and spacing rhythm (within the ODS scale)
- Ambient color treatment — tints and gradients at low opacity using
  Shift theme tokens from `design-system/themes/shift.json`

---

## What Shift Does NOT Customize

Shift must **not** override any component. All of the following come from
`design-system/components/*.json` and are untouchable:

- Buttons and CTAs
- Inputs, selects, checkboxes, toggles
- Cards (component-level; surface background may be set via layout)
- Typography system (sizes, weights, line-heights, tracking)

Component styles are controlled by the ODS design system alone.

---

## Surface Treatment (Backgrounds Only)

- Use the dark surface tokens defined in `themes/shift.json` (e.g.
  `--shift-surface-800`, `--shift-surface-900` — use the actual token
  names from the theme file).
- Subtle elevation; avoid heavy shadows.
- Corner radii always come from ODS radius tokens — never arbitrary.

---

## Interaction Style

- Smooth and minimal transitions
- Avoid flashy animations
- Focus on usability and speed

---

## Usage Instructions (AI)

When generating UI for Shift:

1. Load global system rules from `design-system/DESIGN.md`.
2. Load Shift theme tokens from `design-system/themes/shift.json`.
3. Apply Shift-specific behavior from this file (backgrounds, layout,
   ambient treatment only).
4. Use canonical components from `design-system/components/*.json` without
   modification.
5. Maintain consistency across all components and surfaces.

---

## Restrictions

- Do **NOT** redefine tokens
- Do **NOT** override component styles (buttons, inputs, cards, etc.)
- Do **NOT** override the typography system
- Do **NOT** introduce new spacing values
- Do **NOT** hardcode colors

If a required token or rule is missing → **ASK**, do not substitute.

---

## Notes

Shift UI should feel:

- Calm
- Focused
- Professional
- Distraction-free