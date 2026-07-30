# Shopify Theme Framework

**Document ID:** 18  
**Document Title:** Performance Engine  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Performance Engine

## 1. Purpose

This document defines the Performance Engine for the Shopify Theme Framework.

The Performance Engine protects storefront speed while the framework grows from a minimal base theme into a powerful theme platform with components, variants, skins, templates, optional features, and companion app workflows.

---

## 2. Performance Vision

Performance is not an optimisation step at the end of development. It is a product feature.

The guiding principle is:

```text
Fast by default. Powerful by choice. Measured before release.
```

---

## 3. Core Responsibilities

The Performance Engine is responsible for:

- Conditional asset loading
- Component-level loading rules
- Feature-based loading rules
- Lazy loading
- Media optimisation
- Layout shift prevention
- Script loading strategy
- CSS loading strategy
- Skin and template performance rules
- Performance metadata
- Performance warnings
- Performance testing and release gates

---

## 4. Default Performance Strategy

The base theme should remain lightweight.

Default rules:

- Load only essential CSS.
- Load minimal JavaScript.
- Avoid heavy effects by default.
- Keep the default skin simple.
- Disable advanced features until needed.
- Prefer native browser capabilities.
- Avoid unnecessary third-party dependencies.

---

## 5. Component Performance

Every component should define performance metadata.

Metadata may include:

- CSS requirement
- JavaScript requirement
- Media requirement
- Lazy loading support
- Performance impact level
- Required assets
- Optional assets
- Known risks

Impact levels:

- Lightweight
- Moderate
- Heavy

---

## 6. Feature Performance

Features should not load assets when disabled.

Rules:

- Disabled features do not load CSS.
- Disabled features do not load JavaScript.
- Heavy features must be clearly labelled.
- Feature dependencies must be validated.
- App-powered features must not block storefront rendering.

---

## 7. Skin and Template Performance

Skins and templates can improve visual quality, but they must not make the theme unnecessarily heavy.

Rules:

- Only active skin assets should load.
- Template pack assets should load only where needed.
- Decorative effects should be optional.
- Premium visual treatments should have performance notes.
- Base design system must remain fast.

---

## 8. Media Performance

Media-heavy storefronts can quickly become slow.

Rules:

- Use responsive images.
- Lazy-load below-the-fold images.
- Define image dimensions where possible.
- Avoid video backgrounds by default.
- Provide fallbacks for video-heavy sections.
- Warn users when media choices may affect performance.

---

## 9. JavaScript Strategy

JavaScript should be modular and intentional.

Rules:

- Avoid large global scripts.
- Load scripts only for active components or features.
- Defer non-critical scripts.
- Avoid blocking rendering.
- Prefer progressive enhancement.
- Keep interactions accessible without unnecessary dependencies.

---

## 10. CSS Strategy

CSS should be token-driven and minimal.

Rules:

- Keep base CSS small.
- Use CSS custom properties for tokens.
- Scope component styles.
- Avoid unused skin CSS.
- Avoid excessive animations.
- Avoid layout-shift-causing styles.

---

## 11. Performance UX

Merchants should understand performance tradeoffs without needing technical knowledge.

Possible labels:

- Lightweight
- Moderate
- Heavy

The Theme Editor or companion app may show performance hints for heavy features, video sections, carousels, advanced animations, and app-powered integrations.

---

## 12. Testing and Benchmarks

Performance testing should include:

- Lighthouse checks
- Core Web Vitals review
- Mobile performance
- JavaScript size review
- CSS size review
- Image loading behaviour
- Layout shift review
- Theme editor preview behaviour

Exact benchmark targets will be defined in the Performance Benchmarks document.

---

## 13. MVP Scope

The first Performance Engine version should support:

- Minimal base CSS
- Conditional feature asset loading
- Component performance metadata
- Feature performance labels
- Lazy loading patterns
- Basic media optimisation rules
- Release performance checklist

---

## 14. Future Enhancements

Future capabilities may include:

- Performance dashboard
- Automated performance scoring
- AI performance recommendations
- Feature-level performance budgets
- Skin performance comparison
- Template performance preview
- Regression monitoring

---

## 15. Acceptance Criteria

The Performance Engine will be successful when:

- The base theme remains lightweight.
- Disabled features do not load unnecessary assets.
- Heavy features are clearly labelled.
- Components include performance metadata.
- Skins and templates do not harm performance unnecessarily.
- Performance is tested before release.

---

## 16. Related Documents

- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 07 - Companion App Architecture
- Document 16 - Feature Manager Architecture
- Document 19 - Rendering Pipeline
- Document 20 - Asset Management System

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Performance Engine document |
