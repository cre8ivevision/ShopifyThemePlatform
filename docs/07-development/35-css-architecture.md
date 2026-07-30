# Shopify Theme Framework

**Document ID:** 35  
**Document Title:** CSS Architecture  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# CSS Architecture

## 1. Purpose

This document defines the CSS architecture for the Shopify Theme Framework.

CSS should support the base design system, skins, templates, components, variants, blocks, responsive layouts, and accessibility states while staying lightweight and maintainable.

---

## 2. CSS Vision

The framework should use CSS as a structured design layer, not a scattered collection of styles.

```text
Token-driven. Component-scoped. Skin-ready. Performance-safe.
```

---

## 3. Core Principles

- Use design tokens.
- Keep base CSS minimal.
- Scope component styles.
- Separate skin styles from component logic.
- Avoid unnecessary global rules.
- Avoid unused CSS from inactive features.
- Support responsive behaviour consistently.
- Preserve accessibility states.

---

## 4. Recommended CSS Layers

```text
Base
Tokens
Layout
Utilities
Components
Blocks
Variants
Features
Skins
Templates
Overrides
```

Each layer should have a clear purpose.

---

## 5. Naming Strategy

Use a consistent framework prefix.

Example:

```css
.stp-section {}
.stp-container {}
.stp-hero {}
.stp-product-card {}
.stp-button {}
```

Avoid class names that are too generic and likely to conflict with app or merchant code.

---

## 6. Token Usage

CSS should use custom properties for design tokens.

Examples:

```css
color: var(--stp-color-text);
background: var(--stp-color-surface);
gap: var(--stp-space-4);
border-radius: var(--stp-radius-md);
```

Hardcoded repeated values should be avoided.

---

## 7. Component CSS

Component CSS should:

- Be scoped to the component.
- Use stable hooks.
- Support variants.
- Support skins through tokens.
- Avoid unnecessary specificity.
- Include responsive behaviour.
- Include focus and state styles.

---

## 8. Skin CSS

Skin CSS should override tokens and visual treatment without replacing component structure.

Skins may adjust:

- Colours
- Typography
- Spacing feel
- Radius
- Shadows
- Button style
- Card style
- Media treatment

---

## 9. Responsive CSS

Responsive CSS should be mobile-first.

Rules:

- Start with mobile-safe defaults.
- Add larger breakpoint enhancements.
- Avoid layout shifts.
- Keep text readable.
- Ensure tap targets are usable.

---

## 10. Accessibility CSS

CSS must preserve:

- Visible focus states
- Sufficient contrast
- Reduced motion support
- Readable text sizes
- Clear interactive states

---

## 11. Performance Rules

- Keep global CSS small.
- Avoid loading inactive skin CSS.
- Avoid loading disabled feature CSS.
- Avoid overly broad selectors.
- Avoid excessive animation defaults.
- Keep CSS maintainable and reviewable.

---

## 12. MVP Scope

Initial CSS architecture should include:

- Base CSS
- Token CSS
- Layout CSS
- Utility CSS
- Core component CSS
- Basic skin CSS
- Feature CSS separation

---

## 13. Acceptance Criteria

CSS architecture is successful when styles are predictable, token-driven, skin-compatible, responsive, accessible, and performance-conscious.

---

## Related Documents

- Document 04 - Design System
- Document 09 - Design Tokens Specification
- Document 18 - Performance Engine
- Document 20 - Asset Management System
- Document 32 - Coding Standards

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First CSS Architecture document |
