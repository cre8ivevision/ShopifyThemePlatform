# Shopify Theme Platform

**Document ID:** 64  
**Document Title:** Cursor Rules  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Cursor Rules

## 1. Purpose

This document defines recommended rules for using Cursor with the Shopify Theme Platform. Cursor should operate from repository documentation, follow project conventions, and avoid generating inconsistent architecture.

## 2. Cursor Usage Principles

- Use documentation as the source of truth.
- Keep prompts specific and scoped.
- Ask Cursor to reference relevant docs before editing.
- Prefer small changes over broad rewrites.
- Review all generated changes before merging.

## 3. Recommended Cursor Context

Cursor should be pointed to:

- README.md
- Technical Architecture
- Development Standards
- Component Architecture
- Design Tokens Specification
- Relevant ADRs
- Relevant component documents

## 4. Suggested Rule Categories

| Category | Purpose |
|---|---|
| Architecture | Preserve engine-based platform structure |
| Components | Follow reusable component rules |
| Styling | Use design tokens and CSS standards |
| JavaScript | Keep scripts modular and lightweight |
| Liquid | Follow Shopify and Liquid standards |
| Documentation | Update docs when behaviour changes |

## 5. Prompting Guidelines

Good Cursor prompts should include:

- Target document or file
- Desired change
- Relevant constraints
- Acceptance criteria
- Files that should not be changed

## 6. Review Checklist

Before accepting Cursor output, check:

- Does it follow documented architecture?
- Did it duplicate existing logic?
- Are tokens used correctly?
- Is accessibility preserved?
- Is performance protected?
- Are docs updated where needed?

## 7. Acceptance Criteria

- Cursor work remains scoped.
- Cursor uses project documentation.
- Generated changes are reviewable.
- Cursor does not create undocumented architecture.

## 8. Related Documents

- Document 61 - AI Development Guide
- Document 62 - AI Coding Rules
- Document 63 - AI Context Files
- Document 69 - Documentation Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First Cursor rules document |
