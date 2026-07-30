# Shopify Theme Framework

**Document ID:** 12  
**Document Title:** Component Registry Specification  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Component Registry Specification

## 1. Purpose

This document defines the Component Registry for the Shopify Theme Framework.

The Component Registry is the central catalogue of all framework components. It stores structured metadata about each component, including purpose, category, variants, blocks, presets, assets, dependencies, skin compatibility, accessibility requirements, performance notes, and lifecycle status.

The registry should make the framework easier to maintain, extend, document, test, and eventually support through the companion app and AI-assisted development workflows.

---

## 2. Registry Vision

The Shopify Theme Framework should not rely on tribal knowledge or scattered files to understand available components.

Every component should be discoverable through a consistent registry model.

The guiding principle is:

```text
If a component exists, the registry should know what it is, what it supports, and how it behaves.
```

This registry becomes the internal source of truth for component discovery, compatibility, documentation, feature management, and future automation.

---

## 3. Core Responsibilities

The Component Registry is responsible for tracking:

- Component identity
- Component category
- Component purpose
- Component status
- Supported variants
- Supported blocks
- Supported presets
- Supported layout modes
- Supported skins
- Required assets
- Optional assets
- Dependencies
- Accessibility requirements
- Performance notes
- Theme Editor settings groups
- Documentation links
- Test coverage expectations
- Version and lifecycle state

---

## 4. What the Registry Is Not

The registry should not be responsible for rendering storefront HTML directly.

It should not replace Shopify sections, Liquid snippets, design tokens, or component templates.

Instead, it should describe components and provide metadata that other systems can consume.

---

## 5. Registry Consumers

The registry may be consumed by:

- Theme rendering logic
- Component documentation
- Theme Editor configuration
- Feature Manager
- Companion App
- Skin Library
- Template Library
- Preset Manager
- Testing tools
- AI coding assistants
- Future marketplace systems

The registry should be designed so it can start simple and become more powerful over time.

---

## 6. Component Record Model

Each component should have a registry record.

Recommended high-level model:

```text
Component Record
  -> Identity
  -> Classification
  -> Capabilities
  -> Variants
  -> Blocks
  -> Presets
  -> Layout Support
  -> Skin Support
  -> Assets
  -> Dependencies
  -> Settings
  -> Accessibility
  -> Performance
  -> Documentation
  -> Lifecycle
```

---

## 7. Required Metadata Fields

Each component record should include:

| Field | Purpose |
| --- | --- |
| `id` | Stable component identifier. |
| `name` | Human-readable component name. |
| `description` | Short explanation of the component purpose. |
| `category` | Component category. |
| `version` | Component version. |
| `status` | Current lifecycle status. |
| `variants` | Supported layout or behaviour variants. |
| `blocks` | Supported block types. |
| `presets` | Available preset configurations. |
| `layoutModes` | Supported layout systems. |
| `skins` | Skin compatibility information. |
| `assets` | Required and optional assets. |
| `dependencies` | Component dependencies. |
| `settingsGroups` | Theme Editor setting groups. |
| `docs` | Documentation links. |

---

## 8. Example Registry Record

Example draft structure:

```json
{
  "id": "hero",
  "name": "Hero",
  "description": "Primary marketing section for page introductions, campaigns, and product storytelling.",
  "category": "marketing",
  "version": "0.1.0",
  "status": "draft",
  "variants": [
    "centered",
    "split-media-left",
    "split-media-right",
    "full-bleed-background",
    "product-focused"
  ],
  "blocks": [
    "heading",
    "text",
    "button-group",
    "image",
    "video",
    "badge"
  ],
  "presets": [
    "minimal-hero",
    "product-launch-hero",
    "fashion-campaign-hero"
  ],
  "layoutModes": [
    "contained",
    "full-width",
    "split",
    "stack"
  ],
  "skins": {
    "compatible": true,
    "notes": "Uses token hooks for typography, spacing, colours, buttons, and media presentation."
  },
  "assets": {
    "required": ["hero.css"],
    "optional": ["hero-video.js"]
  },
  "dependencies": [],
  "settingsGroups": [
    "content",
    "layout",
    "design",
    "behaviour",
    "responsive",
    "advanced"
  ],
  "docs": {
    "component": "docs/04-components/hero-components.md"
  }
}
```

This is a planning example. Final implementation format may change after technical validation.

---

## 9. Component Categories

Initial supported categories:

- Layout
- Header
- Footer
- Hero
- Product
- Collection
- Navigation
- Marketing
- Commerce
- Content
- Forms
- Interactive
- Utility

Categories should remain stable enough to support documentation, filtering, and companion app discovery.

---

## 10. Component Status Values

Recommended lifecycle status values:

| Status | Meaning |
| --- | --- |
| `proposed` | Idea exists but is not fully designed. |
| `planned` | Approved for future work. |
| `draft` | Being designed or documented. |
| `in-development` | Implementation has started. |
| `experimental` | Available but not stable. |
| `stable` | Safe for production use. |
| `deprecated` | Still available but should not be used for new work. |
| `removed` | No longer available. |

---

## 11. Capability Metadata

The registry should describe component capabilities.

Example capabilities:

- Supports variants
- Supports blocks
- Supports presets
- Supports skins
- Supports responsive overrides
- Supports animations
- Supports dynamic content
- Supports product data
- Supports collection data
- Supports app integration
- Supports accessibility checks

Capability metadata allows the system to recommend suitable components for different use cases.

---

## 12. Variant Metadata

Each variant should be described clearly.

Variant metadata may include:

- Variant ID
- Variant name
- Description
- Supported layout modes
- Required blocks
- Optional blocks
- Skin compatibility notes
- Responsive behaviour
- Performance impact

Variants should remain part of the component identity rather than becoming duplicated components.

---

## 13. Block Compatibility Metadata

The registry should define which blocks each component supports.

Example:

```text
Hero Component
  -> Heading block
  -> Text block
  -> Button group block
  -> Image block
  -> Video block
  -> Badge block
```

Block compatibility should help prevent unsupported configurations and improve Theme Editor UX.

---

## 14. Preset Metadata

Presets should be registered with useful context.

Preset metadata may include:

- Preset ID
- Preset name
- Component ID
- Recommended use case
- Included blocks
- Default variant
- Compatible skins
- Complexity level
- Performance impact

This helps the companion app and Theme Editor recommend better starting points.

---

## 15. Asset Metadata

Asset metadata should clarify what each component needs.

Asset groups:

- Required CSS
- Optional CSS
- Required JavaScript
- Optional JavaScript
- Media assets
- Icon assets
- External dependencies, if any

The registry should support conditional asset loading decisions.

---

## 16. Dependency Metadata

Dependencies should be explicit.

Examples:

- Requires design tokens
- Requires layout engine
- Requires variant engine
- Requires universal block system
- Requires product data
- Requires collection data
- Requires app embed

Dependencies should help avoid broken configurations and support future validation tooling.

---

## 17. Skin Compatibility Metadata

Components should declare how they work with skins.

Skin metadata may include:

- Compatible by default
- Requires token hooks
- Requires component-specific skin rules
- Not compatible with certain visual systems
- Recommended skins
- Known limitations

The goal is to ensure skins change appearance without replacing component structure.

---

## 18. Settings Group Metadata

Each component should declare which Theme Editor settings groups it uses.

Standard groups:

- Content
- Layout
- Design
- Behaviour
- Features
- Responsive
- Advanced

This supports consistency across the editor experience.

---

## 19. Accessibility Metadata

Each component should define accessibility requirements.

Examples:

- Requires heading level control
- Requires alt text support
- Requires keyboard navigation
- Requires ARIA labels
- Requires focus management
- Requires reduced motion support
- Requires form error messaging

Accessibility metadata should support QA and future automated checks.

---

## 20. Performance Metadata

Each component should include performance notes.

Performance metadata may include:

- CSS weight estimate
- JavaScript requirement
- Media requirement
- Lazy loading support
- Performance impact level
- Conditional asset rules

Suggested impact levels:

- Lightweight
- Moderate
- Heavy

---

## 21. Registry Storage Options

Possible storage formats:

| Option | Notes |
| --- | --- |
| JSON | Easy for tooling, app, and AI workflows. |
| Liquid schema metadata | Native to Shopify Theme Editor but less flexible. |
| YAML | Human-friendly but requires parsing. |
| Hybrid | JSON for registry plus Liquid schema for Shopify editor. |

Recommended initial approach:

```text
Hybrid model:
  JSON registry for framework metadata
  Shopify section schema for Theme Editor settings
```

---

## 22. Registry and Companion App

The companion app may use registry data to support:

- Component discovery
- Feature recommendations
- Skin compatibility checks
- Template pack selection
- Performance warnings
- Setup guidance
- Licensing decisions
- Component usage insights

The app should not require the registry to render storefront content.

---

## 23. Registry and AI Development

The registry should make AI-assisted development safer and more accurate.

AI assistants should be able to use registry data to understand:

- What components exist
- What variants are supported
- What blocks are allowed
- What assets are required
- What dependencies exist
- What documents are relevant
- What status a component has

This reduces accidental duplication and undocumented patterns.

---

## 24. Validation Rules

The registry should eventually support validation checks.

Examples:

- Every component has required metadata.
- Every variant belongs to a valid component.
- Every preset references a valid component and variant.
- Every block reference points to a supported block type.
- Every required asset exists.
- Every stable component has documentation.
- Every stable component has accessibility notes.

---

## 25. MVP Scope

The first registry implementation should include:

- Component ID
- Component name
- Category
- Description
- Status
- Supported variants
- Supported blocks
- Supported presets
- Required assets
- Optional assets
- Dependencies
- Documentation links

Advanced validation, app integration, analytics, and marketplace metadata can be added later.

---

## 26. Future Enhancements

Future registry capabilities may include:

- Automated documentation generation
- Component health dashboard
- AI component recommendations
- App-powered component discovery
- Marketplace compatibility metadata
- Component version history
- Deprecation warnings
- Cross-theme component reuse tracking
- Automated dependency validation

---

## 27. Acceptance Criteria

The Component Registry will be considered successful when:

- Every component has a clear identity.
- Component metadata is easy to inspect.
- Variants, blocks, presets, assets, and dependencies are traceable.
- The registry supports documentation and testing workflows.
- The companion app can eventually use registry data safely.
- AI coding assistants can use the registry to avoid duplicate or inconsistent components.
- The registry can start simple and scale over time.

---

## 28. Open Questions

- Should the registry be one central file or multiple component-level files?
- Should registry data live inside the theme, documentation, companion app, or all three?
- Should the companion app read registry data directly from the theme package?
- Should registry validation run in CI?
- How should component versioning work?
- Should custom third-party components be allowed in the registry?

---

## 29. Related Documents

- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
- Document 08 - Development Standards
- Document 11 - Layout Engine Specification
- Document 13 - Variant Engine Specification
- Document 14 - Universal Block System
- ADR 001 - Adopt Component-First Architecture

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Component Registry Specification document |
