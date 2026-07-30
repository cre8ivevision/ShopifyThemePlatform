# Shopify Theme Platform

**Document ID:** 98  
**Document Title:** Multi-Tenant Architecture  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Multi-Tenant Architecture

## 1. Purpose

This document defines the long-term multi-tenant architecture direction for cloud and app-backed parts of the Shopify Theme Platform. Multi-tenancy should support many merchants, stores, agencies, and enterprise accounts safely.

## 2. Multi-Tenant Principles

- Tenant data must be isolated.
- Access control must be explicit.
- Configuration should be scoped correctly.
- Shared infrastructure should remain secure and observable.
- Enterprise accounts may manage multiple shops.

## 3. Tenant Types

| Tenant Type | Description |
|---|---|
| Shop Tenant | A single Shopify store installation |
| Merchant Tenant | A merchant account managing one or more shops |
| Agency Tenant | An agency managing client stores |
| Enterprise Tenant | A larger organisation with teams and governance |

## 4. Data Isolation

The system should isolate:

- Shop configuration
- Licensing state
- Analytics data
- Team access
- Marketplace purchases
- Recommendation history

## 5. Access Control

Access control should support:

- Owner roles
- Admin roles
- Editor roles
- Viewer roles
- Agency roles
- Support roles

## 6. Acceptance Criteria

- Tenant types are defined.
- Data isolation requirements are documented.
- Access control needs are identified.
- Multi-tenancy aligns with enterprise features and cloud services.

## 7. Related Documents

- Document 52 - App Architecture
- Document 53 - App Database
- Document 94 - Cloud Services
- Document 97 - Enterprise Features

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First multi-tenant architecture document |
