# Shopify Theme Framework

**Document ID:** 21  
**Document Title:** Hero Components  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Hero Components

## 1. Purpose

This document defines the Hero Components category for the Shopify Theme Framework.

Hero components are primary page-introduction and campaign sections used to communicate value, promote products, introduce collections, and guide visitors toward important actions.

---

## 2. Component Vision

Hero components should be flexible enough for simple stores and powerful enough for premium brand storytelling.

The guiding principle is:

```text
Clear message. Strong structure. Skin-ready presentation.
```

---

## 3. Primary Use Cases

- Homepage introduction
- Product launch
- Collection promotion
- Seasonal campaign
- Brand storytelling
- Single-product landing page
- Newsletter or lead capture entry point

---

## 4. Initial Hero Components

- Basic Hero
- Split Hero
- Full-Bleed Hero
- Product-Focused Hero
- Collection Hero
- Campaign Hero
- Newsletter Hero
- Video Hero, optional advanced

---

## 5. Supported Variants

- Centered content
- Content left, media right
- Media left, content right
- Full-bleed background
- Product highlight
- Collection highlight
- Minimal announcement
- Video background, advanced only

---

## 6. Supported Blocks

- Badge
- Heading
- Text
- Rich Text
- Button
- Button Group
- Image
- Video
- Product Card
- Collection Card
- Trust Badge
- Newsletter Form

---

## 7. Settings Strategy

Basic settings:

- Heading
- Text
- Primary button
- Image or media
- Layout preset

Advanced settings:

- Container width
- Content alignment
- Media position
- Spacing
- Responsive stacking
- Animation
- Token overrides
- Custom classes

---

## 8. Skin and Template Compatibility

Hero components must support the base mono design system and advanced skins.

Skins may change typography, button style, spacing, media treatment, and visual mood without replacing hero structure.

---

## 9. Accessibility Requirements

- Preserve correct heading hierarchy.
- Support readable text contrast.
- Provide alt text for media.
- Ensure buttons have clear labels.
- Avoid autoplay video by default.
- Respect reduced motion settings.

---

## 10. Performance Requirements

- Lazy-load non-critical media.
- Avoid heavy video defaults.
- Load video scripts only when needed.
- Define media dimensions to reduce layout shift.
- Keep base hero CSS lightweight.

---

## 11. MVP Scope

First release should include Basic Hero, Split Hero, Full-Bleed Hero, and Product-Focused Hero.

---

## 12. Related Documents

- Document 05 - Component Architecture
- Document 11 - Layout Engine Specification
- Document 13 - Variant Engine Specification
- Document 14 - Universal Block System

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Hero Components specification |
