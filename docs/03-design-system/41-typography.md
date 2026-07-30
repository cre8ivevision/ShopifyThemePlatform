# Shopify Theme Platform

**Document ID:** 41  
**Document Title:** Typography  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Typography

## 1. Purpose

This document defines the typography strategy for the Shopify Theme Platform. Typography must support a minimal default experience while allowing premium skins and industry templates to introduce richer brand expression without breaking readability, accessibility, or component consistency.

## 2. Scope

This document covers type roles, scale, hierarchy, font strategy, responsive behaviour, merchant controls, accessibility, and skin-level typography overrides.

## 3. Typography Principles

- Typography must be readable before it is decorative.
- The base theme should use a minimal, neutral typographic system.
- Skins may introduce stronger brand personality through controlled presets.
- Components should consume typography tokens rather than hardcoded font values.
- Merchant controls should remain simple for beginners and deeper for advanced users.

## 4. Default Typography System

The default typography system should be intentionally minimal.

Recommended default characteristics:

- Neutral font pairing
- Clear heading hierarchy
- Comfortable body text size
- Predictable line heights
- Limited weight usage
- No excessive decorative styling

The default system should feel clean, professional, and suitable for most stores before any premium skin is applied.

## 5. Type Roles

The platform should define reusable type roles.

| Role | Purpose |
|---|---|
| Display | High-impact hero and campaign messaging |
| Heading | Section and page titles |
| Subheading | Secondary supporting titles |
| Body | Standard readable content |
| Caption | Supporting metadata and small labels |
| Button | Action text |
| Navigation | Menu and navigation labels |
| Price | Commerce pricing display |
| Badge | Labels, tags, and status markers |

## 6. Type Scale

Typography should use tokenised scales rather than arbitrary sizes.

Example scale:

| Token | Usage |
|---|---|
| `type.size.xs` | Captions and small metadata |
| `type.size.sm` | Small body and labels |
| `type.size.md` | Default body text |
| `type.size.lg` | Lead text |
| `type.size.xl` | Small headings |
| `type.size.2xl` | Section headings |
| `type.size.3xl` | Page headings |
| `type.size.4xl` | Hero headings |

## 7. Font Strategy

The system should support:

- Shopify font picker compatibility
- System font defaults
- Optional brand font pairing
- Skin-level font presets
- Performance-conscious font loading

Fonts should never block the first usable render.

## 8. Skin-Level Overrides

Skins may define typography presets such as:

- Minimal Mono
- Editorial Luxury
- Modern Commerce
- Bold Campaign
- Soft Lifestyle
- Technical B2B

Each skin may adjust font family, scale, weight, letter case, and heading rhythm while preserving semantic type roles.

## 9. Merchant Controls

Beginner controls:

- Choose typography style preset
- Adjust base size
- Adjust heading style

Advanced controls:

- Heading font
- Body font
- Scale ratio
- Line height
- Weight mapping
- Letter case rules

## 10. Accessibility Requirements

Typography must support:

- Minimum readable font sizes
- Sufficient line height
- No negative letter spacing by default
- Responsive scaling without viewport-only font sizing
- Clear heading order
- Sufficient contrast with colour tokens

## 11. Acceptance Criteria

- Typography is token-based.
- Default typography works without a skin.
- Skins can override typography safely.
- Components use roles, not arbitrary font styles.
- Text remains readable on mobile and desktop.

## 12. Related Documents

- Document 04 - Design System
- Document 09 - Design Tokens Specification
- Document 42 - Colour System
- Document 45 - Responsive Behaviour

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First typography specification |
