# Shopify Theme Platform

**Document ID:** 86  
**Document Title:** Security Checklist  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Security Checklist

## 1. Purpose

This document defines security checklist requirements for the Shopify Theme Platform and Companion App. Security should protect merchants, shoppers, storefront integrity, and platform trust.

## 2. Security Principles

- Follow Shopify platform security expectations.
- Avoid unsafe script patterns.
- Sanitize and escape output appropriately.
- Protect app credentials and tokens.
- Minimise data collection and storage.
- Treat third-party integrations carefully.

## 3. Theme Security Checklist

- Liquid output is escaped where needed.
- User-generated content is handled safely.
- External scripts are minimised and reviewed.
- Theme settings do not allow unsafe injection.
- App blocks follow Shopify guidance.
- Forms use appropriate validation.

## 4. App Security Checklist

- Shopify authentication is implemented correctly.
- Access tokens are stored securely.
- API routes enforce authorization.
- Webhooks are verified.
- Sensitive data is minimised.
- Uninstall data handling is documented.

## 5. Release Security Review

Before release, review:

- New dependencies
- New scripts
- New API endpoints
- New data storage
- New app permissions
- Third-party integrations

## 6. Acceptance Criteria

- Theme and app security areas are covered.
- Release security review is documented.
- Shopify security expectations are acknowledged.
- Sensitive data handling is considered.

## 7. Related Documents

- Document 52 - App Architecture
- Document 60 - App API
- Document 81 - QA Standards
- Document 87 - Release Checklist

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First security checklist document |
