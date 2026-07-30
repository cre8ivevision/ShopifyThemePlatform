# Shopify Theme Platform

**Document ID:** 45  
**Document Title:** Responsive Behaviour  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Responsive Behaviour

## 1. Purpose

This document defines how the Shopify Theme Platform adapts across mobile, tablet, desktop, and wide screens. Responsive behaviour must be consistent, predictable, and merchant-friendly.

## 2. Scope

This document covers breakpoints, responsive layout rules, component adaptation, typography, spacing, media, commerce patterns, and theme editor controls.

## 3. Responsive Principles

- Mobile experience must be first-class.
- Components should adapt through defined rules, not one-off fixes.
- Responsive controls should be simple by default and advanced when needed.
- Layout changes should preserve content priority.
- Visual quality must remain strong across all common devices.

## 4. Breakpoint Strategy

The system should define standard breakpoints as tokens.

| Token | Purpose |
|---|---|
| `breakpoint.sm` | Small mobile |
| `breakpoint.md` | Large mobile / small tablet |
| `breakpoint.lg` | Tablet / small desktop |
| `breakpoint.xl` | Desktop |
| `breakpoint.2xl` | Wide desktop |

Exact values should be documented in the Design Tokens Specification.

## 5. Layout Adaptation

Common responsive patterns:

- Columns stack on mobile.
- Split sections become vertical stacks.
- Product grids reduce column count.
- Navigation switches to mobile navigation.
- Media should maintain usable aspect ratios.
- Dense content should collapse into accordions where appropriate.

## 6. Typography Adaptation

Typography should adapt through role-based responsive tokens.

Rules:

- Avoid viewport-only font scaling.
- Maintain readable line lengths.
- Keep buttons and labels legible.
- Preserve heading hierarchy on mobile.

## 7. Spacing Adaptation

Spacing should reduce naturally on smaller screens while preserving rhythm.

Example:

- Hero spacing: large on desktop, medium on tablet, compact on mobile.
- Grid gaps: standard on desktop, tight on mobile.

## 8. Commerce Adaptation

Commerce-specific responsive patterns:

- Product cards remain tappable.
- Add-to-cart controls remain visible and usable.
- Variant selectors avoid cramped layouts.
- Price and discount information remains readable.
- Cart and drawer interactions work well on touch devices.

## 9. Merchant Controls

Beginner controls:

- Mobile layout preset
- Image crop behaviour
- Stack order

Advanced controls:

- Breakpoint-specific visibility
- Mobile spacing
- Tablet layout
- Desktop layout
- Custom ordering

## 10. Acceptance Criteria

- Responsive behaviour is documented per component family.
- Mobile layouts are not afterthoughts.
- Breakpoints use tokens.
- Merchant controls avoid unnecessary complexity.
- Commerce interactions remain usable on touch devices.

## 11. Related Documents

- Document 11 - Layout Engine Specification
- Document 41 - Typography
- Document 43 - Spacing System
- Document 44 - Grid System

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First responsive behaviour specification |
