# Shopify Theme Platform

**Document ID:** 65  
**Document Title:** Claude Code Rules  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Claude Code Rules

## 1. Purpose

This document defines recommended rules for using Claude Code with the Shopify Theme Platform. Claude Code should be used as an implementation assistant that respects architecture, documentation, and review boundaries.

## 2. Usage Principles

- Start from repository documentation.
- Inspect existing files before editing.
- Make narrow, intentional changes.
- Avoid undocumented architecture changes.
- Preserve user work and unrelated files.
- Summarise changes clearly after completion.

## 3. Required Pre-Work

Before making code changes, Claude Code should inspect:

- Current file structure
- Relevant docs
- Existing implementation patterns
- Related tests or QA expectations
- Related ADRs

## 4. Implementation Rules

Claude Code should:

- Prefer existing conventions.
- Use shared utilities and components.
- Avoid large refactors unless requested.
- Keep commits logically grouped.
- Update docs when required.
- Run relevant checks when possible.

## 5. Documentation Workflows

For documentation tasks, Claude Code should:

- Preserve Markdown consistency.
- Maintain document IDs.
- Update related indexes.
- Keep revision history current.
- Link related documents.

## 6. Review Checklist

Before completion, verify:

- Requested files were created or updated.
- Indexes and links are correct.
- No unrelated changes were introduced.
- The final summary includes what changed and what remains.

## 7. Acceptance Criteria

- Claude Code follows documentation-first workflow.
- Changes are scoped and verifiable.
- Repository navigation remains updated.
- Architecture rules are preserved.

## 8. Related Documents

- Document 61 - AI Development Guide
- Document 62 - AI Coding Rules
- Document 63 - AI Context Files
- Document 64 - Cursor Rules

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First Claude Code rules document |
