# Shopify Theme Platform

**Document ID:** 70  
**Document Title:** AI Workflow  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# AI Workflow

## 1. Purpose

This document defines the standard workflow for using AI assistants in the Shopify Theme Platform. The workflow ensures AI work is scoped, documented, reviewed, and aligned with the platform architecture.

## 2. Workflow Overview

```text
Request
  -> Context Review
  -> Scope Definition
  -> Implementation or Documentation
  -> Verification
  -> Index Update
  -> Summary
```

## 3. Step 1: Request

The task should clearly define the expected output, target area, and any constraints.

## 4. Step 2: Context Review

AI should review relevant documents, ADRs, and existing files before acting.

## 5. Step 3: Scope Definition

The assistant should identify:

- Files to change
- Files not to change
- Risks
- Acceptance criteria

## 6. Step 4: Work Execution

AI should produce focused changes and avoid unrelated refactoring.

## 7. Step 5: Verification

Verification may include:

- File existence checks
- Markdown link checks
- Code checks
- Tests
- Manual review notes

## 8. Step 6: Documentation and Index Updates

When documents or public behaviour change, indexes and related documents should be updated.

## 9. Acceptance Criteria

- AI workflow is repeatable.
- AI work starts from project context.
- Verification is included.
- Final summaries explain what changed and what remains.

## 10. Related Documents

- Document 61 - AI Development Guide
- Document 62 - AI Coding Rules
- Document 63 - AI Context Files
- Document 69 - Documentation Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First AI workflow document |
