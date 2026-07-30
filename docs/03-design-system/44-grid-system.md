# Shopify Theme Platform

**Document ID:** 44  
**Document Title:** Grid System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Grid System

## 1. Purpose

This document defines the grid system used by the Shopify Theme Platform. The grid system should provide a consistent structural foundation for sections, templates, components, and layout variants.

## 2. Scope

This document covers containers, columns, gutters, responsive grids, layout presets, merchant controls, and relationship to the Layout Engine.

## 3. Grid Principles

- The grid should support structure before decoration.
- The default grid should be simple and predictable.
- Advanced layouts should be exposed through presets and variants.
- Grid behaviour should align with the Layout Engine.
- Components should be able to adapt to container context.

## 4. Container Types

The platform should support multiple container modes.

| Container | Purpose |
|---|---|
| Full Width | Edge-to-edge sections |
| Standard | Default page content width |
| Narrow | Text-heavy editorial content |
| Wide | Rich commerce and campaign sections |
| Boxed | Controlled page frame |
| Floating | Elevated layout moments |

## 5. Column System

The system should support common column patterns:

- 1 column
- 2 columns
- 3 columns
- 4 columns
- 6 columns
- 12-column advanced grid
- Auto-fit product grids
- Mixed editorial grids

## 6. Gutter System

Gutters should use spacing tokens.

Gutter presets:

- None
- Tight
- Standard
- Spacious
- Custom advanced value

## 7. Responsive Rules

Grid layouts should collapse predictably on smaller screens.

Examples:

- 4 columns become 2 columns on tablet and 1 column on mobile.
- Split layouts stack vertically on mobile.
- Product grids use adaptive minimum card width.

## 8. Layout Presets

The grid system should support familiar workflow presets without copying external builders.

Examples:

- Simple Columns
- Flexible Grid
- Editorial Split
- Product Matrix
- Feature Rows
- Asymmetric Campaign

## 9. Merchant Controls

Beginner controls:

- Container width
- Column count
- Gap size

Advanced controls:

- Breakpoint behaviour
- Column ratios
- Alignment
- Auto-fit rules
- Section-level grid overrides

## 10. Acceptance Criteria

- Grid decisions are token and preset driven.
- Containers are reusable across sections.
- Responsive behaviour is predictable.
- Layout presets map to the Layout Engine.
- Components do not implement private grid systems unless required.

## 11. Related Documents

- Document 11 - Layout Engine Specification
- Document 43 - Spacing System
- Document 45 - Responsive Behaviour
- Document 05 - Component Architecture

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First grid system specification |
