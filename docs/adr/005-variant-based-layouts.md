# ADR 005: Prefer Variant-Based Layouts over Duplicate Sections

**Status:** Accepted  
**Date:** July 30, 2026

---

## Context

A single storefront component may need multiple layout styles, such as centered, split, grid, full-width, boxed, or media-first layouts.

Creating a separate section for every layout leads to duplication and maintenance problems.

---

## Decision

We will prefer variant-based layouts.

A component should support multiple layout variants through a shared component model instead of duplicating the entire section for each layout.

---

## Consequences

Positive consequences:

- Less duplicated code
- More consistent settings
- Easier skin compatibility
- Easier future extension

Tradeoffs:

- Variant logic must remain controlled
- Component schemas need careful organisation
- Documentation must clearly describe variant behaviour

---

## Related Documents

- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 11 - Layout Engine Specification
- Document 13 - Variant Engine Specification
