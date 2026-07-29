# Shopify Theme Framework

**Document ID:** 07  
**Document Title:** Companion App Architecture  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Companion App Architecture

## 1. Purpose

This document defines the architecture and strategic role of the optional Shopify companion app for the Shopify Theme Framework.

The companion app is not intended to replace the theme. Its purpose is to extend the theme with capabilities that are difficult, limited, or unsuitable to handle entirely inside Shopify Theme Editor.

The guiding principle is:

```text
The theme should work independently. The app should make it smarter, easier, and more scalable.
```

---

## 2. Companion App Vision

The Shopify Theme Framework should be usable as a standalone theme, but its full long-term potential should be unlocked through a companion app.

The companion app should provide a richer control layer for onboarding, feature management, design upgrades, templates, analytics, licensing, recommendations, and future AI-assisted workflows.

This allows the theme to remain lightweight and performance-focused while still supporting advanced platform-level functionality.

---

## 3. Core Principles

### Theme Independence

The storefront must continue working even if the companion app is not installed, unavailable, or disconnected.

### App as Control Layer

The app should manage configuration, guidance, feature discovery, and advanced workflows. It should not directly own core storefront rendering.

### Performance Protection

The app should help merchants enable powerful features without making the theme unnecessarily heavy.

### Progressive Enhancement

The app should enhance the merchant experience gradually, based on business stage, experience level, and selected features.

### Reversible Configuration

Changes applied by the app should be traceable and reversible wherever possible.

---

## 4. Theme vs App Responsibility Boundary

| Responsibility | Theme | Companion App |
| --- | --- | --- |
| Storefront rendering | Yes | No |
| Core sections and blocks | Yes | No |
| Basic theme settings | Yes | Limited |
| Basic skin support | Yes | Yes |
| Full onboarding wizard | Limited | Yes |
| Feature Manager dashboard | Limited | Yes |
| Skin and template library | Limited | Yes |
| Licensing | No | Yes |
| Usage analytics | Limited | Yes |
| AI recommendations | No | Yes |
| Cloud configuration | No | Yes |
| Remote update guidance | No | Yes |
| Merchant education | Limited | Yes |

The theme should contain the rendering system. The app should contain the intelligence and management system.

---

## 5. Primary App Modules

The companion app should be organised into clear modules.

```text
Companion App
  -> Onboarding Wizard
  -> Feature Manager
  -> Skin Library
  -> Template Library
  -> Preset Manager
  -> Merchant Dashboard
  -> Analytics Engine
  -> Recommendation Engine
  -> Licensing System
  -> Configuration Sync
  -> Support and Education
```

Each module should be independently maintainable.

---

## 6. Onboarding Wizard

The onboarding wizard should guide merchants through initial setup more effectively than the Shopify Theme Editor alone.

Recommended onboarding steps:

1. Store profile
2. Merchant experience level
3. Business stage
4. Industry or store type
5. Design starting point
6. Required features
7. Recommended skin
8. Recommended template pack
9. Initial setup summary
10. Apply configuration

The app should generate a recommended configuration that can be applied to the theme.

---

## 7. Feature Manager

The Feature Manager allows merchants to enable or disable optional capabilities.

Each feature should include:

- Name
- Description
- Business use case
- Recommended user level
- Dependencies
- Performance impact
- Complexity level
- Status
- Enable or disable action

Feature categories may include:

- Storefront structure
- Navigation
- Product experience
- Collection experience
- Marketing
- Conversion
- Trust and credibility
- Search and discovery
- Advanced behaviour
- Integrations

---

## 8. Skin Library

The Skin Library should allow merchants to browse and apply visual skins.

A skin may define:

- Colour palette
- Typography pairing
- Spacing rhythm
- Radius system
- Shadow style
- Button styling
- Card styling
- Animation style
- Component visual defaults

Skin cards should show:

- Preview image
- Skin name
- Best use case
- Complexity level
- Included design traits
- Performance impact
- Compatibility notes

Applying a skin should preserve merchant content wherever possible.

---

## 9. Template Library

The Template Library should provide page-level and industry-specific starting points.

Template packs may include:

- Homepage templates
- Product page templates
- Collection page templates
- Landing page templates
- Campaign templates
- Industry starter packs

Template packs should combine:

- Components
- Blocks
- Layout variants
- Presets
- Skin recommendations
- Page structure

---

## 10. Preset Manager

The Preset Manager should allow merchants to manage reusable configurations.

Possible capabilities:

- Save section presets
- Save component presets
- Save page presets
- Import presets
- Export presets
- Duplicate presets
- Reset presets
- Share presets across stores, future

This feature is especially useful for agencies and advanced merchants.

---

## 11. Merchant Dashboard

The Merchant Dashboard should provide a clear overview of the current theme setup.

Recommended dashboard cards:

- Active skin
- Active template pack
- Enabled features
- Disabled recommended features
- Performance status
- Setup completion
- Recommended next actions
- Documentation shortcuts
- Support shortcuts

The dashboard should help merchants understand where they are and what to do next.

---

## 12. Analytics Engine

The app may collect and display usage analytics related to the theme configuration.

Potential analytics:

- Enabled features
- Most-used components
- Unused features
- Setup progress
- Performance-impacting features
- Skin usage
- Template usage
- Merchant experience level

Analytics should be used to improve recommendations and product decisions.

Privacy and Shopify policy compliance must be considered before implementation.

---

## 13. Recommendation Engine

The Recommendation Engine should provide contextual suggestions.

Examples:

- Recommend enabling product recommendations for larger catalogues.
- Recommend simplifying layouts when too many heavy sections are active.
- Recommend a premium skin when the merchant wants a stronger brand identity.
- Recommend a template pack based on industry.
- Recommend mobile improvements when a section has risky settings.

Recommendations should be optional, explainable, and easy to dismiss.

---

## 14. Licensing System

The companion app may manage access to premium capabilities.

Possible licensed items:

- Premium skins
- Premium template packs
- Advanced component packs
- AI recommendations
- Agency features
- Preset import/export
- Advanced analytics
- Priority support

Licensing should not break the basic theme experience.

The base theme should remain functional even if premium features are unavailable.

---

## 15. Configuration Sync

The companion app must communicate configuration changes to the theme safely.

Possible configuration areas:

- Active skin
- Enabled features
- Template pack settings
- Preset data
- Merchant experience level
- Store profile
- Recommended settings

Configuration sync should be:

- Predictable
- Versioned
- Reversible where possible
- Compatible with theme updates
- Safe for existing merchant content

---

## 16. Data Model Overview

Initial app data entities may include:

- Store
- Merchant Profile
- Theme Installation
- Feature
- Feature Group
- Skin
- Template Pack
- Preset
- Recommendation
- License
- Usage Event
- Configuration Snapshot

Detailed database schema will be defined in a separate app database document.

---

## 17. App and Theme Communication

Communication should be designed carefully because the storefront rendering belongs to the theme.

Possible communication methods:

- Theme settings updates
- Metaobjects or metafields, where appropriate
- App embeds
- Theme app extensions
- Admin API configuration workflows
- Script or asset injection only when necessary and compliant

The preferred approach should minimise storefront dependency on remote app availability.

---

## 18. Failure Behaviour

The theme should fail gracefully if the companion app is unavailable.

Required behaviours:

- Storefront remains functional.
- Existing configuration remains active.
- Premium visual settings do not break rendering.
- Disabled app-dependent features show safe fallbacks.
- Merchant receives clear guidance inside the app when reconnected.

---

## 19. Security and Compliance

The companion app must follow Shopify security and app development requirements.

Considerations:

- OAuth security
- Secure token handling
- Minimal required permissions
- Data privacy
- Merchant consent
- Webhook validation
- API rate limits
- Billing compliance
- App review requirements

Security details should be expanded in a dedicated security document.

---

## 20. Performance Rules

The companion app must protect storefront performance.

Rules:

- Do not load unnecessary scripts on the storefront.
- Prefer static configuration over runtime remote dependencies.
- Avoid blocking storefront rendering.
- Keep app embeds optional.
- Load app-powered features only when enabled.
- Provide performance impact indicators for heavy features.

---

## 21. MVP Scope

The first version of the companion app should remain focused.

Recommended MVP modules:

- Basic onboarding wizard
- Feature Manager dashboard
- Skin selection
- Template pack selection
- Setup checklist
- Basic recommendations
- Licensing foundation
- Configuration sync foundation

Advanced analytics, AI recommendations, marketplace extensions, and agency workflows can be added later.

---

## 22. Future Capabilities

Future companion app capabilities may include:

- AI store setup assistant
- AI layout recommendations
- AI copy recommendations
- Performance optimisation advisor
- Component marketplace
- Skin marketplace
- Template marketplace
- Agency workspace
- Multi-store management
- Cloud backup and restore
- Team collaboration
- A/B testing guidance

---

## 23. Acceptance Criteria

The companion app architecture will be considered successful when:

- The theme remains functional without the app.
- The app improves onboarding and feature discovery.
- Merchants can enable and disable features confidently.
- Skins and templates can be managed without rebuilding the store.
- Performance impact is visible and controlled.
- Configuration sync is predictable and safe.
- Premium features can be licensed without harming the base experience.
- The app can evolve into a platform control layer over time.

---

## 24. Open Questions

- Which features must be available in the theme without the app?
- Which features should require the app from day one?
- Should skins be bundled in the theme, delivered through the app, or both?
- Should template packs be stored locally, remotely, or as a hybrid system?
- What Shopify permissions will the app require?
- What should be included in the free/base app experience?
- Which premium capabilities should be monetised first?
- How should configuration rollback work?

---

## 25. Related Documents

- Document 01 - Vision & Product Strategy
- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 16 - Feature Manager Architecture
- Document 17 - Onboarding Engine
- Document 51 - App PRD
- Document 52 - App Architecture
- Document 53 - App Database

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Companion App Architecture document |
