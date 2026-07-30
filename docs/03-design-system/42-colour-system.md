# Shopify Theme Platform

**Document ID:** 42  
**Document Title:** Colour System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Colour System

## 1. Purpose

This document defines the colour architecture for the Shopify Theme Platform. The colour system must support a clean minimal default theme while enabling advanced skins and templates to introduce premium visual direction safely.

## 2. Scope

This document covers colour roles, semantic tokens, accessibility, merchant controls, skin palettes, commerce states, and implementation rules.

## 3. Colour Principles

- Colours should communicate meaning, hierarchy, and brand personality.
- The default palette should be minimal, neutral, and broadly usable.
- Components must use semantic colour tokens rather than raw colour values.
- Skins should transform the visual experience without rewriting components.
- Accessibility contrast must remain protected.

## 4. Default Palette Strategy

The default design system should begin with a restrained mono-style palette.

Default palette characteristics:

- Neutral background
- Neutral foreground
- One primary action colour
- Soft borders
- Clear error, warning, success, and info states
- Low visual noise

This supports the project vision: start simple, then upgrade through skins or templates.

## 5. Semantic Colour Tokens

| Token | Purpose |
|---|---|
| `color.background` | Main page background |
| `color.surface` | Cards, panels, and grouped UI |
| `color.text` | Primary readable text |
| `color.text.muted` | Secondary text |
| `color.border` | Dividers and component boundaries |
| `color.primary` | Primary actions |
| `color.secondary` | Secondary actions |
| `color.accent` | Highlight moments |
| `color.success` | Positive state |
| `color.warning` | Caution state |
| `color.error` | Error state |
| `color.info` | Informational state |

## 6. Commerce Colour Roles

Commerce-specific colours should include:

- Sale price
- Compare-at price
- Inventory warning
- Sold out state
- Discount badge
- Trust badge
- Checkout call-to-action

These should be semantic and skin-aware.

## 7. Skin Palette System

Skins may provide complete palette presets.

Examples:

- Minimal Mono
- Premium Fashion
- Organic Wellness
- Bold Streetwear
- Clean B2B
- Editorial Luxury

A skin palette must map into the same semantic token structure.

## 8. Merchant Controls

Beginner controls:

- Select colour preset
- Choose primary brand colour
- Choose light or dark base

Advanced controls:

- Surface colours
- Border colours
- Text hierarchy
- State colours
- Section-level overrides

## 9. Accessibility Requirements

The system should enforce or warn for:

- Text contrast
- Button contrast
- Focus state visibility
- Error state visibility
- Sale badge readability

## 10. Implementation Rules

- Avoid hardcoded colours in components.
- All colours should resolve through tokens.
- Skins should override token values, not component logic.
- Commerce states must remain visually distinct.
- Dark mode should be treated as a skin or mode, not a separate component system.

## 11. Acceptance Criteria

- Colour roles are semantic.
- Default palette is usable without skin selection.
- Skins can upgrade visual quality through token overrides.
- Accessibility requirements are documented.
- Commerce-specific states are covered.

## 12. Related Documents

- Document 04 - Design System
- Document 09 - Design Tokens Specification
- Document 41 - Typography
- Document 46 - Accessibility Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First colour system specification |
