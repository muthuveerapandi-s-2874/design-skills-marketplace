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