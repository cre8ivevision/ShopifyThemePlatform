# Shopify Theme Framework

**Document ID:** 36  
**Document Title:** API Reference  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# API Reference

## 1. Purpose

This document defines the planned API reference strategy for the Shopify Theme Framework.

The API layer includes internal contracts between framework systems, theme metadata, companion app communication, feature state, registry data, configuration sync, and future extension points.

---

## 2. API Vision

APIs should make the framework predictable and extensible without exposing unnecessary complexity.

```text
Stable contracts. Clear ownership. Safe extension.
```

---

## 3. API Categories

Planned API categories:

- Component Registry API
- Component API
- Variant API
- Block API
- Design Token API
- Feature Manager API
- Settings API
- Asset Manifest API
- Companion App API
- Event API
- Hooks API

---

## 4. Internal API Rules

- APIs should be versioned where stability matters.
- APIs should avoid leaking implementation details.
- Inputs and outputs should be documented.
- Breaking changes should require migration notes.
- API behaviour should be testable.

---

## 5. Theme API Boundaries

Theme APIs may include Liquid-accessible metadata, JSON manifests, settings conventions, snippet contracts, and asset declarations.

Theme APIs should not depend on remote app availability for core storefront rendering.

---

## 6. Companion App API Boundaries

The companion app may read or manage configuration, feature state, recommendations, licensing, templates, skins, and setup progress.

App APIs must follow Shopify security and permission requirements.

---

## 7. MVP Scope

Initial API documentation should define:

- Component metadata contract
- Feature metadata contract
- Token naming contract
- Settings resolution contract
- Asset declaration contract
- Basic app-theme sync contract

---

## 8. Acceptance Criteria

The API Reference is successful when developers and AI assistants can understand system contracts without guessing from implementation files.

---

## Related Documents

- Document 12 - Component Registry Specification
- Document 15 - Theme Settings Architecture
- Document 16 - Feature Manager Architecture
- Document 37 - Component API
- Document 38 - Event System
- Document 39 - Hooks and Extension Points

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First API Reference document |
