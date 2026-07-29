# Shopify Theme Framework

**Document ID:** 04  
**Document Title:** Design System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Design System

## 1. Purpose

This document defines the design system strategy for the Shopify Theme Framework.

The design system must support a minimal default experience while allowing merchants to move from a basic visual foundation to advanced, premium, industry-specific design systems through skins, templates, presets, and controlled design tokens.

The goal is to keep the default theme simple, clean, fast, and easy to understand, while making the framework capable of supporting high-end storefront experiences without requiring a theme replacement.

---

## 2. Design System Vision

The Shopify Theme Framework should ship with a minimal base design system by default.

This base system should behave like a neutral mono foundation:

- Simple
- Lightweight
- Clean
- Accessible
- Predictable
- Easy to customise
- Performance-friendly
- Not visually opinionated

Advanced visual quality should be introduced through optional skins, templates, and preset packs rather than being forced into the default experience.

This creates a system where merchants can start simple and grow into a more polished, premium design experience over time.

---

## 3. Core Design Philosophy

### Minimal by Default

The default visual system should not overwhelm the merchant.

It should provide enough structure to make the store usable and professional, but it should avoid heavy styling, complex effects, excessive animations, or highly specific visual direction.

### Progressive Visual Enhancement

The framework should allow merchants to upgrade the visual experience gradually.

A merchant may begin with the base system and later apply:

- A skin
- A template pack
- A section preset pack
- An industry-specific design pack
- A premium layout pack
- Advanced typography and colour systems

### Structure Before Styling

The framework architecture should prioritise structure first.

Sections, components, blocks, layout variants, and responsive rules should work independently of any specific visual skin.

### Design Tokens Over Hardcoded Styling

Every visual decision should be controlled through design tokens whenever possible.

This allows the same component structure to support multiple design directions without duplicating component code.

### Familiar but Original

The framework may support familiar workflows inspired by common website builders, but it should not copy any platform interface or brand-specific design language.

The goal is to reduce the learning curve while maintaining a unique Shopify-native product experience.

---

## 4. Base Design System

The base design system is the default design layer included with the framework.

It should be intentionally simple and neutral.

### Base System Characteristics

- Neutral colour palette
- Simple typography scale
- Conservative spacing
- Minimal shadows
- Minimal border radius
- Accessible contrast
- Mobile-first behaviour
- Clean product presentation
- Low visual noise
- Fast rendering

### Base System Responsibilities

The base design system should provide:

- Default typography
- Default spacing
- Default containers
- Default grid behaviour
- Default button styles
- Default form styles
- Default product card styles
- Default media handling
- Default accessibility behaviour

### Base System Non-Goals

The base system should not attempt to provide:

- Highly decorative layouts
- Heavy animations
- Industry-specific visuals
- Strong brand personality
- Complex visual effects
- Large design libraries by default

Those should be handled through optional skins and templates.

---

## 5. Skin Layer

A skin is a visual layer that changes the look and feel of the framework without changing the underlying structure.

Skins should sit above the base system and should primarily modify design tokens, component styling rules, and preset selections.

### Skin Responsibilities

A skin may define:

- Colour palette
- Typography pairing
- Spacing rhythm
- Border radius system
- Shadow style
- Button style
- Card style
- Image treatment
- Animation style
- Section mood
- Component visual defaults

### Skin Non-Responsibilities

A skin should not:

- Replace core component logic
- Break layout compatibility
- Require duplicated sections
- Introduce unnecessary JavaScript
- Make the theme dependent on external services

### Example Skins

- Mono Minimal
- Editorial Luxury
- Fashion Premium
- Beauty Soft
- Tech Clean
- Health Trust
- B2B Professional
- Bold Campaign
- Lifestyle Warm
- High-Conversion Commerce

---

## 6. Template Packs

A template pack is a higher-level design package that includes page-level and section-level compositions.

Template packs should combine components, variants, blocks, layout rules, and skin defaults into complete storefront experiences.

### Template Pack Examples

- Fashion Store Starter
- Beauty Brand Launch
- Single Product Landing Page
- Supplements Store
- B2B Catalogue
- Digital Product Store
- Luxury Brand Store
- Minimal Portfolio Commerce

### Difference Between Skins and Templates

| Layer | Purpose | Example |
| --- | --- | --- |
| Base Design System | Neutral default foundation | Mono base |
| Skin | Changes visual personality | Luxury, Clean, Bold |
| Template Pack | Provides ready-made page compositions | Fashion homepage, product launch page |
| Preset | Configures a specific section or component | Hero variant with image left and CTA right |

---

## 7. Preset System

Presets provide ready-made configurations for sections and components.

A preset should help merchants avoid starting from a blank section.

### Preset Types

- Section presets
- Component presets
- Layout presets
- Block presets
- Page presets
- Industry presets
- Campaign presets

### Preset Goals

- Speed up store creation
- Reduce decision fatigue
- Support beginner users
- Provide professional defaults
- Maintain consistency across the store

---

## 8. Progressive Design Upgrade Path

The framework should support a clear design progression path.

```text
Base System
  -> Skin
  -> Preset Pack
  -> Template Pack
  -> Advanced Design System
  -> Custom Brand System
```

This path allows a merchant to start with a simple store and later evolve into a sophisticated storefront without changing themes.

### Stage 1: Basic

The merchant uses the default mono-style base system.

Focus:

- Fast setup
- Basic brand colours
- Basic typography
- Essential layouts

### Stage 2: Polished

The merchant applies a skin.

Focus:

- Improved visual personality
- Better spacing rhythm
- Stronger component styling
- More refined storefront appearance

### Stage 3: Professional

The merchant applies templates and preset packs.

Focus:

- Conversion-focused layouts
- Industry-specific sections
- Better storytelling
- More complete page systems

### Stage 4: Advanced

The merchant, designer, or agency customises the design token system deeply.

Focus:

- Custom brand system
- Advanced layout control
- Multiple page experiences
- Campaign-specific design patterns

---

## 9. Design Token Architecture

Design tokens are the foundation of the design system.

Tokens should control reusable values such as:

- Colours
- Typography
- Spacing
- Radius
- Shadows
- Borders
- Breakpoints
- Motion
- Z-index
- Component density

### Token Inheritance

```text
Framework Defaults
  -> Base Design System
  -> Active Skin
  -> Template Pack Defaults
  -> Global Theme Settings
  -> Section Settings
  -> Block Settings
  -> Manual Overrides
```

Lower levels may override higher levels, but overrides should remain controlled and predictable.

---

## 10. Visual Complexity Levels

The design system should support multiple visual complexity levels.

| Level | Name | Description |
| --- | --- | --- |
| 1 | Basic | Minimal design controls and neutral defaults |
| 2 | Standard | More layout and styling options |
| 3 | Advanced | Detailed design token controls |
| 4 | Designer | Full visual system control |
| 5 | Developer | Low-level configuration and extension points |

The Theme Editor experience should reveal controls progressively based on the selected user level.

---

## 11. Layout and Spacing Principles

The design system should support consistent layout behaviour across all components.

### Layout Modes

- Full width
- Boxed
- Contained
- Split
- Grid
- Flex
- Multi-column
- Floating
- Stacked

### Spacing Principles

- Use tokens instead of arbitrary spacing values.
- Provide simple spacing controls for beginners.
- Provide advanced spacing controls for designers and developers.
- Maintain consistent spacing rhythm across sections.
- Ensure mobile spacing is treated as a first-class concern.

---

## 12. Typography Principles

Typography should be simple by default and expandable through skins.

### Base Typography

- One default font family
- Clear heading scale
- Readable body text
- Accessible line height
- Predictable font weights

### Skin Typography

Skins may introduce:

- Font pairings
- Editorial scales
- Luxury typography
- High-conversion commerce typography
- Brand-specific type systems

---

## 13. Colour Principles

The base colour system should be neutral and accessible.

Skins may introduce stronger colour personalities.

### Colour Token Categories

- Background
- Surface
- Text
- Muted text
- Primary
- Secondary
- Accent
- Border
- Success
- Warning
- Error
- Sale

Colour tokens should support light and dark modes in future versions, even if dark mode is not included in the initial release.

---

## 14. Component Styling Rules

Components should consume design tokens rather than hardcoded styles.

Each component should support:

- Base styling
- Skin styling
- Variant styling
- State styling
- Responsive styling
- Accessibility styling

### Component States

- Default
- Hover
- Focus
- Active
- Disabled
- Loading
- Empty
- Error

---

## 15. Accessibility Standards

The design system should follow accessibility best practices from the beginning.

Requirements include:

- Strong text contrast
- Visible focus states
- Keyboard navigation support
- Readable font sizes
- Clear interactive states
- Sufficient tap targets
- Semantic structure
- Reduced motion support

Accessibility should not be treated as an optional skin feature. It belongs to the base system.

---

## 16. Performance Rules

The design system must remain performance-friendly.

Rules:

- Do not load unused skin assets.
- Do not load unused template assets.
- Avoid unnecessary JavaScript for visual styling.
- Prefer CSS variables and tokens.
- Keep the base system lightweight.
- Load advanced effects only when enabled.

---

## 17. Recommended Mechanism

The recommended mechanism is a layered design architecture:

```text
Base Design System
  + Active Skin
  + Optional Template Pack
  + Section Presets
  + Merchant Brand Overrides
```

This is better than making the default theme visually heavy.

It gives beginners a simple start while allowing advanced users to reach a premium visual standard when they are ready.

---

## 18. Acceptance Criteria

The design system will be considered successful when:

- A merchant can launch with the base design system without confusion.
- A merchant can apply a skin without rebuilding the store.
- A merchant can apply template packs without changing the theme.
- Components continue working across multiple skins.
- Visual upgrades do not require duplicated component logic.
- Unused skins and templates do not affect performance.
- Design tokens remain the source of truth for visual styling.
- Accessibility remains built into the base system.

---

## 19. Open Questions

- Should skins be included inside the theme package, delivered through the companion app, or both?
- Should premium skins be sold separately?
- Should users be allowed to create and export their own skins?
- How much skin customisation should be available inside Shopify Theme Editor?
- Which skins should be included in the first release?
- Should template packs be industry-specific from day one or introduced later?

---

## 20. Related Documents

- Document 01 - Vision & Product Strategy
- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 09 - Design Tokens Specification
- Document 11 - Layout Engine Specification
- Document 16 - Feature Manager Architecture
- Document 17 - Onboarding Engine

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Design System document |
