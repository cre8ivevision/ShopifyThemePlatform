# Shopify Theme Framework

**Document ID:** 31  
**Document Title:** Folder Structure  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Folder Structure

## 1. Purpose

This document defines the recommended repository and implementation folder structure for the Shopify Theme Framework.

The goal is to keep documentation, theme code, companion app code, shared packages, examples, scripts, and tests clearly separated.

---

## 2. Structure Vision

The repository should be organised like a long-term product platform, not a one-off theme.

```text
Clear folders. Clear ownership. Easy navigation.
```

---

## 3. Recommended Top-Level Structure

```text
shopify-theme-platform/
  README.md
  CHANGELOG.md
  CONTRIBUTING.md
  docs/
  theme/
  app/
  packages/
  examples/
  scripts/
  tests/
  .github/
```

---

## 4. Documentation Folder

```text
docs/
  00-foundation/
  01-product/
  02-architecture/
  03-design-system/
  04-components/
  05-theme-editor/
  06-companion-app/
  07-development/
  08-testing/
  09-business/
  10-ai/
  adr/
  roadmap/
```

Documentation should remain the source of truth for planning, architecture, standards, and decisions.

---

## 5. Theme Folder

Recommended future Shopify theme structure:

```text
theme/
  assets/
  config/
  layout/
  locales/
  sections/
  snippets/
  templates/
```

Additional source folders may exist before build output:

```text
theme/src/
  components/
  blocks/
  variants/
  tokens/
  skins/
  features/
  utilities/
```

Final implementation must remain compatible with Shopify theme requirements.

---

## 6. Companion App Folder

```text
app/
  frontend/
  backend/
  database/
  routes/
  services/
  workers/
  tests/
```

The companion app should be separated from storefront rendering concerns.

---

## 7. Packages Folder

Shared logic may live under `packages/` when needed.

Examples:

- registry schemas
- token utilities
- validation utilities
- shared TypeScript types, if used
- documentation generators

---

## 8. Tests Folder

```text
tests/
  theme/
  app/
  accessibility/
  performance/
  integration/
```

Testing structure may evolve with implementation.

---

## 9. Rules

- Keep generated files separate from source files.
- Do not mix documentation drafts with production implementation.
- Keep Shopify-compatible output clear.
- Use lowercase kebab-case file names.
- Keep component-related files discoverable.
- Avoid unclear catch-all folders.

---

## 10. Acceptance Criteria

The folder structure is successful when developers and AI assistants can quickly locate documentation, theme code, app code, shared logic, tests, and examples without guessing.

---

## Related Documents

- Document 08 - Development Standards
- Document 20 - Asset Management System
- Document 32 - Coding Standards

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Folder Structure document |
