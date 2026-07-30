# Shopify Theme Framework

**Document ID:** 13  
**Document Title:** Variant Engine Specification  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Variant Engine Specification

## 1. Purpose

This document defines the Variant Engine for the Shopify Theme Framework.

The Variant Engine allows a single component to support multiple layout, structure, behaviour, and presentation options without duplicating entire Shopify sections or component implementations.

It is one of the core systems required to make the framework scalable, maintainable, skin-compatible, and easy for merchants to customise.

---

## 2. Variant Engine Vision

The framework should avoid creating separate components or sections for every layout style.

Instead, components should expose controlled variants that reuse the same core component identity, settings model, block system, design tokens, and accessibility rules.

The guiding principle is:

```text
One component. Multiple valid expressions. No unnecessary duplication.
```

---

## 3. Core Responsibilities

The Variant Engine is responsible for:

- Defining supported variants for each component
- Resolving the active variant
- Applying variant-specific layout rules
- Applying variant-specific settings
- Supporting variant-specific blocks when needed
- Supporting responsive variant behaviour
- Supporting skin compatibility
- Supporting preset compatibility
- Preventing invalid variant configurations
- Reducing duplicated Liquid, CSS, and JavaScript

---

## 4. What a Variant Is

A variant is a controlled alternative expression of the same component.

A variant may change:

- Layout
- Content arrangement
- Media position
- Block ordering
- Responsive behaviour
- Visual density
- Behaviour options
- Supported presets

A variant should not change the fundamental purpose of the component.

---

## 5. What a Variant Is Not

A variant should not be used when the feature is actually a different component.

A new component may be justified when:

- The purpose is different.
- The data model is different.
- The required blocks are completely different.
- The accessibility requirements are substantially different.
- The interaction model is substantially different.
- The component cannot share meaningful logic with the original component.

---

## 6. Variant Model

Recommended variant model:

```text
Variant
  -> Identity
  -> Parent Component
  -> Layout Rules
  -> Supported Blocks
  -> Settings Overrides
  -> Token Hooks
  -> Asset Rules
  -> Responsive Rules
  -> Accessibility Rules
  -> Preset Compatibility
```

---

## 7. Required Variant Metadata

Each variant should define:

| Field | Purpose |
| --- | --- |
| `id` | Stable variant identifier. |
| `name` | Human-readable variant name. |
| `componentId` | Parent component identifier. |
| `description` | Short explanation of the variant. |
| `layoutMode` | Primary layout mode used by the variant. |
| `supportedBlocks` | Blocks supported by this variant. |
| `requiredBlocks` | Blocks required for correct output. |
| `settingsOverrides` | Variant-specific setting rules. |
| `responsiveBehaviour` | How the variant adapts across breakpoints. |
| `assetRules` | Required or optional assets. |
| `skinCompatibility` | Notes on skin compatibility. |
| `status` | Lifecycle status. |

---

## 8. Example Variant Record

```json
{
  "id": "split-media-right",
  "name": "Split: Media Right",
  "componentId": "hero",
  "description": "Hero layout with content on the left and media on the right.",
  "layoutMode": "split",
  "supportedBlocks": ["heading", "text", "button-group", "image", "badge"],
  "requiredBlocks": ["heading"],
  "settingsOverrides": {
    "mediaPosition": "right",
    "contentAlignment": "left"
  },
  "responsiveBehaviour": {
    "mobile": "stack-media-after-content",
    "desktop": "two-column-split"
  },
  "assetRules": {
    "requiredCss": ["hero.css"],
    "optionalJs": []
  },
  "skinCompatibility": "Uses global spacing, typography, button, and media tokens.",
  "status": "draft"
}
```

This is a planning example. Final implementation format may evolve during development.

---

## 9. Variant Types

Initial variant types may include:

| Variant Type | Description |
| --- | --- |
| Layout Variant | Changes structure or arrangement. |
| Content Variant | Changes content emphasis or block order. |
| Behaviour Variant | Changes interaction behaviour. |
| Density Variant | Changes spacing and compactness. |
| Commerce Variant | Changes product or shopping-related presentation. |
| Campaign Variant | Supports promotional or launch-specific layouts. |

A component may support multiple types of variants, but the system should avoid excessive complexity.

---

## 10. Variant Inheritance

Variants should inherit from the parent component.

```text
Parent Component Defaults
  -> Component Settings
  -> Active Variant Rules
  -> Active Preset Rules
  -> Active Skin Tokens
  -> Section Overrides
  -> Block Overrides
```

Variant-specific rules should only define what is different.

---

## 11. Variant and Layout Engine Relationship

The Variant Engine should work with the Layout Engine.

The Variant Engine decides which structural expression is active. The Layout Engine provides the layout rules used to render it.

Example:

```text
Hero Component
  -> Split Media Variant
  -> Layout Engine: Split Layout
  -> Design Tokens: Active Skin Values
```

The Variant Engine should not duplicate layout system responsibilities.

---

## 12. Variant and Component Registry Relationship

The Component Registry should know which variants each component supports.

The registry should track:

- Variant IDs
- Variant descriptions
- Supported blocks
- Required assets
- Layout modes
- Responsive behaviour
- Performance impact
- Skin compatibility
- Documentation links

This makes variants discoverable by the theme, companion app, documentation, and AI assistants.

---

## 13. Variant and Universal Block System Relationship

Variants may support different block arrangements while still relying on the Universal Block System.

Example:

```text
Hero Component
  Centered Variant:
    Heading
    Text
    Button Group

  Product-Focused Variant:
    Badge
    Heading
    Product Media
    Price
    Button Group
```

The variant should define allowed block patterns without creating a completely separate component unless necessary.

---

## 14. Variant and Preset Relationship

Presets should often select a default variant.

Example:

| Preset | Component | Default Variant |
| --- | --- | --- |
| Minimal Hero | Hero | Centered |
| Product Launch Hero | Hero | Product-Focused |
| Editorial Hero | Hero | Split Media Left |
| Campaign Hero | Hero | Full-Bleed Background |

Presets configure variants. Variants define valid structure.

---

## 15. Variant and Skin Relationship

Skins should be able to style variants without changing their structure.

Rules:

- Variants must expose stable styling hooks.
- Skins may adjust spacing, typography, colour, radius, and visual treatment.
- Skins should not replace variant markup.
- Variant-specific skin overrides should be limited and documented.

---

## 16. Theme Editor UX

Variant selection should be easy for merchants.

Instead of exposing technical names only, variants should use human-readable labels.

Examples:

| Internal Variant | User-Facing Label |
| --- | --- |
| `centered` | Centered Content |
| `split-media-left` | Image Left, Text Right |
| `split-media-right` | Text Left, Image Right |
| `full-bleed-background` | Background Image |
| `product-focused` | Product Highlight |

Where possible, the editor or companion app should show visual previews.

---

## 17. Progressive Variant Controls

Variant settings should follow user experience levels.

### Basic

- Choose layout style
- Choose preset

### Standard

- Adjust alignment
- Adjust spacing
- Change media position

### Advanced

- Responsive behaviour
- Column ratios
- Conditional visibility

### Designer

- Variant-specific visual tuning
- Density rules
- Advanced composition controls

### Developer

- Debug information
- Custom classes
- Variant data attributes
- Experimental variant options

---

## 18. Variant Asset Loading

Variant assets should load only when required.

Rules:

- Shared component CSS should remain minimal.
- Variant-specific CSS should be loaded only when needed, where technically possible.
- Variant JavaScript should be avoided unless necessary.
- Heavy media or interaction variants should be clearly marked.
- Disabled variants should not affect storefront performance.

---

## 19. Variant Validation Rules

The Variant Engine should prevent invalid configurations.

Possible validation checks:

- Active variant exists for the component.
- Required blocks are present.
- Unsupported blocks are not rendered unexpectedly.
- Required assets exist.
- Variant settings are valid.
- Variant supports the selected layout mode.
- Variant is compatible with the active skin.
- Mobile fallback exists.

---

## 20. Accessibility Requirements

Every variant must preserve accessibility.

Requirements:

- Maintain logical reading order.
- Preserve heading structure.
- Ensure keyboard navigation remains functional.
- Avoid visual order that creates confusing screen reader order.
- Provide accessible controls for interactive variants.
- Support reduced motion where animation exists.

---

## 21. Performance Requirements

Variant design should avoid unnecessary performance cost.

Rules:

- Prefer CSS-based layout changes over JavaScript.
- Avoid duplicating markup heavily across variants.
- Avoid loading inactive variant assets.
- Mark heavy variants clearly in metadata.
- Provide safer default variants for beginners.

---

## 22. MVP Scope

The first version of the Variant Engine should support:

- Variant metadata
- Variant selection through section settings
- Variant-specific layout rules
- Variant-specific block compatibility notes
- Variant-friendly CSS hooks
- Basic responsive fallback rules
- Registry integration

Advanced visual previews, app-powered variant recommendations, and AI-generated variants can be added later.

---

## 23. Future Enhancements

Future capabilities may include:

- Visual variant previews
- AI variant recommendations
- Variant performance scoring
- Variant compatibility checks
- Variant import/export
- Agency custom variant libraries
- A/B testing support
- Dynamic variant selection based on page context

---

## 24. Acceptance Criteria

The Variant Engine will be considered successful when:

- A single component can support multiple layouts without duplicated sections.
- Variants reuse parent component settings and blocks where possible.
- Variants work with skins and templates.
- Variant selection is easy for merchants.
- Advanced users can access deeper variant controls.
- Variant assets do not load unnecessarily.
- Accessibility and responsive behaviour are preserved.
- Component Registry can track variant support clearly.

---

## 25. Open Questions

- Should variants be stored as JSON metadata, Liquid case logic, snippet files, or a hybrid system?
- How many variants should each component support before it becomes too complex?
- Should merchants be able to create custom variants?
- Should variant previews live inside the theme, companion app, or both?
- Should variant compatibility with skins be validated automatically?
- Should variant-specific settings be hidden until the variant is selected?

---

## 26. Related Documents

- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 11 - Layout Engine Specification
- Document 12 - Component Registry Specification
- Document 14 - Universal Block System
- ADR 001 - Adopt Component-First Architecture
- ADR 005 - Prefer Variant-Based Layouts over Duplicate Sections

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Variant Engine Specification document |
