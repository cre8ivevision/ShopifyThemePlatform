# Shopify Theme Framework

**Document ID:** 30  
**Document Title:** Utility Components  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Utility Components

## 1. Purpose

This document defines Utility Components for the Shopify Theme Framework.

Utility components provide small reusable building blocks that support layout, spacing, visibility, messaging, embeds, placeholders, and developer workflows.

---

## 2. Component Vision

Utility components should solve common structural and support needs without becoming visually dominant.

```text
Small parts. Clear purpose. Reusable everywhere.
```

---

## 3. Initial Utility Components

- Container
- Spacer
- Divider
- Section Wrapper
- Grid Wrapper
- Stack Wrapper
- Visibility Controller
- Empty State
- Loading State
- Error State
- Icon
- Badge
- App Block Placeholder
- Custom Liquid, advanced only

---

## 4. Supported Variants

- Small spacer
- Medium spacer
- Large spacer
- Horizontal divider
- Vertical divider
- Contained wrapper
- Full-width wrapper
- Mobile-only visibility
- Desktop-only visibility

---

## 5. Supported Blocks

- Text
- Icon
- Badge
- Divider
- Spacer
- Custom Liquid
- App Block Placeholder

---

## 6. Settings Strategy

Basic settings:

- Size
- Visibility
- Alignment
- Simple style

Advanced settings:

- Responsive visibility
- Token overrides
- Custom classes
- Data attributes
- Developer notes

---

## 7. Accessibility Requirements

- Decorative utilities should not create noise for assistive technologies.
- Dividers should be semantic only when meaningful.
- Visibility controls must not hide critical accessible content incorrectly.
- Loading and error states must communicate clearly.

---

## 8. Performance Requirements

- Utility components should be lightweight.
- Avoid JavaScript unless necessary.
- Avoid unnecessary wrappers.
- Keep CSS small and reusable.

---

## 9. MVP Scope

First release should include Container, Spacer, Divider, Section Wrapper, Empty State, Loading State, Error State, Icon, Badge, and App Block Placeholder.

---

## 10. Related Documents

- Document 05 - Component Architecture
- Document 11 - Layout Engine Specification
- Document 14 - Universal Block System

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Utility Components specification |
