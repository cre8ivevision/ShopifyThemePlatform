# Shopify Theme Framework

**Document ID:** 06  
**Document Title:** Theme Editor UX Specification  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Theme Editor UX Specification

## 1. Purpose

This document defines the user experience strategy for the Shopify Theme Framework inside the Shopify Theme Editor.

The Theme Editor experience is one of the most important parts of the product. The framework must help beginners build confidently while giving advanced users, designers, developers, and agencies enough control to create sophisticated storefronts without changing themes.

This document defines how settings, components, layouts, skins, templates, presets, onboarding, and progressive controls should be exposed to merchants.

---

## 2. UX Vision

The Shopify Theme Framework should make powerful theme customisation feel simple.

The user should not feel that they are configuring a complex technical system. They should feel guided, confident, and in control.

The Theme Editor UX should follow this principle:

```text
Simple first. Powerful when needed.
```

A beginner should be able to launch a clean store with minimal decisions. A professional user should be able to unlock deeper layout, component, design, and behaviour controls without needing to switch themes.

---

## 3. Core UX Principles

### Clarity Before Control

Controls should be easy to understand before they are powerful.

### Progressive Disclosure

Only relevant settings should be shown at the right time.

### Guided Decision-Making

The framework should help merchants choose settings instead of forcing them to understand every option.

### Familiar Mental Models

The editor should feel familiar to users coming from tools such as Elementor, Webflow, Wix, Squarespace, or modern Shopify themes, while remaining original and Shopify-native.

### Safe Customisation

Users should be able to experiment without breaking the store layout.

### Performance Awareness

The editor should help users understand when enabled features may affect storefront performance.

### Reversible Choices

Major design and feature choices should be easy to change later.

---

## 4. Target User Levels

The Theme Editor UX should support multiple experience levels.

| Level | User Type | Editor Experience |
| --- | --- | --- |
| 1 | Beginner | Guided setup, minimal controls, recommended defaults |
| 2 | Standard Merchant | Common layout and design controls |
| 3 | Growth Merchant | Marketing, conversion, and feature controls |
| 4 | Designer | Advanced visual and layout controls |
| 5 | Developer | Technical controls, hooks, debug options |

The user should be able to change their level later.

---

## 5. First-Time Onboarding Flow

When the theme is installed, the user should be guided through a simple setup flow.

Recommended onboarding steps:

1. Select experience level
2. Select store type
3. Select business stage
4. Select design starting point
5. Select required features
6. Confirm initial setup

### Experience Level

Options:

- Basic
- Standard
- Advanced
- Designer
- Developer

### Store Type

Examples:

- Fashion
- Beauty
- Health
- Electronics
- Home and Lifestyle
- B2B
- Single Product
- Digital Product
- General Store

### Business Stage

Options:

- Launch
- Growth
- Scale
- Enterprise

### Design Starting Point

Options:

- Minimal Base
- Clean Commerce
- Premium Brand
- Conversion Focused
- Industry Template

### Required Features

Examples:

- Announcement bar
- Header navigation
- Product recommendations
- Collection filters
- Newsletter
- Reviews
- Trust badges
- FAQ
- Cart drawer
- Promotional banners

---

## 6. Default Experience

The default experience should be minimal and beginner-friendly.

By default, the user should see:

- Essential settings only
- Clean section presets
- Minimal design controls
- Basic layout choices
- Recommended defaults
- Clear labels
- No technical terminology unless necessary

The default theme should not expose every advanced feature immediately.

---

## 7. Progressive Control System

The editor should reveal controls based on context and user level.

```text
Basic Controls
  -> Standard Controls
  -> Advanced Controls
  -> Designer Controls
  -> Developer Controls
```

### Basic Controls

- Content
- Images
- Buttons
- Simple alignment
- Section visibility
- Preset selection

### Standard Controls

- Container width
- Spacing scale
- Layout variants
- Basic colours
- Typography style
- Mobile behaviour

### Advanced Controls

- Token overrides
- Section-level design rules
- Responsive settings
- Animation controls
- Conditional visibility
- Conversion options

### Designer Controls

- Detailed spacing
- Custom typography scales
- Skin tuning
- Visual density
- Component styling behaviour
- Section mood presets

### Developer Controls

- Custom CSS classes
- Data attributes
- Debug information
- Integration hooks
- Experimental options

---

## 8. Settings Information Architecture

Settings should be grouped consistently across all sections and components.

Recommended structure:

```text
Content
Layout
Design
Behaviour
Features
Responsive
Advanced
```

### Content

Text, media, buttons, links, products, collections, and block content.

### Layout

Structure, alignment, columns, grid, flex behaviour, container width, and ordering.

### Design

Colours, typography, spacing, radius, shadows, and skin-related options.

### Behaviour

Animations, interactions, visibility, sticky behaviour, collapsible behaviour, and timing.

### Features

Optional component capabilities such as countdowns, badges, trust elements, dynamic content, or promotional controls.

### Responsive

Mobile, tablet, desktop, and large screen behaviour.

### Advanced

Developer-facing and technical settings.

---

## 9. Layout Selection UX

Layout selection should be visual and understandable.

Instead of exposing only technical names, the editor should present layout options as human-readable presets.

Examples:

| Technical System | User-Facing Label |
| --- | --- |
| CSS Grid | Grid Layout |
| Flexbox | Flexible Row |
| Columns | Column Layout |
| Full Width | Edge-to-Edge |
| Boxed | Contained Layout |
| Split | Image + Content Split |

Where possible, layout presets should include small previews or descriptive names.

---

## 10. Familiar Workflow Modes

The framework may support familiar workflow modes without copying external platforms.

Possible workflow modes:

- Simple Builder Mode
- Flex Layout Mode
- Grid Layout Mode
- Designer Mode
- Developer Mode

These modes should map to the same internal architecture.

```text
Workflow Mode
  -> Layout Engine
  -> Component Settings
  -> Design Tokens
```

The workflow mode changes the editing experience, not the underlying component system.

---

## 11. Skins and Templates UX

Skins and templates should be presented as upgrade paths, not as technical configuration.

### Skin Selection

The user should be able to choose a skin from a simple visual list.

Skin cards may include:

- Skin name
- Visual preview
- Best use case
- Complexity level
- Included styling features
- Performance impact indicator

### Template Pack Selection

Template packs should be grouped by business type and goal.

Examples:

- Launch a Fashion Store
- Build a Single Product Store
- Create a Premium Beauty Brand
- Build a B2B Catalogue
- Create a Conversion-Focused Landing Page

### Key Rule

Applying a skin or template should not destroy existing merchant content.

The system should preserve content wherever possible and only change structure or visual configuration when confirmed.

---

## 12. Feature Manager UX

The Feature Manager should allow users to enable or disable optional capabilities.

It should answer three questions clearly:

1. What does this feature do?
2. When should I use it?
3. Will it affect performance or complexity?

Each feature should show:

- Name
- Description
- Recommended for
- Complexity level
- Performance impact
- Dependencies
- Enable or disable control

Feature categories:

- Storefront structure
- Product experience
- Collection experience
- Marketing
- Conversion
- Trust and credibility
- Navigation
- Search and discovery
- Advanced behaviour

---

## 13. Component Editor UX

Each component should feel consistent in the editor.

Recommended component editor structure:

```text
Quick Setup
Content
Layout
Blocks
Design
Behaviour
Responsive
Advanced
```

### Quick Setup

A compact starting point with presets and recommended defaults.

### Blocks

Blocks should be easy to add, remove, reorder, and configure.

### Design

Design settings should use simple labels and token-driven controls.

### Advanced

Advanced options should remain collapsed by default unless the user level requires them.

---

## 14. Preset UX

Presets should reduce decision fatigue.

A user should be able to add a component and choose from recommended presets instead of manually building everything from scratch.

Preset information should include:

- Preset name
- Use case
- Included blocks
- Recommended skin compatibility
- Complexity level

Examples:

- Minimal Hero
- Product Launch Hero
- Trust-Focused Product Section
- Editorial Image with Text
- Campaign Banner
- FAQ for Product Objections

---

## 15. Error Prevention

The Theme Editor UX should prevent common merchant mistakes.

Examples:

- Warn when contrast is too low.
- Warn when too many animations are enabled.
- Warn when a section has missing content.
- Warn when a layout may not work well on mobile.
- Warn when heavy media may affect performance.
- Suggest simpler settings when the user appears overwhelmed.

Warnings should be helpful, not aggressive.

---

## 16. Empty States

Every section and component should include helpful empty states.

Empty states should explain:

- What the component is for
- What content is needed
- What preset can be used
- What the next best action is

Empty states should be short and practical.

---

## 17. Performance UX

The editor should make performance understandable.

Potential indicators:

- Lightweight
- Moderate
- Heavy

Examples:

- A simple text section is Lightweight.
- A carousel may be Moderate.
- A video background may be Heavy.

The user should not need to understand technical performance details to make better decisions.

---

## 18. Mobile-First Editing

The Theme Editor UX should encourage mobile-first thinking.

Requirements:

- Mobile preview should be easy to access.
- Mobile spacing should be configurable where necessary.
- Mobile layout warnings should be provided.
- Components should include mobile-safe defaults.

---

## 19. Accessibility UX

Accessibility should be built into the editor experience.

Possible checks:

- Contrast warnings
- Missing alt text warnings
- Link text guidance
- Focus state preservation
- Reduced motion support
- Heading hierarchy suggestions

Accessibility should be presented as quality guidance, not as a burden.

---

## 20. Companion App Relationship

Some UX features may be better handled through the companion app rather than the Shopify Theme Editor alone.

The Theme Editor should handle:

- Section configuration
- Component settings
- Layout choices
- Skin selection, where possible
- Basic feature controls

The Companion App may handle:

- Full onboarding wizard
- Feature Manager dashboard
- Skin and template library
- Recommendations
- Usage analytics
- Licensing
- Cloud configuration
- Advanced setup guidance

The theme should remain useful even if the companion app is not installed.

---

## 21. UX Success Metrics

The Theme Editor UX should be measured by:

- Faster setup time
- Higher onboarding completion
- Lower support requests
- Fewer abandoned configurations
- Higher use of presets
- Higher use of mobile preview
- Lower theme switching
- Higher merchant satisfaction
- Better performance outcomes

---

## 22. Acceptance Criteria

The Theme Editor UX will be considered successful when:

- Beginner users can launch without feeling overwhelmed.
- Advanced users can access deeper controls without needing custom code.
- Users can move from minimal design to advanced design through skins and templates.
- Settings are grouped consistently across components.
- Layout choices are easy to understand.
- Feature activation is clear and reversible.
- The editor prevents common mistakes.
- Performance and accessibility guidance are included in the experience.
- The companion app enhances the experience without making the theme dependent on it.

---

## 23. Open Questions

- Which onboarding steps can be implemented directly inside Shopify Theme Editor?
- Which onboarding steps require the companion app?
- Should workflow mode be selected during onboarding or inside theme settings?
- Should users be able to switch between Basic, Advanced, Designer, and Developer levels at any time?
- How visual can skin and template previews be inside Shopify Theme Editor?
- Should performance indicators be shown in the theme editor, companion app, or both?
- Should beginner mode hide advanced settings completely or collapse them under an upgrade/control section?

---

## 24. Related Documents

- Document 01 - Vision & Product Strategy
- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 07 - Companion App Architecture
- Document 09 - Design Tokens Specification
- Document 16 - Feature Manager Architecture
- Document 17 - Onboarding Engine

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Theme Editor UX Specification document |
