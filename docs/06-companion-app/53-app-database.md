# Shopify Theme Platform

**Document ID:** 53  
**Document Title:** App Database  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# App Database

## 1. Purpose

This document defines the data model requirements for the Shopify Companion App. The database should support merchant configuration, feature activation, licensing, analytics, recommendations, skins, templates, and sync state.

## 2. Data Principles

- Store only what the app needs to operate.
- Keep merchant configuration versioned.
- Separate operational data from analytics data.
- Preserve auditability for critical changes.
- Avoid storing sensitive data unnecessarily.

## 3. Core Entities

| Entity | Purpose |
|---|---|
| Shop | Represents an installed Shopify store |
| Installation | Tracks app installation and status |
| Plan | Represents subscription or access tier |
| Entitlement | Defines what a shop can access |
| Feature | Defines an optional platform capability |
| Feature State | Tracks enabled or disabled features per shop |
| Skin | Represents a visual design system pack |
| Template Pack | Represents installable template collections |
| Configuration Snapshot | Stores versioned app/theme configuration |
| Recommendation | Stores suggested improvements |
| Analytics Event | Stores usage and adoption signals |

## 4. Configuration Versioning

Configuration should support:

- Draft state
- Published state
- Rollback snapshots
- Migration version
- Timestamped change history

## 5. Analytics Data

Analytics should be structured to answer questions such as:

- Which features are used most?
- Which onboarding steps are skipped?
- Which skins are most popular?
- Which recommendations improve adoption?

## 6. Privacy and Security

The app should:

- Minimise personally identifiable data.
- Respect Shopify app privacy requirements.
- Protect access tokens and sensitive records.
- Provide deletion workflows when stores uninstall.

## 7. Acceptance Criteria

- Core entities are identified.
- Configuration supports versioning.
- Analytics and operational records are separated conceptually.
- Security and privacy requirements are documented.

## 8. Related Documents

- Document 52 - App Architecture
- Document 56 - Analytics Engine
- Document 58 - Cloud Synchronisation
- Document 60 - App API

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First app database document |
