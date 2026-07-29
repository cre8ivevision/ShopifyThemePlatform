# ADR 003: Adopt Progressive Disclosure for Merchant UX

**Status:** Accepted  
**Date:** July 30, 2026

---

## Context

Shopify merchants have different skill levels. Some are beginners building their first store, while others are designers, developers, agencies, or advanced merchants.

Showing every possible setting to every user creates confusion and increases support burden.

---

## Decision

We will adopt progressive disclosure across onboarding, theme settings, component settings, feature management, skins, templates, and advanced controls.

The editor experience will support levels such as:

- Basic
- Standard
- Advanced
- Designer
- Developer

---

## Consequences

Positive consequences:

- Beginners see a simpler interface
- Advanced users still get deeper control
- Theme can grow with the merchant
- User experience becomes a product advantage

Tradeoffs:

- Requires careful settings architecture
- Requires clear defaults
- Requires thoughtful UX writing and grouping

---

## Related Documents

- Document 02 - Product Requirements Document
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
