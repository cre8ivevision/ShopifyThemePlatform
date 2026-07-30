# Shopify Theme Platform

**Document ID:** 48  
**Document Title:** Iconography  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Iconography

## 1. Purpose

This document defines the iconography strategy for the Shopify Theme Platform. Icons should improve recognition, reduce cognitive load, and support consistent interaction patterns across the storefront.

## 2. Scope

This document covers icon style, sizing, usage rules, commerce icons, accessibility, skin-level variation, and implementation guidelines.

## 3. Icon Principles

- Icons should communicate common actions clearly.
- Icons should not replace necessary text when clarity is required.
- Icon style should be consistent across the platform.
- Skins may adjust icon personality within defined rules.
- Interactive icons must remain accessible.

## 4. Default Icon Style

The default icon style should be:

- Minimal
- Clear
- Geometric
- Legible at small sizes
- Neutral enough for many industries

## 5. Icon Categories

The platform should support icons for:

- Navigation
- Search
- Cart
- Account
- Wishlist
- Filters
- Sorting
- Product media
- Payment and trust
- Social links
- Forms
- Alerts and states

## 6. Icon Sizes

Example sizing tokens:

| Token | Usage |
|---|---|
| `icon.size.xs` | Inline metadata |
| `icon.size.sm` | Small controls |
| `icon.size.md` | Standard buttons |
| `icon.size.lg` | Feature icons |
| `icon.size.xl` | Marketing blocks |

## 7. Commerce Icon Rules

Commerce icons must be instantly recognisable.

Examples:

- Cart
- Bag
- Search
- Account
- Filter
- Star rating
- Delivery
- Secure checkout
- Payment method

Avoid overly decorative commerce icons that reduce clarity.

## 8. Accessibility

Rules:

- Decorative icons should be hidden from assistive technology.
- Meaningful icons need accessible labels.
- Icon-only buttons require aria labels.
- Icons should preserve visible focus states when interactive.

## 9. Skin-Level Iconography

Skins may adjust:

- Stroke width
- Roundedness
- Filled vs outline style
- Decorative feature icons

Core commerce and navigation icons should remain familiar.

## 10. Acceptance Criteria

- Icons have consistent sizing tokens.
- Icon-only controls are accessible.
- Commerce icons remain recognisable.
- Skins can adjust style without breaking usability.
- Icons are not used as unclear decoration.

## 11. Related Documents

- Document 04 - Design System
- Document 46 - Accessibility Standards
- Document 50 - UI Guidelines
- Document 27 - Navigation Components

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First iconography specification |
