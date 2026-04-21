---
title: "Shift Product Theme"
purpose: "Product behavior and UI direction for Shift"
---

# PRODUCT — Shift

> This file defines the behavior and visual direction for the Shift product.
> It extends the global design system.

---

## System Usage

Always load:

1. @design-system/DESIGN.md  
2. @design-system/themes/shift.json  

---

## Theme Identity

- Product: Shift
- Mode: Dark
- Tone: Focused, minimal, productivity-driven
- Visual Style: Clean, low-noise interface

---

## UI Behavior

- Prefer **dark backgrounds** and deep surfaces
- Use **primary color for actions and highlights**
- Maintain **high contrast for readability**
- Reduce visual clutter and distractions

---

## Layout Guidelines

- Use spacious layouts with clear hierarchy
- Prioritize content over decoration
- Keep alignment strict and grid-based

---

## Component Variations

### Buttons

- Background: `var(--color-primary-500)`
- Text: white
- Style: slightly elevated using system shadow
- Avoid excessive variants

---

### Cards / Surfaces

- Use darker surfaces (`gray` tokens)
- Subtle elevation (no heavy shadows)
- Rounded corners from system tokens

---

### Typography

- Follow system typography strictly
- Use fewer font weights
- Maintain strong heading contrast

---

## Interaction Style

- Smooth and minimal transitions
- Avoid flashy animations
- Focus on usability and speed

---

## Usage Instructions (AI)

When generating UI:

1. Follow global system rules from `DESIGN.md`
2. Apply token overrides from `shift.json`
3. Apply Shift-specific behavior from this file
4. Maintain consistency across all components

---

## Restrictions

- Do NOT redefine tokens
- Do NOT override typography system
- Do NOT introduce new spacing values
- Do NOT hardcode colors

---

## Notes

Shift UI should feel:

- Calm
- Focused
- Professional
- Distraction-free