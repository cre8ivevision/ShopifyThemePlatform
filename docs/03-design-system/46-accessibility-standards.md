# Shopify Theme Platform

**Document ID:** 46  
**Document Title:** Accessibility Standards  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Accessibility Standards

## 1. Purpose

This document defines accessibility standards for the Shopify Theme Platform. Accessibility must be treated as a core product requirement, not a final-stage fix.

## 2. Scope

This document covers visual accessibility, keyboard navigation, semantic structure, focus states, forms, commerce interactions, media, and theme editor considerations.

## 3. Accessibility Principles

- Accessibility should be built into components by default.
- Merchant customisation should not easily break core accessibility.
- Skins must preserve contrast, readability, and interaction clarity.
- Components should use semantic HTML where possible.
- Keyboard and screen reader users must be supported.

## 4. Visual Accessibility

The platform should define requirements for:

- Text contrast
- Button contrast
- Focus indicators
- Error states
- Hover and active states
- Disabled states
- Sale and discount labels

Colour tokens should include accessible defaults.

## 5. Semantic Structure

Components should use appropriate semantic elements:

- Headings for document structure
- Buttons for actions
- Links for navigation
- Lists for grouped items
- Forms for data collection
- Landmarks for major page regions

## 6. Keyboard Navigation

Interactive components must support keyboard access.

Examples:

- Menus
- Drawers
- Modals
- Accordions
- Tabs
- Sliders
- Product media galleries
- Variant selectors

## 7. Focus Management

Focus should be visible and predictable.

Requirements:

- Modals trap focus while open.
- Drawers return focus after closing.
- Skip links are supported.
- Focus states are not removed.
- Hidden elements are not reachable by keyboard.

## 8. Forms and Errors

Forms must provide:

- Labels
- Helpful validation messages
- Error summaries where appropriate
- Clear required field handling
- Keyboard-friendly inputs

## 9. Media Accessibility

Media patterns should support:

- Alt text for meaningful images
- Empty alt text for decorative images
- Captions or transcripts for video where applicable
- Pause controls for motion-heavy content

## 10. Theme Editor Protection

The platform should guide merchants away from inaccessible choices.

Examples:

- Warn when contrast is poor.
- Preserve focus styling in skins.
- Provide accessible defaults for presets.
- Avoid hiding critical labels by default.

## 11. Acceptance Criteria

- Components include accessibility requirements.
- Skins preserve accessible defaults.
- Interactive patterns support keyboard use.
- Forms expose labels and useful errors.
- Accessibility testing is part of QA.

## 12. Related Documents

- Document 40 - Testing Guidelines
- Document 42 - Colour System
- Document 45 - Responsive Behaviour
- Document 84 - Performance Benchmarks

---

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | July 30, 2026 | Initial Draft | First accessibility standards document |
