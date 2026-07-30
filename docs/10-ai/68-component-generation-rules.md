# Shopify Theme Platform

**Document ID:** 68  
**Document Title:** Component Generation Rules  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Component Generation Rules

## 1. Purpose

This document defines how AI assistants should generate Shopify Theme Platform components. Generated components must follow the architecture, design system, accessibility rules, and documentation standards.

## 2. Required Inputs

Before generating a component, AI should know:

- Component purpose
- Target merchant use case
- Supported variants
- Supported blocks
- Required design tokens
- Accessibility requirements
- Responsive behaviour
- Related component documents

## 3. Generation Rules

AI-generated components should:

- Prefer existing component patterns.
- Use variant-based layouts where suitable.
- Use universal blocks where possible.
- Avoid hardcoded design values.
- Keep Liquid, CSS, and JavaScript responsibilities separate.
- Include schema settings that are clear to merchants.

## 4. Required Output

A generated component should include:

- Component file or files
- Settings schema
- Supported blocks
- Variant notes
- Styling rules
- JavaScript only when needed
- Documentation update
- Testing checklist

## 5. Do Not Generate

AI should not generate:

- Duplicate components with only minor layout changes
- Heavy JavaScript when CSS or Liquid is enough
- Hardcoded colours, spacing, or typography
- Inaccessible controls
- Undocumented settings

## 6. Acceptance Criteria

- Components follow platform architecture.
- Variants reduce duplication.
- Tokens are used correctly.
- Accessibility and responsive behaviour are included.
- Documentation is updated with generated behaviour.

## 7. Related Documents

- Document 05 - Component Architecture
- Document 14 - Universal Block System
- Document 37 - Component API
- Document 62 - AI Coding Rules

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First component generation rules document |
