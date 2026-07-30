# Shopify Theme Platform

**Document ID:** 63  
**Document Title:** AI Context Files  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# AI Context Files

## 1. Purpose

This document defines the context files that should be provided to AI coding assistants so they can understand the Shopify Theme Platform before producing work.

## 2. Context Strategy

AI context should be structured, concise, and relevant. Assistants should receive enough information to make correct decisions without being overloaded by unrelated documents.

## 3. Core Context Files

| Context File | Purpose |
|---|---|
| Project Overview | Explains platform vision and current status |
| Architecture Summary | Summarises technical architecture and engines |
| Development Rules | Provides coding standards and constraints |
| Component Rules | Defines component generation expectations |
| Design Rules | Summarises design tokens, skins, and UI rules |
| Shopify Rules | Captures Shopify-specific constraints |
| ADR Index | Lists accepted architecture decisions |

## 4. Task-Specific Context

For each task, AI should receive:

- Relevant document IDs
- Target files
- Constraints
- Expected output
- Acceptance criteria
- Related ADRs

## 5. Context File Format

Context files should be written in Markdown and include:

- Purpose
- Scope
- Rules
- Examples
- Do not do list
- Related references

## 6. Maintenance Rules

Context files should be updated when:

- Architecture changes
- New coding rules are added
- New component conventions are introduced
- Design system decisions change
- Shopify platform constraints change

## 7. Acceptance Criteria

- AI context is modular and reusable.
- Context files reduce repeated explanations.
- Assistants receive task-relevant context.
- Context files stay aligned with project documentation.

## 8. Related Documents

- Document 61 - AI Development Guide
- Document 62 - AI Coding Rules
- Document 67 - Project Memory Structure
- Document 69 - Documentation Standards

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First AI context files document |
