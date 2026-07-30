# Shopify Theme Platform

**Document ID:** 43  
**Document Title:** Spacing System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Spacing System

## 1. Purpose

This document defines spacing rules for the Shopify Theme Platform. Spacing must create visual rhythm, improve readability, and support consistent layouts across components, skins, and templates.

## 2. Scope

This document covers spacing tokens, section spacing, component spacing, responsive spacing, merchant controls, and skin-level spacing behaviour.

## 3. Spacing Principles

- Spacing should be systematic, not arbitrary.
- The default spacing system should feel clean and simple.
- Skins may adjust spacing density and rhythm.
- Components should consume spacing tokens.
- Merchant controls should provide useful presets rather than excessive pixel-level decisions.

## 4. Spacing Token Scale

Example token scale:

| Token | Purpose |
|---|---|
| `space.0` | No spacing |
| `space.1` | Extra small spacing |
| `space.2` | Small spacing |
| `space.3` | Compact component spacing |
| `space.4` | Default component spacing |
| `space.5` | Medium section spacing |
| `space.6` | Large section spacing |
| `space.7` | Extra large layout spacing |
| `space.8` | Hero and campaign spacing |

## 5. Spacing Categories

The system should define spacing for:

- Page margins
- Section padding
- Component padding
- Grid gaps
- Stack gaps
- Inline gaps
- Form spacing
- Navigation spacing
- Commerce card spacing

## 6. Density Modes

The platform should support spacing density modes.

| Mode | Usage |
|---|---|
| Compact | Dense product grids, B2B, operational stores |
| Standard | Default commerce experience |
| Spacious | Premium, editorial, lifestyle stores |

Density modes should map to token values.

## 7. Section Spacing

Sections should support:

- Top padding
- Bottom padding
- Inner gap
- Container gap
- Mobile-specific adjustments

Beginner users should choose presets such as Compact, Standard, or Spacious.

## 8. Skin-Level Spacing

Skins may define spacing rhythm.

Examples:

- Minimal Mono: compact and clean
- Luxury Editorial: spacious and calm
- Bold Campaign: high-impact vertical spacing
- B2B Clean: dense and efficient

## 9. Responsive Behaviour

Spacing should adapt by breakpoint using tokens rather than manual overrides.

Mobile spacing should generally be tighter but never cramped.

## 10. Acceptance Criteria

- Spacing is token-based.
- Components do not use arbitrary spacing values.
- Density modes are supported.
- Skins can modify spacing rhythm.
- Mobile spacing remains usable and consistent.

## 11. Related Documents

- Document 04 - Design System
- Document 09 - Design Tokens Specification
- Document 44 - Grid System
- Document 45 - Responsive Behaviour

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First spacing system specification |
