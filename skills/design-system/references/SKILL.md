---
name: ods-design-system
description: Apply Zoho ODS design tokens when building UI, components, or webpages.
---

triggers:
  - zoho ui
  - ods
  - design system
  - build ui
  - create component
  - landing page
  - dashboard ui
  - web page design

# ODS Design System Skill

## Purpose
Ensure all UI follows ODS tokens strictly.

## Rules
- Use ONLY tokens from DESIGN.md
- No custom styles
- Follow component structure exactly
- If missing → ASK
- Components must strictly follow definitions from @design-system/components/*.json
- Do NOT override component colors, sizes, variants, or states
- Product files (e.g., shift.md) must NOT modify component styles
- Components must strictly follow definitions from @design-system/components/*.json
- Do NOT override component colors, sizes, variants, or states
- Product files (e.g., shift.md) must NOT modify component styles
- Do NOT fetch design tokens from external URLs
- Always use local references via @design-system/*
- Do NOT mix global tokens with product-specific tokens

## Data Access Rule

Do NOT fetch design tokens from external URLs (e.g., GitHub links).

Always use local references:

@design-system/tokens/*
@design-system/components/*
@design-system/themes/*

External HTTP fetch calls are not allowed.


## Component Authority Rule

All UI components (e.g., Button, CTA, Input) must strictly follow definitions from:

@design-system/components/*.json

Never override component styles using product tokens.

## Token Priority

1. Component tokens (highest priority)
2. Global tokens (@design-system/DESIGN.md)
3. Product tokens (lowest priority)

Product tokens must never override component definitions.


## Token Scope Rule

When a product context is active (e.g., Shift):

- ONLY use tokens defined in that product scope
- Do NOT use generic tokens (e.g., grey-*, blue-*, etc.) unless explicitly defined in the product

Example:
- Use: darkGrey-*, shift-primary
- Avoid: grey-900, blue-500 (unless mapped)

If a required token is missing:
→ ASK instead of substituting


## Token Validation Rule

Before using any token:
- Verify it exists in current product or design system
- Do not invent token names

## Instruction   ← ✅ PUT IT HERE

Always follow the external design system:
https://github.com/muthuveerapandi-s-2874/ODS--design-system/blob/main/DESIGN.md

If needed:
- Fetch tokens from design-system/tokens/
- Use themes from design-system/themes/

## Prioritize
1. Semantic tokens
2. Component rules
3. Typography and spacing

## Auto Activation Hint
This skill should activate automatically when the request involves UI, layout, components, design systems, styling, or frontend generation.

## Product Overrides

If the request is related to a specific product:

- Look inside: references/products/
- Match product name (e.g., shift, crm, books)
- Apply product-specific rules and tokens

Product rules override base design system when present.

## Product Context Loading

When a product is specified (e.g., Shift),
load tokens and references from:

@design-system/references/products/{product}.md