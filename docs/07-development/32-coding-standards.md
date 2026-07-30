# Shopify Theme Framework

**Document ID:** 32  
**Document Title:** Coding Standards  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Coding Standards

## 1. Purpose

This document defines general coding standards for the Shopify Theme Framework.

These standards apply across theme code, companion app code, shared packages, scripts, tests, and AI-assisted development.

---

## 2. Coding Vision

Code should remain understandable, maintainable, and aligned with the documented architecture.

```text
Readable first. Reusable when useful. Performant by default.
```

---

## 3. General Rules

- Prefer existing patterns over new abstractions.
- Keep changes focused.
- Avoid unnecessary dependencies.
- Avoid broad refactors without clear reason.
- Use clear names.
- Keep logic close to its ownership boundary.
- Document major architectural changes.
- Write tests when behaviour risk is meaningful.

---

## 4. Naming Rules

- Use lowercase kebab-case for files.
- Use stable component IDs.
- Use clear variable names.
- Prefix framework CSS classes consistently, for example `stp-`.
- Avoid unclear abbreviations.

---

## 5. Component Rules

Components should:

- Have a clear purpose.
- Support documented variants.
- Use supported blocks.
- Consume design tokens.
- Expose stable styling hooks.
- Avoid duplicated logic.
- Include accessibility considerations.
- Include performance considerations.

---

## 6. Settings Rules

Settings should:

- Use merchant-friendly labels.
- Follow standard groups: Content, Layout, Design, Behaviour, Features, Responsive, Advanced.
- Provide safe defaults.
- Hide advanced complexity until needed.
- Map visual settings to tokens where possible.

---

## 7. Dependency Rules

Dependencies should be intentional.

- Avoid dependencies for small behaviours.
- Prefer native platform capabilities.
- Document required dependencies.
- Keep third-party scripts optional.
- Avoid dependencies that block storefront rendering.

---

## 8. Review Checklist

Review changes for:

- Architecture consistency
- Component reuse
- Theme Editor clarity
- Performance impact
- Accessibility impact
- Skin compatibility
- Documentation updates
- Test coverage

---

## 9. AI Assistant Rules

AI assistants should:

- Read relevant docs before implementation.
- Avoid inventing undocumented patterns.
- Keep changes scoped.
- Update docs when architecture changes.
- Preserve existing user work.

---

## 10. Acceptance Criteria

Coding standards are successful when contributors can build consistently without creating scattered patterns, duplicated logic, or unclear behaviour.

---

## Related Documents

- Document 08 - Development Standards
- Document 31 - Folder Structure
- Document 33 - Liquid Standards
- Document 34 - JavaScript Standards
- Document 35 - CSS Architecture

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Coding Standards document |
