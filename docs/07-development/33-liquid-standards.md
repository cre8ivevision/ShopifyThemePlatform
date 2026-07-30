# Shopify Theme Framework

**Document ID:** 33  
**Document Title:** Liquid Standards  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Liquid Standards

## 1. Purpose

This document defines Liquid coding standards for the Shopify Theme Framework.

Liquid should remain readable, predictable, safe, and aligned with Shopify Online Store 2.0 conventions.

---

## 2. Liquid Vision

Liquid should handle rendering, configuration resolution, and Shopify data output without becoming an unmaintainable logic layer.

```text
Simple Liquid. Clear rendering. Shared snippets.
```

---

## 3. General Rules

- Keep section files focused.
- Move repeated markup into snippets.
- Avoid deeply nested conditionals.
- Use meaningful variable names.
- Escape output where appropriate.
- Keep schema labels merchant-friendly.
- Avoid hardcoded styling where tokens can be used.

---

## 4. Section Rules

Sections should:

- Represent clear storefront areas.
- Use component architecture where possible.
- Support documented variants.
- Use supported blocks.
- Keep settings grouped clearly.
- Avoid becoming large monolithic files.

---

## 5. Snippet Rules

Snippets should be used for:

- Shared component markup
- Reusable blocks
- Icons
- Product card rendering
- Utility wrappers
- Repeated schema-adjacent rendering patterns

Snippets should avoid hidden side effects.

---

## 6. Schema Rules

Schema should:

- Use clear names and labels.
- Provide sensible defaults.
- Keep advanced settings grouped.
- Avoid excessive options in beginner-facing sections.
- Support presets where possible.

---

## 7. Variant Handling

Variant logic should be clear and controlled.

Preferred approaches:

- Use stable variant IDs.
- Keep shared markup common.
- Move variant-specific fragments into snippets when helpful.
- Avoid duplicating entire sections for minor layout changes.

---

## 8. Accessibility Rules

Liquid output should preserve:

- Semantic headings
- Image alt text
- Button labels
- Form labels
- ARIA attributes where needed
- Logical reading order

---

## 9. Performance Rules

Liquid should avoid:

- Rendering empty wrappers
- Repeating expensive loops unnecessarily
- Loading unused assets
- Large duplicated markup
- Unnecessary external scripts

---

## 10. Acceptance Criteria

Liquid standards are successful when theme files are readable, reusable, Shopify-compatible, accessible, and performance-conscious.

---

## Related Documents

- Document 08 - Development Standards
- Document 19 - Rendering Pipeline
- Document 32 - Coding Standards

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Liquid Standards document |
