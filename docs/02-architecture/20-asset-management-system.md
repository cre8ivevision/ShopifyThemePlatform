# Shopify Theme Framework

**Document ID:** 20  
**Document Title:** Asset Management System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Asset Management System

## 1. Purpose

This document defines the Asset Management System for the Shopify Theme Framework.

The Asset Management System controls how CSS, JavaScript, images, fonts, icons, media, skin assets, template assets, component assets, variant assets, block assets, and feature assets are organised, loaded, optimised, and governed.

---

## 2. Asset Vision

The framework should support rich storefront experiences without loading unnecessary assets.

The guiding principle is:

```text
Organise clearly. Load conditionally. Optimise continuously.
```

---

## 3. Core Responsibilities

The Asset Management System is responsible for:

- Asset organisation
- Asset naming standards
- Conditional loading
- Component asset mapping
- Feature asset mapping
- Skin asset mapping
- Template asset mapping
- Media optimisation rules
- Font loading rules
- Icon strategy
- JavaScript loading rules
- CSS loading rules
- Performance governance

---

## 4. Asset Categories

Initial asset categories:

- Base CSS
- Component CSS
- Skin CSS
- Template CSS
- Utility CSS
- Component JavaScript
- Feature JavaScript
- App embed scripts
- Images
- Videos
- Fonts
- Icons
- JSON metadata

---

## 5. Naming Standards

Asset names should be predictable and lowercase kebab-case.

Examples:

```text
base.css
layout.css
tokens.css
hero.css
product-card.css
cart-drawer.js
skin-mono.css
skin-luxury.css
```

Names should describe purpose rather than implementation detail.

---

## 6. Folder Strategy

Recommended future structure:

```text
theme/assets/
  base.css
  tokens.css
  layout.css
  components/
  features/
  skins/
  templates/
  utilities/
  scripts/
  media/
```

Final Shopify-compatible structure may require assets to compile or copy into Shopify's supported `assets/` directory.

---

## 7. CSS Asset Rules

CSS should be modular and token-driven.

Rules:

- Keep base CSS minimal.
- Avoid loading all component CSS globally when possible.
- Keep skin CSS separate from base CSS.
- Keep feature CSS separate from base CSS.
- Use CSS variables for token values.
- Avoid unused CSS from inactive skins and features.

---

## 8. JavaScript Asset Rules

JavaScript should be used carefully.

Rules:

- Avoid unnecessary global scripts.
- Load scripts only for active features or components.
- Defer non-critical scripts.
- Keep modules small.
- Avoid heavy dependencies.
- Preserve functionality where possible without JavaScript.
- Keep interactive behaviours accessible.

---

## 9. Image and Media Rules

Media assets should be optimised for speed and clarity.

Rules:

- Use responsive image sizes.
- Define dimensions where possible.
- Lazy-load below-the-fold images.
- Avoid autoplay video by default.
- Provide fallback images for video sections.
- Warn users about heavy media choices.

---

## 10. Font Rules

Fonts can strongly affect performance.

Rules:

- Keep default typography lightweight.
- Avoid loading too many font families.
- Use system fonts where appropriate.
- Allow skins to define font strategy.
- Document performance impact for premium font pairings.

---

## 11. Icon Strategy

Icons should be consistent and lightweight.

Possible strategies:

- Inline SVG snippets
- Optimised icon sprite
- Limited built-in icon set
- Skin-specific icon styling through tokens

The first release should avoid heavy icon libraries unless clearly justified.

---

## 12. Component Asset Mapping

Each component should declare required and optional assets in the Component Registry.

Example:

```json
{
  "componentId": "hero",
  "requiredCss": ["hero.css"],
  "optionalJs": ["hero-video.js"]
}
```

This supports conditional loading and documentation.

---

## 13. Feature Asset Mapping

Each feature should declare asset requirements.

Example:

```json
{
  "featureId": "cart-drawer",
  "requiredCss": ["cart-drawer.css"],
  "requiredJs": ["cart-drawer.js"]
}
```

Disabled features should not load these assets.

---

## 14. Skin and Template Assets

Only active skin and relevant template assets should load.

Rules:

- Inactive skin CSS should not affect storefront output.
- Template assets should load only on relevant templates.
- Skin and template assets should not duplicate base component logic.

---

## 15. App Assets

Companion app assets should not block storefront rendering.

Rules:

- Keep app embeds optional.
- Avoid remote dependency for core storefront rendering.
- Load app-powered scripts only when enabled.
- Provide safe fallbacks when app assets fail.

---

## 16. Asset Performance Metadata

Assets should include metadata where useful:

- Asset type
- Owner system
- Required or optional
- Related component
- Related feature
- Performance impact
- Load condition
- Dependencies

---

## 17. Validation Rules

Future validation may check:

- Required assets exist.
- Disabled feature assets are not loaded.
- Inactive skin assets are not loaded.
- Asset names follow conventions.
- Heavy assets are documented.
- JavaScript modules are mapped to active features.

---

## 18. MVP Scope

The first version should support:

- Base CSS strategy
- Component CSS mapping
- Feature asset mapping
- Skin asset separation
- Conditional loading rules
- Media optimisation rules
- JavaScript loading guidelines

---

## 19. Future Enhancements

Future capabilities may include:

- Asset manifest generation
- Automated asset validation
- Asset performance dashboard
- AI asset optimisation recommendations
- Skin asset previews
- Per-template asset reports
- Bundle size monitoring

---

## 20. Acceptance Criteria

The Asset Management System will be successful when:

- Assets are organised predictably.
- Disabled features do not load assets.
- Inactive skins do not load styling.
- Components declare asset needs clearly.
- JavaScript remains minimal and modular.
- Media and fonts are managed with performance in mind.
- The system supports future automation.

---

## 21. Related Documents

- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 12 - Component Registry Specification
- Document 16 - Feature Manager Architecture
- Document 18 - Performance Engine
- Document 19 - Rendering Pipeline

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Asset Management System document |
