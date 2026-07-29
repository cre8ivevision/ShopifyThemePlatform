# Shopify Theme Framework

**Document ID:** 05  
**Document Title:** Component Architecture  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Component Architecture

## 1. Purpose

This document defines the component architecture for the Shopify Theme Framework.

The component architecture is responsible for turning the framework vision into a reusable, scalable, maintainable system of sections, blocks, variants, presets, and design-compatible component patterns.

This document explains how components should be structured, registered, configured, rendered, extended, and reused across skins, templates, and future theme products.

---

## 2. Component Architecture Vision

The Shopify Theme Framework should not be built as a collection of isolated Shopify sections.

It should be built as a structured component platform where every visible storefront element follows consistent rules and can be reused across multiple contexts.

The long-term goal is to allow one component system to support:

- Multiple layouts
- Multiple skins
- Multiple industries
- Multiple template packs
- Multiple merchant experience levels
- Multiple future premium themes

A component should be treated as a reusable product asset, not as a one-time theme file.

---

## 3. Core Principles

### Component First

Every major storefront feature should be represented as a reusable component.

### Variants Over Duplication

A component should support multiple layout options through variants rather than requiring duplicate sections for every design.

### Blocks as Reusable Content Units

Blocks should be reusable wherever possible and should not be tightly locked to one section unless there is a clear reason.

### Design-System Compatibility

Components should consume design tokens and skin rules instead of hardcoded visual styles.

### Progressive Complexity

Beginner users should see simple component options. Advanced users, designers, and developers should be able to access deeper controls when needed.

### Performance by Default

Components should only load the assets they need.

---

## 4. Key Definitions

| Term | Definition |
| --- | --- |
| Component | A reusable storefront unit with structure, settings, variants, blocks, and styling hooks. |
| Section | A Shopify Online Store 2.0 section that may render one or more framework components. |
| Block | A reusable content element used inside sections or components. |
| Variant | A layout or behavioural variation of a component. |
| Preset | A predefined configuration of a section, component, layout, or block. |
| Skin | A visual layer that changes look and feel without changing component structure. |
| Template Pack | A page-level composition made from components, variants, presets, and skins. |
| Registry | A catalogue containing metadata for available components. |

---

## 5. Component Model

Each component should be described using a consistent model.

```text
Component
  -> Metadata
  -> Schema
  -> Settings
  -> Variants
  -> Blocks
  -> Presets
  -> Rendering Logic
  -> Styling Hooks
  -> Assets
  -> Accessibility Rules
  -> Performance Rules
```

This model allows every component to behave predictably across the framework.

---

## 6. Component Metadata

Each component should define metadata that can be used by the framework, documentation, AI assistants, and future companion app features.

Recommended metadata fields:

- Component ID
- Component name
- Component category
- Description
- Version
- Status
- Supported variants
- Supported blocks
- Supported skins
- Supported layout modes
- Required assets
- Optional assets
- Dependencies
- Accessibility requirements
- Performance notes
- Related documents

Example:

```json
{
  "id": "hero",
  "name": "Hero",
  "category": "Marketing",
  "version": "0.1",
  "status": "Draft",
  "supportsVariants": true,
  "supportsPresets": true,
  "supportsSkins": true
}
```

---

## 7. Component Categories

Initial component categories should include:

- Layout Components
- Header Components
- Footer Components
- Hero Components
- Product Components
- Collection Components
- Navigation Components
- Marketing Components
- Commerce Components
- Content Components
- Forms and Interactive Components
- Utility Components

These categories may evolve as the framework matures.

---

## 8. Section and Component Relationship

Shopify sections are the platform-level container. Framework components are the internal architecture.

A section may:

- Render a single component
- Render a configured component variant
- Render a component with reusable blocks
- Expose settings for a component
- Provide presets for quick merchant setup

Recommended model:

```text
Shopify Section
  -> Framework Component
    -> Variant
    -> Blocks
    -> Preset
    -> Design Tokens
```

This keeps Shopify compatibility while preserving a stronger internal framework structure.

---

## 9. Universal Block System

The Universal Block System allows common content blocks to be reused across multiple components.

Example universal blocks:

- Heading
- Text
- Rich Text
- Image
- Video
- Button
- Button Group
- Icon
- Badge
- Divider
- Product Card
- Collection Card
- Testimonial
- Review
- Accordion
- FAQ Item
- Form Field
- Newsletter Form
- Social Links
- Trust Badge

Universal blocks should follow shared styling, accessibility, and schema conventions.

---

## 10. Block Rules

Blocks should:

- Have clear names and purposes.
- Avoid unnecessary visual styling.
- Consume design tokens.
- Support responsive behaviour.
- Include accessibility rules where applicable.
- Be reusable across components when possible.
- Load assets only when needed.

Blocks should not:

- Contain unrelated business logic.
- Duplicate other block functionality.
- Force a specific skin.
- Break component-level layout rules.

---

## 11. Variant Architecture

Variants allow a component to support multiple layout patterns without duplicating the component.

Example Hero variants:

- Centered content
- Image left, content right
- Content left, image right
- Full-bleed background image
- Video background
- Product-focused hero
- Split-screen hero

Each variant should reuse shared component settings and only define what is different.

---

## 12. Variant Rules

Variants should:

- Share the same component identity.
- Reuse common settings where possible.
- Define layout-specific settings only when required.
- Support the active design skin.
- Maintain accessibility and responsive behaviour.
- Avoid duplicated HTML unless necessary.

Variants should not:

- Become separate components without a strong reason.
- Break the base component API.
- Require duplicated CSS and JavaScript for every layout.

---

## 13. Preset Architecture

Presets are predefined configurations designed to help merchants start faster.

Preset levels:

- Block preset
- Component preset
- Section preset
- Page preset
- Template pack preset
- Industry preset

Example Hero presets:

- Minimal announcement hero
- Product launch hero
- Fashion campaign hero
- B2B credibility hero
- Beauty brand hero
- Single product conversion hero

Presets should improve speed without locking users into rigid designs.

---

## 14. Skin Compatibility

Components should be skin-compatible by default.

A component should not know whether the active skin is minimal, luxury, bold, editorial, or commerce-focused.

Instead, it should expose styling hooks and consume tokens.

```text
Component Structure
  -> Token Hooks
  -> Skin Values
  -> Rendered Visual Output
```

This allows the same component to look minimal in the base system and premium under an advanced skin.

---

## 15. Component Styling Hooks

Each component should expose predictable styling hooks.

Examples:

- Wrapper
- Container
- Content area
- Media area
- Heading
- Text
- Button group
- Primary action
- Secondary action
- Decorative elements
- State indicators

These hooks allow skins and templates to style components consistently without changing component logic.

---

## 16. Component Settings Strategy

Component settings should be grouped into clear levels.

### Basic Settings

For beginners:

- Content
- Image
- Button text
- Button link
- Layout preset
- Visibility

### Standard Settings

For growing merchants:

- Spacing
- Alignment
- Container width
- Basic colour options
- Responsive behaviour

### Advanced Settings

For designers and agencies:

- Token overrides
- Variant-level settings
- Advanced layout controls
- Animation settings
- Device-specific settings

### Developer Settings

For technical users:

- Custom classes
- Data attributes
- Integration hooks
- Debug mode
- Experimental options

---

## 17. Progressive Disclosure

The component editor experience should reveal settings progressively.

Beginner users should not see every setting by default.

Recommended user levels:

- Basic
- Standard
- Advanced
- Designer
- Developer

The same component should support all levels without requiring separate versions.

---

## 18. Component Rendering Pipeline

Recommended rendering flow:

```text
Load component metadata
  -> Load merchant settings
  -> Resolve active variant
  -> Resolve active preset
  -> Resolve active skin
  -> Resolve design tokens
  -> Validate block configuration
  -> Render component markup
  -> Load required assets
  -> Apply accessibility rules
  -> Output final section
```

This keeps rendering predictable and traceable.

---

## 19. Asset Loading Rules

Components should only load assets when required.

Rules:

- Shared base CSS should remain minimal.
- Component CSS should load only when the component is used.
- Variant CSS should load only when the variant is active, where technically possible.
- JavaScript should be avoided unless necessary.
- Interactive components should lazy-load optional scripts.
- Skin assets should not load unless the skin is active.

---

## 20. Accessibility Requirements

Every component should define accessibility requirements.

Examples:

- Correct semantic HTML
- Keyboard support
- Visible focus states
- Accessible labels
- Image alt text support
- Proper heading structure
- Reduced motion support
- Error state messaging for forms

Accessibility belongs to the base component system, not only to skins.

---

## 21. Performance Requirements

Every component should be reviewed for performance impact.

Performance considerations:

- HTML size
- CSS size
- JavaScript usage
- Image loading
- Video loading
- Third-party dependencies
- Rendering cost
- Liquid complexity

Heavy features should be optional and disabled by default.

---

## 22. Component Registry

The Component Registry should act as the internal catalogue of available components.

It may support future features such as:

- Component discovery
- AI-assisted component generation
- Companion app recommendations
- Feature manager integration
- Documentation automation
- Component health tracking
- Dependency visibility

The registry should be designed early, even if the first implementation is simple.

---

## 23. Component Lifecycle

Recommended lifecycle:

```text
Proposed
  -> Designed
  -> Documented
  -> Built
  -> Tested
  -> Released
  -> Maintained
  -> Deprecated
  -> Replaced
```

Each component should have a clear status.

---

## 24. Initial Component Priority

The first release should prioritise foundational components.

### Core Layout Components

- Container
- Grid
- Columns
- Stack
- Spacer

### Storefront Structure

- Header
- Footer
- Announcement Bar
- Navigation

### Commerce Components

- Product Card
- Product Media
- Product Information
- Collection Grid
- Cart Drawer

### Marketing Components

- Hero
- Featured Collection
- Image with Text
- Testimonials
- FAQ
- Newsletter

---

## 25. Acceptance Criteria

The component architecture will be considered successful when:

- Components are reusable across multiple sections and templates.
- Variants reduce duplication.
- Universal blocks can be reused across components.
- Components work with the base design system and advanced skins.
- Presets speed up merchant setup.
- Beginner settings remain simple.
- Advanced controls remain available for designers and developers.
- Components avoid unnecessary CSS and JavaScript loading.
- Accessibility rules are built into the component system.

---

## 26. Open Questions

- Should every Shopify section map to exactly one framework component?
- Should the component registry be stored as JSON, Liquid schema metadata, or both?
- How much component metadata should be readable by the companion app?
- Should merchants be able to import/export component presets?
- Should custom components be supported in the first release or later?
- How should deprecated components be handled?

---

## 27. Related Documents

- Document 01 - Vision & Product Strategy
- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 06 - Theme Editor UX Specification
- Document 09 - Design Tokens Specification
- Document 11 - Layout Engine Specification
- Document 12 - Component Registry Specification
- Document 13 - Variant Engine Specification
- Document 14 - Universal Block System

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Component Architecture document |
