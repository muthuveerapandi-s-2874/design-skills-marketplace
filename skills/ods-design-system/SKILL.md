---
name: ods-design-system
description: >
  Apply Zoho ODS design tokens, components, and themes when building any UI,
  landing page, dashboard, or component. Enforces strict token usage from the
  local ODS design system — never invents colors, sizes, radii, or typography.
  Use whenever the request involves Zoho UI, ODS, a design system, building a
  component, a landing page, a dashboard, or any web page design.
triggers:
  - zoho ui
  - ods
  - design system
  - build ui
  - create component
  - landing page
  - dashboard ui
  - web page design
---

# ODS Design System Skill

## Purpose

Ensure every UI strictly follows ODS tokens, components, and themes from the
local design system submodule. No invented tokens, no external fetches, no
component overrides.

---

## Data Access Rule

- **Never** fetch tokens, components, or themes from external URLs (GitHub
  links, CDNs, the web).
- **Always** read from the local submodule mounted at the repo root:
  - `design-system/DESIGN.md`
  - `design-system/tokens/*`
  - `design-system/components/*.json`
  - `design-system/themes/*.json`
- Product-specific rules live **inside this skill**, in `./products/`.

If the submodule is not initialized, stop and ask the user to run
`git submodule update --init --recursive`. Do not substitute with web-fetched
copies.

---

## Token Priority

When resolving any style value, walk this order top-down:

1. **Component tokens** — from `design-system/components/*.json`
2. **Global tokens** — from `design-system/DESIGN.md` and
   `design-system/tokens/*`
3. **Product tokens** — from `design-system/themes/{product}.json`

A lower-priority layer never overrides a higher one.

---

## Token Validation Rule

Before using any token:

- Verify it exists in the current product scope or in the global design system.
- Never invent token names, hex values, or spacing numbers.
- If a required token is missing → **ASK the user**, do not substitute.

---

## Component Authority Rule

All UI components (Button, CTA, Input, etc.) must strictly follow definitions
from `design-system/components/*.json`.

- Do **not** override component colors, sizes, variants, or states.
- Product files (e.g. `products/shift.md`, `products/crm.md`) must **not**
  modify component styles.
- Components are isolated from product themes.

### Component Isolation Example

- CTA → uses `design-system/components/cta.json` only (ODS blue `#0047FF`).
- Background → may use Shift product theme (e.g. Shift darkGrey).
- Product tokens apply only to: **backgrounds, layout, sections** — never to
  components.

---

## Token Scope Rule (Product Context)

When a product context is active (e.g. Shift):

- Use **only** tokens defined in that product's scope.
- Do **not** use generic tokens like `grey-900` or `blue-500` unless they are
  explicitly mapped into the product theme.

Correct for Shift: `darkGrey-*`, `shift-primary`
Avoid for Shift: `grey-900`, `blue-500` (unless mapped)

If a required product token is missing → ASK instead of substituting.

---

## Product Activation Rule

When a product is specified (e.g. Shift):

- Auto-load `design-system/themes/{product}.json` for theme tokens.
- Auto-load `./products/{product}.md` for product-specific rules and context.
- Apply product tokens to:
  - page background
  - sections
  - layout surfaces
- Do **not** apply product tokens to:
  - components (CTA, inputs, buttons)

---

## Product Overrides

If the request names a specific product:

1. Look inside `./products/` (relative to this skill).
2. Match the product name (e.g. `shift`, `crm`, `books`).
3. Apply product-specific rules and tokens on top of the base system.

Product rules override the base design system **only where explicitly
permitted** (backgrounds, layout, sections — never components).

---

## Prioritize

1. Semantic tokens
2. Component rules
3. Typography and spacing

---

## Auto-Activation Hint

This skill should activate automatically whenever a request involves UI,
layout, components, design systems, styling, or frontend generation in a Zoho
or ODS context.