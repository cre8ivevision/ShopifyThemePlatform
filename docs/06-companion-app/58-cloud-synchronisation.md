# Shopify Theme Platform

**Document ID:** 58  
**Document Title:** Cloud Synchronisation  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Cloud Synchronisation

## 1. Purpose

This document defines how the Companion App synchronises cloud-backed configuration with the Shopify theme. Synchronisation should be reliable, versioned, recoverable, and safe for live storefronts.

## 2. Sync Goals

- Keep app and theme configuration aligned.
- Support recoverable configuration changes.
- Enable app-managed features without making the storefront fragile.
- Track sync status clearly for merchants and support teams.

## 3. Sync Data

Sync may include:

- Feature state
- Skin selection
- Template pack status
- Design presets
- Recommendation state
- Licensing state
- Configuration snapshots

## 4. Sync States

| State | Meaning |
|---|---|
| Synced | App and theme are aligned |
| Pending | Changes are waiting to be applied |
| Failed | Sync attempt failed |
| Conflict | App and theme have conflicting changes |
| Recovering | System is restoring a known good state |

## 5. Versioning

Every synced configuration should include:

- Configuration version
- Theme compatibility version
- App version
- Timestamp
- Source of change

## 6. Conflict Handling

When conflicts occur, the app should:

- Avoid silent overwrites.
- Show clear conflict messaging.
- Offer restore or keep-current options.
- Preserve latest known safe configuration.

## 7. Storefront Safety

The storefront should use the last valid published configuration if cloud sync fails.

## 8. Acceptance Criteria

- Sync states are defined.
- Configuration is versioned.
- Failed sync does not break storefront rendering.
- Conflict handling is merchant-safe.

## 9. Related Documents

- Document 52 - App Architecture
- Document 53 - App Database
- Document 54 - Feature Activation System
- Document 60 - App API

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First cloud synchronisation document |
