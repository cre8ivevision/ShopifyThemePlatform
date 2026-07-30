# Shopify Theme Platform

**Document ID:** 67  
**Document Title:** Project Memory Structure  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Project Memory Structure

## 1. Purpose

This document defines how reusable project knowledge should be organised for AI assistants and future contributors. Project memory helps preserve decisions, preferences, architecture rules, and implementation patterns across sessions.

## 2. Memory Principles

- Memory should be structured and easy to update.
- Memory should distinguish decisions from ideas.
- Memory should reference source documents.
- Memory should avoid storing outdated assumptions.
- Memory should support both human and AI workflows.

## 3. Memory Categories

| Category | Examples |
|---|---|
| Vision | Product purpose, positioning, long-term direction |
| Architecture | Engines, modules, ADR decisions |
| Design | Minimal base system, skins, templates, tokens |
| Development | Coding standards, file structure, naming rules |
| Business | Pricing, licensing, marketplace decisions |
| AI | Prompt rules, coding assistant behaviour |

## 4. Memory File Format

Each memory file should include:

- Purpose
- Current truth
- Source references
- Last reviewed date
- Open questions
- Related documents

## 5. Update Rules

Memory should be updated when:

- A decision is accepted.
- A document changes core rules.
- A repeated preference emerges.
- A deprecated assumption is discovered.

## 6. Acceptance Criteria

- Memory is structured by domain.
- Memory points back to documentation.
- Memory remains current and reviewable.
- AI assistants can use memory without replacing documentation.

## 7. Related Documents

- Document 63 - AI Context Files
- Document 69 - Documentation Standards
- ADR 001 - Component-First Architecture
- ADR 004 - Minimal Base Design System with Skins

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First project memory structure document |
