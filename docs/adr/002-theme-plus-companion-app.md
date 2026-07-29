# ADR 002: Use Theme plus Companion App Architecture

**Status:** Accepted  
**Date:** July 30, 2026

---

## Context

The product vision includes onboarding, feature management, skins, templates, licensing, analytics, recommendations, and future AI-assisted workflows.

Some of these capabilities are not suitable to implement entirely inside a Shopify theme without creating unnecessary complexity or performance risk.

---

## Decision

We will use a hybrid architecture:

```text
Shopify Theme
  + Companion Shopify App
```

The theme will own storefront rendering, core sections, blocks, layout behaviour, and base design system.

The companion app will own richer onboarding, feature management, skins and templates library, analytics, licensing, recommendations, and cloud configuration where needed.

---

## Consequences

Positive consequences:

- Theme remains lightweight
- Advanced features can evolve independently
- Better merchant onboarding
- Easier premium feature management
- Better foundation for future AI features

Tradeoffs:

- Adds app development complexity
- Requires safe app-theme communication
- Requires clear failure behaviour if the app is unavailable

---

## Related Documents

- Document 03 - Technical Architecture
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
