# Shopify Theme Framework

**Document ID:** 39  
**Document Title:** Hooks and Extension Points  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Hooks and Extension Points

## 1. Purpose

This document defines hooks and extension points for the Shopify Theme Framework.

Hooks and extension points allow advanced users, developers, agencies, and future platform systems to extend behaviour without modifying core framework code unnecessarily.

---

## 2. Extension Vision

The framework should be extensible without becoming fragile.

```text
Extend safely. Preserve the core. Document every entry point.
```

---

## 3. Extension Categories

Potential extension categories:

- Component hooks
- Block hooks
- Layout hooks
- Token hooks
- CSS class hooks
- Data attribute hooks
- JavaScript events
- Feature hooks
- App integration hooks
- Template hooks

---

## 4. CSS Extension Points

Components should expose stable classes and token hooks for styling.

Custom CSS should be possible, but skins and tokens should remain the preferred styling path.

---

## 5. JavaScript Extension Points

JavaScript extension points may include events, module initialisation hooks, data attributes, and custom integration points.

They should be minimal and documented.

---

## 6. Liquid Extension Points

Liquid extension points may include snippets, app block placeholders, template slots, and documented section schema patterns.

Core rendering should remain stable.

---

## 7. App Extension Points

The companion app may extend onboarding, feature management, skins, templates, recommendations, and licensing.

The app should not be required for core storefront rendering.

---

## 8. Safety Rules

- Extension points must be documented.
- Avoid exposing unstable internals.
- Preserve accessibility.
- Preserve performance.
- Avoid allowing extensions to break core purchase flows.
- Provide fallback behaviour.

---

## 9. MVP Scope

Initial extension points should include stable CSS hooks, component data attributes, basic JavaScript events, app block placeholders, and custom class settings for developer mode.

---

## 10. Acceptance Criteria

Hooks and extension points are successful when advanced users can customise the framework while the core remains maintainable and safe.

---

## Related Documents

- Document 34 - JavaScript Standards
- Document 35 - CSS Architecture
- Document 37 - Component API
- Document 38 - Event System

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Hooks and Extension Points document |
