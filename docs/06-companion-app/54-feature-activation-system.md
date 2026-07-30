# Shopify Theme Platform

**Document ID:** 54  
**Document Title:** Feature Activation System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Feature Activation System

## 1. Purpose

This document defines how optional platform features are enabled, disabled, grouped, recommended, and synchronised between the Companion App and Shopify theme.

## 2. Goals

- Keep the default merchant experience simple.
- Allow advanced features to be enabled progressively.
- Prevent unnecessary CSS and JavaScript loading.
- Support plan-based entitlements.
- Make feature dependencies clear.

## 3. Feature Types

| Type | Example |
|---|---|
| Core | Basic sections and settings |
| Optional | Advanced filters, quick add, popups |
| Premium | Premium skins, analytics, AI recommendations |
| Experimental | Beta or early access modules |
| App-backed | Features requiring cloud services |

## 4. Activation Rules

A feature may require:

- Plan entitlement
- Dependency features
- Theme compatibility
- App installation
- Merchant confirmation
- Migration step

## 5. Merchant Experience

The Feature Manager should show:

- Enabled features
- Available features
- Locked features
- Recommended features
- Feature impact on performance
- Dependencies and warnings

## 6. Theme Sync

Only enabled features should expose their relevant theme settings, assets, and behaviours where technically possible.

The theme should have safe fallbacks if the app cannot be reached.

## 7. Acceptance Criteria

- Feature activation is entitlement-aware.
- Dependencies are documented.
- Disabled features do not create unnecessary complexity.
- Merchant controls remain understandable.
- Theme sync behaviour is defined.

## 8. Related Documents

- Document 16 - Feature Manager Architecture
- Document 51 - App PRD
- Document 55 - Licensing
- Document 58 - Cloud Synchronisation

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First feature activation system document |
