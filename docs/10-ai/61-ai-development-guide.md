# Shopify Theme Platform

**Document ID:** 61  
**Document Title:** AI Development Guide  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# AI Development Guide

## 1. Purpose

This document defines how AI coding assistants should be used to support the Shopify Theme Platform. The goal is to make AI-assisted development consistent, safe, documented, and aligned with the platform architecture.

## 2. Scope

This guide applies to AI-assisted work across documentation, Liquid, JavaScript, CSS, Shopify theme structure, component generation, testing, and future companion app development.

## 3. Core Principles

- AI should follow the documented architecture.
- AI should read relevant documentation before generating code.
- AI should preserve existing patterns and naming conventions.
- AI should avoid inventing undocumented systems.
- AI should produce small, reviewable changes.
- AI should update documentation when decisions change.

## 4. Required Context Before AI Work

Before generating or changing work, AI assistants should review:

- Product vision
- Technical architecture
- Component architecture
- Design system
- Development standards
- Relevant component specification
- Relevant ADRs

## 5. AI Work Categories

| Category | Examples |
|---|---|
| Documentation | Drafting, updating, restructuring docs |
| Component Work | Creating or modifying Shopify theme components |
| Design System Work | Tokens, skins, patterns, templates |
| Development Work | Liquid, JavaScript, CSS, schemas |
| Testing Work | QA checklists, accessibility, performance checks |
| App Work | Companion app modules and APIs |

## 6. Human Review Requirements

AI-generated work should be reviewed for:

- Architectural alignment
- Shopify compatibility
- Maintainability
- Accessibility
- Performance
- Documentation accuracy
- Business fit

## 7. Guardrails

AI assistants should not:

- Rewrite architecture without approval.
- Duplicate components unnecessarily.
- Add heavy dependencies casually.
- Ignore Shopify platform constraints.
- Create undocumented feature behaviour.
- Change public APIs without updating docs.

## 8. Acceptance Criteria

- AI workflows are documentation-led.
- AI outputs are reviewable and consistent.
- AI work references relevant source documents.
- AI does not become a substitute for architecture governance.

## 9. Related Documents

- Document 03 - Technical Architecture
- Document 08 - Development Standards
- Document 62 - AI Coding Rules
- Document 69 - Documentation Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First AI development guide |
