# Shopify Theme Framework

**Document ID:** 11  
**Document Title:** Layout Engine Specification  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Layout Engine Specification

## 1. Purpose

This document defines the Layout Engine for the Shopify Theme Framework.

The Layout Engine is responsible for controlling structural layout behaviour across sections, components, blocks, templates, skins, and responsive breakpoints.

It ensures that merchants can use simple layout controls at the beginner level while advanced users, designers, developers, and agencies can access deeper layout systems such as grid, flex, columns, split layouts, boxed layouts, full-width layouts, and future layout extensions.

---

## 2. Layout Engine Vision

The Layout Engine should make complex layout systems feel simple for merchants.

The user should not need to understand CSS Grid, Flexbox, container rules, responsive calculations, or breakpoint architecture to build a strong storefront.

At the same time, the framework must expose enough layout power for advanced design and agency-level work.

The guiding principle is:

```text
Simple layout choices for merchants. Powerful layout systems underneath.
```

---

## 3. Core Responsibilities

The Layout Engine is responsible for:

- Page structure
- Section width behaviour
- Container behaviour
- Grid layouts
- Flex layouts
- Column layouts
- Split layouts
- Floating layouts
- Stacked layouts
- Responsive layout rules
- Spacing relationships
- Layout presets
- Layout variants
- Layout inheritance
- Layout safety rules

The Layout Engine should not own visual styling such as colours, typography, shadows, or brand personality. Those belong to the Design System and Skin Layer.

---

## 4. Core Principles

### Structure Before Style

Layout defines the arrangement of content. It should remain independent from visual skin decisions.

### Presets Before Complexity

Beginner users should choose from layout presets instead of manually configuring technical layout systems.

### One Layout Model, Multiple Workflows

Different workflow modes may present layout options differently, but all modes should map to the same internal layout architecture.

### Responsive by Default

Every layout must be mobile-safe by default.

### Predictable Overrides

Global layout rules should be inherited unless a section, component, or block intentionally overrides them.

---

## 5. Supported Layout Modes

Initial layout modes should include:

| Layout Mode | Purpose |
| --- | --- |
| Full Width | Allows content or background to stretch edge-to-edge. |
| Boxed | Keeps content inside a controlled maximum width. |
| Contained | Uses a standard content container with responsive padding. |
| Grid | Arranges items in rows and columns. |
| Flex | Arranges items in flexible rows or columns. |
| Columns | Provides merchant-friendly multi-column layouts. |
| Split | Creates two-sided layouts such as image and content. |
| Stack | Arranges items vertically with consistent spacing. |
| Floating | Allows elevated or offset layout effects. |
| Masonry | Future layout mode for uneven content grids. |

---

## 6. Layout Abstraction Model

The framework should expose human-friendly layout choices while mapping them to technical implementation internally.

Example:

| User-Facing Choice | Internal Layout System |
| --- | --- |
| Edge-to-Edge | Full width container |
| Contained | Max-width container |
| Image + Text | Split layout |
| Product Grid | CSS Grid |
| Flexible Row | Flexbox |
| Three Columns | Grid or Flex columns |
| Stacked Content | Vertical stack |

This allows the editor to remain approachable without weakening the underlying architecture.

---

## 7. Layout Inheritance

Layout settings should follow a predictable inheritance model.

```text
Framework Defaults
  -> Global Layout Settings
  -> Template Layout Settings
  -> Section Layout Settings
  -> Component Layout Settings
  -> Block Layout Settings
  -> Manual Overrides
```

Lower levels may override higher levels only when necessary.

---

## 8. Global Layout Settings

Global layout settings should define the default structure for the whole storefront.

Examples:

- Page width
- Container width
- Section spacing
- Grid gap
- Mobile padding
- Desktop padding
- Default layout density
- Default content alignment
- Default responsive behaviour

These settings should provide consistency across the store.

---

## 9. Section Layout Settings

Section-level layout settings control how a section behaves inside a page.

Examples:

- Section width
- Section padding
- Background width
- Content width
- Vertical spacing
- Horizontal spacing
- Alignment
- Visibility by device
- Section order, where Shopify supports it

Section settings should remain merchant-friendly and avoid unnecessary technical language.

---

## 10. Component Layout Settings

Component-level layout settings control the internal arrangement of component content.

Examples:

- Media position
- Content alignment
- Number of columns
- Grid behaviour
- Stack direction
- Gap size
- Reverse layout on mobile
- Image ratio
- Content width ratio

These settings should work consistently across skins.

---

## 11. Block Layout Settings

Block-level layout settings should be limited and intentional.

Examples:

- Block alignment
- Block spacing
- Block width
- Block visibility
- Block order

Too many block-level layout controls can overwhelm merchants, so they should be exposed progressively.

---

## 12. Layout Presets

Layout presets should provide ready-made structural choices.

Example Hero layout presets:

- Centered content
- Content left, media right
- Media left, content right
- Full-bleed background
- Product-focused split
- Minimal announcement

Example Collection layout presets:

- Two-column grid
- Three-column grid
- Four-column grid
- Featured product plus grid
- Editorial collection layout

Presets should be reusable and skin-compatible.

---

## 13. Layout Variants

Layout variants are component-specific layout alternatives.

A variant should define what changes structurally while keeping the component identity intact.

Example:

```text
Hero Component
  -> Centered Variant
  -> Split Variant
  -> Full-Bleed Variant
  -> Product-Focused Variant
```

Variants should avoid duplicating component logic.

---

## 14. Responsive Behaviour

The Layout Engine must be mobile-first.

Responsive rules should define how layouts adapt across:

- Mobile
- Tablet
- Desktop
- Large desktop

Examples:

- Multi-column grids collapse on mobile.
- Split layouts stack on mobile.
- Floating elements become normal flow on mobile.
- Large spacing scales down on smaller screens.
- Media-heavy sections use safe mobile ratios.

---

## 15. Layout Safety Rules

The Layout Engine should prevent broken layouts.

Examples:

- Prevent unreadable content widths.
- Prevent excessive columns on mobile.
- Prevent overlapping text and media.
- Prevent unsafe negative spacing by default.
- Warn when media ratios may break layout.
- Provide safe fallbacks when settings conflict.

Safety rules should protect beginners while still allowing advanced control for expert users.

---

## 16. Theme Editor UX

Layout controls should be exposed progressively.

### Basic Level

- Layout preset
- Width option
- Alignment
- Spacing size

### Standard Level

- Column count
- Grid gap
- Media position
- Container width
- Mobile stack behaviour

### Advanced Level

- Responsive overrides
- Custom ratios
- Advanced spacing
- Visibility by device

### Designer Level

- Detailed layout rhythm
- Visual density
- Advanced composition controls

### Developer Level

- Custom classes
- Data attributes
- Debug layout information

---

## 17. Layout and Design Tokens

The Layout Engine should consume layout-related tokens.

Relevant token categories:

- Spacing
- Breakpoints
- Container width
- Grid gap
- Radius, where layout affects media containers
- Density

The Layout Engine should not define brand visual identity.

---

## 18. Layout and Skins

Skins may influence layout defaults, but they should not replace layout architecture.

Examples:

- A luxury skin may use wider spacing.
- A compact commerce skin may use tighter product grids.
- An editorial skin may prefer larger media and asymmetrical layouts.

The underlying layout system should remain consistent.

---

## 19. Layout and Template Packs

Template packs may define page-level layout compositions.

Examples:

- Fashion homepage layout
- Single product launch layout
- B2B catalogue layout
- Beauty brand storytelling layout
- Conversion landing page layout

Template packs should compose existing layout modes, components, variants, and presets instead of creating separate layout systems.

---

## 20. Performance Considerations

Layout decisions affect performance.

Rules:

- Avoid layout systems that require unnecessary JavaScript.
- Prefer CSS Grid and Flexbox for native browser performance.
- Avoid layout shifts.
- Define media dimensions where possible.
- Keep layout CSS reusable and minimal.
- Load advanced layout behaviour only when needed.

---

## 21. Accessibility Considerations

Layouts should preserve accessibility.

Requirements:

- Maintain logical reading order.
- Avoid visual order that conflicts with keyboard order.
- Ensure responsive stacking remains understandable.
- Preserve heading hierarchy.
- Avoid hidden content that becomes inaccessible.
- Maintain sufficient spacing for touch targets.

---

## 22. Initial MVP Scope

The first implementation of the Layout Engine should support:

- Full width layout
- Boxed layout
- Contained layout
- Stack layout
- Grid layout
- Flex row layout
- Basic columns
- Split layout
- Global container width
- Section spacing scale
- Mobile stacking rules

Advanced floating layouts, masonry, custom ratios, and visual builder-level controls can be added later.

---

## 23. Future Enhancements

Future Layout Engine capabilities may include:

- Visual layout previews
- Drag-and-drop layout composition
- AI layout recommendations
- Custom layout presets
- Layout import/export
- Masonry layouts
- Advanced responsive rules
- Layout performance scoring
- Layout conflict detection
- Agency layout libraries

---

## 24. Acceptance Criteria

The Layout Engine will be considered successful when:

- Beginners can select layouts without technical knowledge.
- Advanced users can access deeper layout controls.
- Layouts remain responsive by default.
- Components can support multiple layout variants without duplication.
- Skins can influence layout feel without replacing layout structure.
- Template packs can compose layouts consistently.
- Layout settings follow predictable inheritance.
- Layout choices do not create unnecessary performance problems.

---

## 25. Open Questions

- Which layout controls should be available in the first release?
- Should layout presets be stored in JSON, Liquid schema, or both?
- Should the companion app manage advanced layout presets?
- How much responsive override control should be exposed to non-technical users?
- Should layout conflict warnings appear in the theme editor, companion app, or both?
- Should agencies be able to save and reuse custom layout presets?

---

## 26. Related Documents

- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 09 - Design Tokens Specification
- Document 10 - Product Roadmap
- Document 12 - Component Registry Specification
- Document 13 - Variant Engine Specification
- Document 14 - Universal Block System
- ADR 005 - Prefer Variant-Based Layouts over Duplicate Sections

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Layout Engine Specification document |
