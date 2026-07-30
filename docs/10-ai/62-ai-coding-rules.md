# Shopify Theme Platform

**Document ID:** 62  
**Document Title:** AI Coding Rules  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# AI Coding Rules

## 1. Purpose

This document defines rules AI coding assistants must follow when generating or modifying code for the Shopify Theme Platform.

## 2. General Rules

- Follow existing project architecture.
- Prefer documented patterns over new abstractions.
- Keep changes small and focused.
- Do not duplicate existing components.
- Do not introduce dependencies without justification.
- Keep storefront performance as a core requirement.
- Preserve accessibility requirements.

## 3. Shopify Theme Rules

AI-generated Shopify theme work must:

- Follow Shopify Online Store 2.0 conventions.
- Use Liquid responsibly and clearly.
- Keep section schemas understandable.
- Avoid unsafe output patterns.
- Use snippets and components consistently.
- Keep feature settings aligned with the Feature Manager.

## 4. Component Rules

When creating components, AI should:

- Check the Component Registry concept.
- Define component purpose and supported variants.
- Use shared blocks where possible.
- Use design tokens instead of hardcoded values.
- Document settings and dependencies.
- Include accessibility expectations.

## 5. CSS Rules

AI-generated CSS should:

- Use design tokens.
- Avoid one-off styling when a system token exists.
- Keep selectors predictable.
- Avoid excessive specificity.
- Support responsive behaviour.
- Respect reduced motion settings.

## 6. JavaScript Rules

AI-generated JavaScript should:

- Be minimal and modular.
- Avoid blocking rendering.
- Use event patterns consistently.
- Avoid global state unless documented.
- Support cleanup where needed.
- Degrade gracefully.

## 7. Documentation Rules

Code changes should update documentation when they affect:

- Component behaviour
- Public APIs
- Settings schema
- Design tokens
- Feature activation
- Architecture decisions

## 8. Acceptance Criteria

- AI-generated code follows platform rules.
- Components remain reusable and documented.
- Performance and accessibility are protected.
- Documentation stays aligned with implementation.

## 9. Related Documents

- Document 32 - Coding Standards
- Document 33 - Liquid Standards
- Document 34 - JavaScript Standards
- Document 35 - CSS Architecture

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First AI coding rules document |
