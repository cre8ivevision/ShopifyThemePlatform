# Shopify Theme Framework

**Document ID:** 15  
**Document Title:** Theme Settings Architecture  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Theme Settings Architecture

## 1. Purpose

This document defines the Theme Settings Architecture for the Shopify Theme Framework.

The settings architecture controls how global settings, section settings, component settings, block settings, design tokens, skins, templates, presets, feature flags, and manual overrides work together.

Its goal is to provide a powerful but predictable configuration system that remains simple for beginners and flexible for advanced users, designers, developers, and agencies.

---

## 2. Settings Architecture Vision

The framework should not expose a confusing collection of unrelated settings.

Settings should behave as a structured system with clear inheritance, sensible defaults, progressive disclosure, and safe override rules.

The guiding principle is:

```text
Defaults create simplicity. Overrides create flexibility. Inheritance creates consistency.
```

---

## 3. Core Responsibilities

The Theme Settings Architecture is responsible for:

- Global theme configuration
- Section-level configuration
- Component-level configuration
- Block-level configuration
- Design token mapping
- Skin configuration
- Template pack configuration
- Preset configuration
- Feature activation settings
- Responsive settings
- User experience level settings
- Override resolution
- Reset and fallback behaviour

---

## 4. Settings Layers

The framework should use a clear settings hierarchy.

```text
Framework Defaults
  -> Base Theme Settings
  -> Active Skin Settings
  -> Active Template Pack Settings
  -> Global Merchant Settings
  -> Template Settings
  -> Section Settings
  -> Component Settings
  -> Block Settings
  -> Manual Overrides
```

Each lower layer may override higher layers only when necessary.

---

## 5. Framework Defaults

Framework defaults are the lowest-level fallback values.

They should provide safe, predictable behaviour even when no merchant customisation exists.

Examples:

- Default container width
- Default spacing scale
- Default typography scale
- Default colour system
- Default layout behaviour
- Default mobile behaviour
- Default accessibility settings

Framework defaults should rarely change after stable release.

---

## 6. Base Theme Settings

Base theme settings represent the default merchant-facing theme configuration.

They should define the minimal mono-style base system discussed in the product vision.

Examples:

- Base colours
- Base typography
- Base spacing
- Basic layout density
- Basic button style
- Basic product card style
- Basic header and footer behaviour

These settings should support a clean store without requiring advanced configuration.

---

## 7. Active Skin Settings

Active skin settings override base visual tokens and styling defaults.

A skin may define:

- Colour palette
- Typography pairing
- Spacing rhythm
- Radius system
- Shadow style
- Button style
- Card style
- Media treatment
- Animation style

Skin settings should not replace component structure or core rendering logic.

---

## 8. Active Template Pack Settings

Template packs may apply page-level and section-level configuration.

A template pack may define:

- Page structure
- Recommended sections
- Section order
- Component presets
- Layout variants
- Skin recommendations
- Initial content placeholders

Template pack settings should preserve merchant content wherever possible.

---

## 9. Global Merchant Settings

Global merchant settings are store-level preferences controlled by the merchant.

Examples:

- Brand colours
- Font choices
- Global container width
- Global spacing scale
- Button style preference
- Product card style
- Header behaviour
- Footer style
- Experience level
- Enabled features

These settings should be easy to understand and should affect the store consistently.

---

## 10. Template Settings

Template settings define behaviour for Shopify templates such as homepage, product page, collection page, page templates, and landing pages.

Examples:

- Product page layout
- Collection grid density
- Landing page width
- Template-specific section defaults
- Template-specific feature recommendations

Template settings should not override global settings without a clear reason.

---

## 11. Section Settings

Section settings control a specific section instance.

Examples:

- Section visibility
- Layout preset
- Container width
- Section spacing
- Background option
- Content alignment
- Component variant
- Enabled section features

Section settings should be grouped using the standard editor information architecture:

```text
Content
Layout
Design
Behaviour
Features
Responsive
Advanced
```

---

## 12. Component Settings

Component settings control the internal behaviour of a component.

Examples:

- Active variant
- Supported blocks
- Media position
- Content alignment
- Component density
- Component-specific design hooks
- Component interaction behaviour

Component settings should align with the Component Registry and Variant Engine.

---

## 13. Block Settings

Block settings control individual content units.

Examples:

- Text content
- Image source
- Alt text
- Button label
- Button link
- Block alignment
- Block visibility
- Block spacing

Block settings should stay simple by default and expose deeper controls only when necessary.

---

## 14. Manual Overrides

Manual overrides are the highest-priority settings.

They may include:

- Section-specific token overrides
- Block-specific alignment
- Custom classes
- Developer settings
- Device-specific overrides

Manual overrides should be powerful but controlled.

The system should avoid allowing beginners to create broken layouts accidentally.

---

## 15. Override Resolution Model

When multiple layers define the same value, the framework should resolve the final value predictably.

Example:

```text
Final Value = Manual Override
  else Block Setting
  else Component Setting
  else Section Setting
  else Template Setting
  else Global Merchant Setting
  else Active Template Pack Setting
  else Active Skin Setting
  else Base Theme Setting
  else Framework Default
```

This order should be documented and followed consistently.

---

## 16. Settings Grouping Standard

All settings should use consistent groups.

| Group | Purpose |
| --- | --- |
| Content | Text, media, products, collections, and links. |
| Layout | Structure, width, alignment, grid, flex, and spacing. |
| Design | Colours, typography, radius, shadows, and visual style. |
| Behaviour | Animation, sticky behaviour, collapsible behaviour, and interactions. |
| Features | Optional capabilities for the section or component. |
| Responsive | Device-specific behaviour. |
| Advanced | Developer or expert-level controls. |

---

## 17. Progressive Disclosure

Settings visibility should depend on the selected user experience level.

### Basic

- Content
- Simple layout preset
- Basic visibility
- Simple design choices

### Standard

- Layout options
- Basic spacing
- Basic design controls
- Common features

### Advanced

- Responsive overrides
- Token overrides
- Advanced feature controls
- Behaviour controls

### Designer

- Detailed visual settings
- Skin tuning
- Density controls
- Component-level design controls

### Developer

- Custom classes
- Data attributes
- Debug settings
- Experimental configuration

---

## 18. Feature Settings

Feature settings should integrate with the Feature Manager.

Feature settings should define:

- Feature name
- Description
- Enabled or disabled state
- Dependencies
- Performance impact
- Recommended user level
- Related components
- Required assets

Disabled features should not load unnecessary assets.

---

## 19. Responsive Settings

Responsive settings should be available progressively.

Basic users should receive safe mobile defaults.

Advanced users may control:

- Mobile stacking
- Mobile spacing
- Tablet layout
- Desktop layout
- Visibility by device
- Device-specific alignment

Responsive overrides should never break accessibility or reading order.

---

## 20. Settings and Design Tokens

Many visual settings should map to design tokens.

Examples:

- Brand colour maps to colour tokens.
- Font choices map to typography tokens.
- Spacing controls map to spacing tokens.
- Button style maps to component tokens.

The settings system should avoid hardcoded visual values where tokens can be used.

---

## 21. Settings and Skins

Skins should provide default token and component styling values.

Merchants may override skin values through global or section settings.

Rules:

- Skin defaults should be reversible.
- Skin changes should preserve content.
- Skin overrides should be documented.
- Applying a skin should not break existing layouts.

---

## 22. Settings and Presets

Presets should apply groups of settings quickly.

Preset types:

- Block presets
- Component presets
- Section presets
- Page presets
- Template pack presets

Applying a preset should make predictable changes and should not silently remove important merchant content.

---

## 23. Conflict Resolution

The settings system should handle conflicts safely.

Examples:

- A selected block is not supported by a selected variant.
- A layout setting conflicts with mobile behaviour.
- A skin does not fully support a component.
- A feature depends on another disabled feature.
- A manual override creates poor contrast or layout risk.

The system should provide safe fallbacks and helpful warnings where possible.

---

## 24. Reset and Fallback Behaviour

Users should be able to recover from unwanted settings changes.

Recommended reset options:

- Reset section to preset defaults
- Reset component to default settings
- Reset block settings
- Reset design overrides
- Reset to active skin defaults
- Reset to base theme defaults

The companion app may provide deeper configuration snapshots and rollback support.

---

## 25. Shopify Schema Considerations

Shopify theme settings and section schemas must remain understandable.

Rules:

- Avoid excessive settings in a single section.
- Use clear labels and grouping.
- Keep defaults sensible.
- Hide or collapse advanced controls where possible.
- Use presets to simplify setup.
- Avoid technical terms for beginner-facing settings.

Some advanced configuration may be better handled by the companion app.

---

## 26. Companion App Relationship

The companion app may provide a richer settings management layer.

The app may handle:

- Full onboarding wizard
- Feature Manager dashboard
- Skin selection
- Template pack selection
- Configuration snapshots
- Rollback
- Advanced recommendations
- Usage analytics
- Licensing-aware settings

The theme should still function with stored settings even when the app is unavailable.

---

## 27. AI Development Relationship

AI coding assistants should use the settings architecture to understand:

- Where settings belong
- Which layer owns each setting
- How overrides are resolved
- Which settings are beginner-facing
- Which settings are advanced or developer-only
- How settings map to tokens, variants, blocks, and features

This reduces inconsistent settings patterns.

---

## 28. MVP Scope

The first version should support:

- Framework defaults
- Base theme settings
- Global merchant settings
- Section settings
- Component variant settings
- Block settings
- Basic skin settings
- Basic preset settings
- Simple feature enable/disable settings
- Safe responsive defaults

Advanced rollback, configuration snapshots, and app-powered settings management can be added later.

---

## 29. Future Enhancements

Future capabilities may include:

- Configuration snapshots
- One-click rollback
- Saved setting profiles
- Store stage-based setting recommendations
- AI setting optimisation
- Skin-specific setting panels
- Template pack configuration wizard
- Agency-level configuration libraries
- Multi-store settings sync

---

## 30. Acceptance Criteria

The Theme Settings Architecture will be considered successful when:

- Settings follow predictable inheritance.
- Beginners are not overwhelmed by advanced options.
- Advanced users can access deeper controls.
- Skins, templates, presets, sections, components, and blocks work together safely.
- Feature settings can control optional capabilities.
- Disabled features do not load unnecessary assets.
- Manual overrides are powerful but controlled.
- Settings can be reset or safely restored where possible.
- AI assistants can follow consistent settings patterns.

---

## 31. Open Questions

- Which settings should live in Shopify Theme Editor versus the companion app?
- How many settings should be exposed in beginner mode?
- Should settings visibility be controlled by a global experience level?
- How should theme settings be migrated between versions?
- Should configuration snapshots be included in the first app release?
- Should merchants be able to export settings as reusable profiles?

---

## 32. Related Documents

- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
- Document 09 - Design Tokens Specification
- Document 11 - Layout Engine Specification
- Document 12 - Component Registry Specification
- Document 13 - Variant Engine Specification
- Document 14 - Universal Block System
- Document 16 - Feature Manager Architecture
- ADR 003 - Adopt Progressive Disclosure for Merchant UX
- ADR 004 - Use Minimal Base Design System with Skins and Templates

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Theme Settings Architecture document |
