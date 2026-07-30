# Shopify Theme Framework

**Document ID:** 17  
**Document Title:** Onboarding Engine  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Onboarding Engine

## 1. Purpose

This document defines the Onboarding Engine for the Shopify Theme Framework.

The Onboarding Engine guides merchants through the first setup experience and converts their answers into a practical initial configuration for the theme, including experience level, business type, design direction, skins, templates, presets, layout choices, and enabled features.

Its purpose is to make the framework approachable for beginners while still supporting advanced merchants, designers, developers, and agencies.

---

## 2. Onboarding Vision

The framework should not drop merchants into a complex theme editor with dozens of settings and no guidance.

Instead, merchants should be guided through a simple setup flow that helps them start with confidence.

The guiding principle is:

```text
Ask only what matters. Configure the rest intelligently.
```

---

## 3. Core Responsibilities

The Onboarding Engine is responsible for:

- First-time setup guidance
- Merchant experience level selection
- Business stage identification
- Store type identification
- Design starting point selection
- Skin recommendation
- Template pack recommendation
- Feature recommendation
- Initial settings generation
- Setup checklist creation
- Progressive next-step guidance
- Handoff to Theme Editor or companion app dashboard

---

## 4. Onboarding Scope

The onboarding system may exist across both the theme and the companion app.

The theme may support a simplified onboarding experience through theme settings and presets.

The companion app should support the complete onboarding wizard, recommendations, configuration generation, saved setup state, and future AI-assisted guidance.

---

## 5. User Inputs

The onboarding flow should collect only the most useful information.

Recommended inputs:

- Experience level
- Store type
- Business stage
- Catalogue size
- Design preference
- Store goal
- Required features
- Brand readiness
- Technical comfort level

The onboarding flow should avoid asking questions that do not affect the initial setup.

---

## 6. Experience Levels

Supported experience levels:

| Level | Description |
| --- | --- |
| Basic | For beginners who want simple defaults and guidance. |
| Standard | For merchants comfortable with normal theme controls. |
| Advanced | For users who want deeper layout, design, and feature control. |
| Designer | For users focused on visual precision and brand experience. |
| Developer | For technical users who need hooks, debug options, and deeper configuration. |

The selected level should influence visible settings, recommended features, setup complexity, and companion app guidance.

---

## 7. Business Stages

Recommended business stages:

- Launch
- Growth
- Scale
- Enterprise

### Launch

Focus:

- Simple setup
- Essential components
- Fast store launch
- Minimal features

### Growth

Focus:

- Marketing features
- Better conversion tools
- Stronger product presentation
- Improved navigation

### Scale

Focus:

- Advanced templates
- Performance control
- Larger catalogues
- More refined design system

### Enterprise

Focus:

- Advanced integrations
- Custom workflows
- Multi-team needs
- Agency or developer control

---

## 8. Store Types

Initial store types may include:

- Fashion
- Beauty
- Health and Wellness
- Electronics
- Home and Lifestyle
- Food and Beverage
- B2B Catalogue
- Single Product
- Digital Product
- General Store

Store type should influence recommended templates, components, skins, and features.

---

## 9. Design Starting Points

The onboarding flow should allow merchants to choose a design direction without forcing deep design decisions.

Recommended options:

- Minimal Base
- Clean Commerce
- Premium Brand
- Conversion Focused
- Editorial
- Industry Template

These choices should map to skins, design tokens, presets, and template packs.

---

## 10. Store Goals

Merchant goals help the system recommend features.

Examples:

- Launch quickly
- Improve conversion
- Build a premium brand
- Grow email list
- Sell a single product
- Manage a large catalogue
- Build trust
- Improve mobile experience

A merchant may select more than one goal.

---

## 11. Onboarding Output

The Onboarding Engine should generate an initial configuration.

Example output:

```text
Experience Level: Basic
Business Stage: Launch
Store Type: Fashion
Design Starting Point: Minimal Base
Recommended Skin: Mono Minimal
Recommended Template Pack: Fashion Starter
Enabled Features:
  - Header
  - Footer
  - Hero
  - Featured Collection
  - Product Cards
  - Newsletter
Disabled Advanced Features:
  - Mega Menu
  - Quick View
  - Advanced Animations
```

---

## 12. Configuration Mapping

Onboarding answers should map to framework systems.

| Input | Output System |
| --- | --- |
| Experience level | Progressive settings visibility |
| Business stage | Feature recommendations and complexity defaults |
| Store type | Template pack and component recommendations |
| Design preference | Skin and token defaults |
| Store goals | Feature recommendations |
| Catalogue size | Navigation, collection, and filter recommendations |
| Technical comfort | Advanced controls visibility |

---

## 13. Theme Editor Handoff

After onboarding, the merchant should be handed to the correct next step.

Possible handoff destinations:

- Theme Editor homepage setup
- Active template page
- Feature Manager dashboard
- Skin selection screen
- Setup checklist
- Documentation guide

The handoff should reduce confusion by showing the next best action.

---

## 14. Companion App Handoff

The companion app should provide the richer onboarding experience.

The app may support:

- Step-by-step setup wizard
- Saved onboarding state
- Smart recommendations
- Configuration preview
- One-click apply
- Setup checklist
- Progress tracking
- Rollback and reset options

The app should make onboarding feel like guided setup rather than manual configuration.

---

## 15. Setup Checklist

The onboarding flow should create a setup checklist.

Example checklist:

- Add logo
- Set brand colours
- Select homepage template
- Add hero content
- Configure product cards
- Enable newsletter
- Review mobile layout
- Publish theme

Checklist items should reflect the merchant's selected stage, store type, and goals.

---

## 16. Recommendation Logic

The first version can use rule-based recommendations.

Example rules:

- If catalogue size is large, recommend collection filters.
- If business stage is launch, keep advanced features disabled.
- If goal is build trust, recommend testimonials, reviews, and trust badges.
- If design preference is premium brand, recommend a premium skin.
- If experience level is developer, expose advanced settings.

Future versions may use AI-assisted recommendations.

---

## 17. Progressive Onboarding

Onboarding should not happen only once.

The framework should support progressive onboarding as the merchant grows.

Examples:

- After launch, recommend growth features.
- After enabling product reviews, recommend testimonials.
- After adding many products, recommend filters.
- After using basic mode for a while, suggest standard controls.
- After performance impact increases, suggest optimisation steps.

---

## 18. User Experience Rules

Onboarding should follow these UX rules:

- Ask one clear thing at a time.
- Avoid technical language for beginners.
- Explain why a recommendation is made.
- Keep choices reversible.
- Do not force advanced features.
- Show progress.
- Provide defaults.
- Avoid overwhelming the merchant.

---

## 19. Data and State

Onboarding state may include:

- Completion status
- Selected experience level
- Store profile
- Selected goals
- Recommended features
- Applied configuration
- Skipped steps
- Setup checklist progress
- Last onboarding update

The storage strategy may use theme settings, metafields, app database records, or a hybrid model.

---

## 20. Onboarding and Feature Manager

The Onboarding Engine should work closely with the Feature Manager.

Onboarding recommends features. The Feature Manager stores and manages feature state.

```text
Onboarding Answers
  -> Feature Recommendations
  -> Feature Manager
  -> Enabled and Disabled Features
```

---

## 21. Onboarding and Skins

The Onboarding Engine should recommend skins based on merchant preferences.

Examples:

- Minimal Base for beginners and clean stores.
- Premium Brand for luxury or high-end stores.
- Clean Commerce for general stores.
- Conversion Focused for landing pages and product launches.

Applying a skin should preserve merchant content.

---

## 22. Onboarding and Templates

The Onboarding Engine should recommend template packs based on store type and goal.

Examples:

- Fashion Starter
- Beauty Brand Launch
- Single Product Store
- B2B Catalogue
- Digital Product Store
- Conversion Landing Page

Template pack application should be clear and reversible where possible.

---

## 23. Onboarding and Design Tokens

Onboarding may set basic token values.

Examples:

- Brand colour
- Font style
- Button style
- Spacing density
- Visual mood

Advanced token control should remain outside beginner onboarding.

---

## 24. Onboarding and AI

Future AI-assisted onboarding may support:

- Store analysis
- Brand style suggestions
- Recommended homepage structure
- Suggested product page improvements
- Copy suggestions
- Feature recommendations
- Performance guidance

AI suggestions should be explainable and optional.

---

## 25. Failure and Recovery

The onboarding system should handle incomplete or failed setup safely.

Requirements:

- Save progress.
- Allow skipping steps.
- Allow restarting onboarding.
- Allow resetting recommendations.
- Preserve merchant content.
- Avoid applying destructive changes without confirmation.

---

## 26. MVP Scope

The first version should support:

- Experience level selection
- Store type selection
- Business stage selection
- Design starting point selection
- Basic feature recommendations
- Basic skin recommendation
- Basic template recommendation
- Setup checklist
- Theme Editor or companion app handoff

AI onboarding, advanced analytics, and deep configuration previews can be added later.

---

## 27. Future Enhancements

Future capabilities may include:

- AI setup assistant
- Store audit-based recommendations
- Industry-specific onboarding flows
- Agency onboarding profiles
- Multi-store onboarding templates
- Setup progress analytics
- Automated performance guidance
- Saved onboarding profiles
- One-click advanced mode migration

---

## 28. Acceptance Criteria

The Onboarding Engine will be considered successful when:

- Beginners can start without confusion.
- Merchants receive useful defaults.
- Onboarding outputs valid theme configuration.
- Recommendations map to skins, templates, features, and settings.
- The merchant can skip, restart, or revise onboarding choices.
- The theme remains usable without the companion app.
- The companion app can provide a richer guided setup experience.
- Progressive onboarding supports merchant growth over time.

---

## 29. Open Questions

- Which onboarding steps can be implemented inside Shopify Theme Editor?
- Which onboarding steps require the companion app?
- Should onboarding be mandatory or optional?
- How much onboarding state should be stored in the theme versus the app?
- Should the first release include rule-based recommendations only?
- Should merchants be able to save onboarding profiles for future stores?

---

## 30. Related Documents

- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
- Document 15 - Theme Settings Architecture
- Document 16 - Feature Manager Architecture
- Document 18 - Performance Engine
- ADR 002 - Use Theme plus Companion App Architecture
- ADR 003 - Adopt Progressive Disclosure for Merchant UX

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Onboarding Engine document |
