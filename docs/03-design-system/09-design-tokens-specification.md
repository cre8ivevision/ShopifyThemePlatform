# Shopify Theme Framework

**Document ID:** 09  
**Document Title:** Design Tokens Specification  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Design Tokens Specification

## 1. Purpose

This document defines the design token system for the Shopify Theme Framework.

Design tokens are the source of truth for visual styling across the base design system, skins, templates, presets, sections, blocks, and components.

---

## 2. Token Vision

The framework should use tokens to separate structure from visual presentation.

A component should not need to know whether the active design is minimal, luxury, bold, editorial, or conversion-focused. It should consume stable token values and styling hooks.

```text
Component Structure
  -> Token Reference
  -> Active Skin Values
  -> Rendered Design
```

---

## 3. Token Principles

- Tokens should be reusable.
- Tokens should be stable.
- Tokens should support skins.
- Tokens should support templates.
- Tokens should reduce hardcoded styling.
- Tokens should improve consistency.
- Tokens should support progressive design complexity.
- Tokens should be understandable for both humans and AI coding assistants.

---

## 4. Token Categories

Initial token categories:

- Colour
- Typography
- Spacing
- Radius
- Shadow
- Border
- Motion
- Breakpoint
- Z-index
- Density
- Component

---

## 5. Token Inheritance Model

```text
Framework Defaults
  -> Base Design System
  -> Active Skin
  -> Active Template Pack
  -> Global Theme Settings
  -> Section Settings
  -> Block Settings
  -> Manual Overrides
```

Lower levels may override higher levels, but overrides should remain controlled and predictable.

---

## 6. Colour Tokens

Recommended colour token groups:

- `color.background`
- `color.surface`
- `color.text`
- `color.text-muted`
- `color.primary`
- `color.secondary`
- `color.accent`
- `color.border`
- `color.success`
- `color.warning`
- `color.error`
- `color.sale`

Colour tokens should support future light and dark mode strategies.

---

## 7. Typography Tokens

Recommended typography token groups:

- `font.family.body`
- `font.family.heading`
- `font.size.body`
- `font.size.heading`
- `font.weight.regular`
- `font.weight.medium`
- `font.weight.bold`
- `line-height.body`
- `line-height.heading`
- `letter-spacing.default`

The base system should use a simple typography scale. Skins may introduce more advanced type pairings.

---

## 8. Spacing Tokens

Spacing should follow a predictable scale.

Example:

```text
space.0
space.1
space.2
space.3
space.4
space.5
space.6
space.8
space.10
space.12
space.16
```

Spacing tokens should be used for section padding, grid gaps, component spacing, and block rhythm.

---

## 9. Radius, Shadow, and Border Tokens

Radius tokens:

- `radius.none`
- `radius.sm`
- `radius.md`
- `radius.lg`
- `radius.full`

Shadow tokens:

- `shadow.none`
- `shadow.sm`
- `shadow.md`
- `shadow.lg`

Border tokens:

- `border.width.default`
- `border.color.default`
- `border.style.default`

---

## 10. Motion Tokens

Motion should be subtle and optional.

Recommended motion tokens:

- `motion.duration.fast`
- `motion.duration.normal`
- `motion.duration.slow`
- `motion.easing.standard`
- `motion.easing.emphasis`

The system must support reduced motion preferences.

---

## 11. Breakpoint Tokens

Breakpoint tokens should support mobile-first design.

Example:

- `breakpoint.sm`
- `breakpoint.md`
- `breakpoint.lg`
- `breakpoint.xl`
- `breakpoint.2xl`

Final breakpoint values should be validated during implementation.

---

## 12. Component Tokens

Component tokens may define component-specific defaults while still inheriting from global tokens.

Examples:

- `button.primary.background`
- `button.primary.text`
- `card.background`
- `card.radius`
- `product-card.image-ratio`
- `section.padding-y`

Component tokens should not become a replacement for reusable CSS architecture.

---

## 13. Skin Token Overrides

A skin should primarily work by overriding tokens.

Example:

```text
Base System
  color.primary = neutral black

Luxury Skin
  color.primary = deep charcoal
  font.family.heading = editorial serif
  radius.md = smaller radius
```

Skins should avoid replacing component structure.

---

## 14. Theme Editor Token Controls

Token controls should be exposed progressively.

Beginner users should see simple controls:

- Brand colour
- Font style
- Button style
- Spacing size

Advanced users may see:

- Section spacing tokens
- Typography scale
- Radius system
- Shadow system
- Component token overrides

---

## 15. Acceptance Criteria

The token system is successful when:

- Components use tokens instead of hardcoded repeated values.
- Skins can change visual personality without changing structure.
- Templates can define consistent visual defaults.
- Beginners are not overwhelmed by token complexity.
- Advanced users can access deeper control.
- Tokens support performance-friendly CSS.

---

## 16. Open Questions

- Should tokens be stored as CSS variables, JSON, Liquid settings, or a hybrid?
- Should the companion app manage advanced token editing?
- Which token values should be editable in Shopify Theme Editor?
- Should merchants be able to export token sets as custom skins?

---

## 17. Related Documents

- Document 04 - Design System
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 08 - Development Standards

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Design Tokens Specification document |
