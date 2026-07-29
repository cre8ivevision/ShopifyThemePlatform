# ADR 004: Use Minimal Base Design System with Skins and Templates

**Status:** Accepted  
**Date:** July 30, 2026

---

## Context

The framework should be simple for beginners but powerful enough for premium, high-end storefronts.

A visually heavy default theme would overwhelm beginners and increase performance risk.

---

## Decision

We will ship a minimal base design system by default and support advanced visual experiences through skins, template packs, and presets.

Recommended design progression:

```text
Base Design System
  -> Active Skin
  -> Optional Template Pack
  -> Section Presets
  -> Merchant Brand Overrides
```

---

## Consequences

Positive consequences:

- Beginners get a clean and simple start
- Advanced visual quality is still possible
- Components remain reusable across skins
- Theme performance remains protected

Tradeoffs:

- Requires strong design token architecture
- Requires skin compatibility rules
- Requires clear UX for selecting skins and templates

---

## Related Documents

- Document 04 - Design System
- Document 09 - Design Tokens Specification
