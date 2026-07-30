# Shopify Theme Platform

**Document ID:** 66  
**Document Title:** Prompt Library  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Prompt Library

## 1. Purpose

This document defines reusable prompt patterns for AI-assisted work on the Shopify Theme Platform. The prompt library helps keep AI outputs consistent, scoped, and aligned with the documented architecture.

## 2. Prompt Principles

- Prompts should name the exact task and target files.
- Prompts should include relevant document references.
- Prompts should define acceptance criteria.
- Prompts should tell AI what not to change.
- Prompts should require a summary of changes.

## 3. Prompt Categories

| Category | Purpose |
|---|---|
| Documentation | Create or update Markdown documents |
| Component | Generate or revise components |
| Design System | Work with tokens, skins, and UI rules |
| Testing | Create QA and validation checklists |
| Refactoring | Improve code without changing behaviour |
| Review | Inspect work for gaps or risks |

## 4. Documentation Prompt Template

```text
Create or update [document name].
Use official English Markdown.
Follow the repository documentation structure.
Reference these documents: [list].
Do not change unrelated files.
Update indexes if needed.
Return a concise summary of changes.
```

## 5. Component Prompt Template

```text
Create a Shopify component for [purpose].
Follow Document 05, Document 37, and relevant design documents.
Use design tokens.
Support accessibility and responsive behaviour.
Avoid duplicate logic.
Document settings and variants.
```

## 6. Review Prompt Template

```text
Review [files] for architecture alignment, accessibility, performance, and documentation consistency.
List findings by severity.
Do not rewrite unless asked.
```

## 7. Acceptance Criteria

- Prompt templates are reusable.
- Prompts reference source documents.
- Prompts reduce ambiguity.
- Prompts support reviewable outputs.

## 8. Related Documents

- Document 61 - AI Development Guide
- Document 62 - AI Coding Rules
- Document 63 - AI Context Files
- Document 69 - Documentation Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First prompt library document |
