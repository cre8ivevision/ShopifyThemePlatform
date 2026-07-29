# Shopify Theme Framework

**Document ID:** 08  
**Document Title:** Development Standards  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Development Standards

## 1. Purpose

This document defines the development standards for the Shopify Theme Framework.

The goal is to ensure that every human developer, AI coding assistant, contributor, and future maintainer follows the same engineering principles when building the theme, companion app, documentation, components, templates, skins, and platform extensions.

These standards protect the long-term maintainability, scalability, performance, accessibility, and consistency of the framework.

---

## 2. Development Philosophy

The Shopify Theme Framework should be developed as a long-term product platform, not as a one-off Shopify theme.

Every implementation decision should support:

- Reusability
- Maintainability
- Performance
- Accessibility
- Scalability
- Predictability
- Documentation quality
- AI-assisted development readiness

The guiding principle is:

```text
Build once. Reuse everywhere. Keep it understandable.
```

---

## 3. Core Engineering Principles

### Component First

Reusable components should be preferred over page-specific or section-specific implementations.

### Clear Boundaries

Layout, content, design, behaviour, configuration, and commerce logic should remain separated wherever possible.

### Minimal Duplication

Duplicate code should be avoided unless duplication is simpler and safer than premature abstraction.

### Performance by Default

Every feature should be designed with performance in mind from the beginning.

### Accessibility by Default

Accessibility should be built into components and patterns from the start.

### Progressive Enhancement

Advanced functionality should enhance the core experience without breaking the basic experience.

### Documentation as Source of Truth

Important systems, components, decisions, and rules should be documented before or alongside implementation.

---

## 4. Repository Standards

The repository should be organised clearly and consistently.

Recommended top-level structure:

```text
shopify-theme-platform/
  README.md
  CHANGELOG.md
  CONTRIBUTING.md
  docs/
  theme/
  app/
  packages/
  examples/
  scripts/
  tests/
  .github/
```

### Repository Rules

- Keep documentation under `docs/`.
- Keep theme source under `theme/` when implementation begins.
- Keep companion app source under `app/` when implementation begins.
- Keep reusable shared logic under `packages/` when needed.
- Keep examples separate from production source.
- Avoid mixing documentation drafts with implementation files.

---

## 5. Documentation Standards

All documentation should be written in official English.

Each major document should include:

- Purpose
- Scope
- Principles
- Requirements
- Acceptance criteria
- Open questions
- Related documents
- Revision history

### Documentation Rules

- Use Markdown.
- Use clear headings.
- Use tables where comparison improves clarity.
- Use code blocks for structures, schemas, and examples.
- Keep each document focused on one subject.
- Link related documents.
- Update revision history for meaningful changes.

---

## 6. Naming Conventions

Names should be predictable and descriptive.

### File Names

Use lowercase kebab-case.

Examples:

```text
hero-banner.liquid
product-card.liquid
feature-manager.md
design-token-specification.md
```

### Component IDs

Use stable lowercase identifiers.

Examples:

```text
hero
product-card
collection-grid
announcement-bar
```

### CSS Classes

Use a consistent framework prefix to avoid conflicts.

Example:

```css
.stp-hero
.stp-product-card
.stp-section
```

### JavaScript Modules

Use clear module names.

Examples:

```text
cart-drawer.js
component-loader.js
feature-manager.js
```

---

## 7. Shopify Theme Standards

The theme should follow Shopify Online Store 2.0 conventions.

Expected directories:

```text
theme/
  assets/
  config/
  layout/
  locales/
  sections/
  snippets/
  templates/
```

### Theme Rules

- Use Shopify-supported Liquid patterns.
- Keep sections focused and reusable.
- Prefer snippets for shared rendering logic.
- Keep schema settings understandable for merchants.
- Avoid unnecessary JavaScript.
- Avoid hardcoded visual styling where tokens can be used.
- Keep theme editor labels clear and human-readable.

---

## 8. Liquid Standards

Liquid should remain readable, predictable, and safe.

### Liquid Rules

- Keep logic simple inside templates.
- Move repeated rendering patterns into snippets.
- Avoid deeply nested conditionals when possible.
- Use meaningful variable names.
- Escape output where appropriate.
- Avoid mixing unrelated concerns in one file.
- Keep schema settings organised by user-facing purpose.

### Liquid Anti-Patterns

Avoid:

- Large monolithic sections
- Duplicated markup across variants
- Hardcoded design values
- Unclear setting names
- Overly complex conditional trees

---

## 9. CSS Standards

CSS should be token-driven, modular, and performance-friendly.

### CSS Rules

- Use design tokens and CSS custom properties.
- Keep base CSS minimal.
- Scope component styles clearly.
- Avoid unnecessary global styles.
- Avoid heavy animation defaults.
- Use responsive rules consistently.
- Ensure focus states are visible.
- Ensure text remains readable on all supported breakpoints.

### CSS Architecture Direction

Recommended structure:

```text
base.css
layout.css
tokens.css
components/
  hero.css
  product-card.css
  collection-grid.css
skins/
  mono.css
  luxury.css
  clean-commerce.css
```

Final CSS architecture will be defined in a separate CSS Architecture document.

---

## 10. JavaScript Standards

JavaScript should be used only when it provides necessary behaviour.

### JavaScript Rules

- Prefer HTML, CSS, and Shopify-native features when possible.
- Keep modules small and focused.
- Avoid global state unless necessary.
- Avoid blocking storefront rendering.
- Lazy-load optional behaviours.
- Do not load scripts for disabled features.
- Keep interactions accessible by keyboard.
- Handle unavailable DOM elements safely.

### JavaScript Anti-Patterns

Avoid:

- Large global scripts
- Unused libraries
- Heavy dependencies for small behaviours
- Inline scripts scattered across templates
- Behaviour that breaks without JavaScript unless unavoidable

---

## 11. Component Development Standards

Every component should follow the framework component model.

Required component considerations:

- Metadata
- Settings
- Variants
- Blocks
- Presets
- Styling hooks
- Accessibility rules
- Performance rules
- Documentation

### Component Rules

- Components should be reusable.
- Variants should reduce duplication.
- Blocks should be reusable where possible.
- Components should consume design tokens.
- Components should support the base design system and future skins.
- Components should avoid unnecessary dependencies.

---

## 12. Settings Schema Standards

Settings should be understandable for merchants.

### Schema Rules

- Use clear labels.
- Group settings logically.
- Keep beginner settings simple.
- Put advanced controls under advanced groups.
- Avoid exposing technical language unless necessary.
- Provide sensible defaults.
- Use presets to reduce manual configuration.

Recommended grouping:

```text
Content
Layout
Design
Behaviour
Features
Responsive
Advanced
```

---

## 13. Design Token Standards

Design tokens should be treated as the source of truth for visual styling.

Token categories:

- Colour
- Typography
- Spacing
- Radius
- Shadow
- Border
- Motion
- Breakpoint
- Z-index
- Density

Rules:

- Avoid hardcoded repeated visual values.
- Use tokens for cross-component consistency.
- Allow skins to override token values safely.
- Keep token names stable.
- Document token changes.

---

## 14. Performance Standards

Performance must be considered a product feature.

Development rules:

- Keep the base theme lightweight.
- Load assets conditionally.
- Avoid unnecessary third-party dependencies.
- Optimise images and media.
- Lazy-load non-critical assets.
- Avoid layout shifts.
- Keep JavaScript minimal.
- Measure performance before release.

Performance goals will be defined in a separate Performance Benchmarks document.

---

## 15. Accessibility Standards

Accessibility should be built into every component and feature.

Minimum requirements:

- Semantic HTML
- Keyboard navigation support
- Visible focus states
- Sufficient colour contrast
- Accessible form labels
- Meaningful link and button text
- Alt text support for images
- Reduced motion support where relevant
- Correct heading structure

Accessibility testing will be expanded in a separate Accessibility Testing document.

---

## 16. Security Standards

Security should be considered throughout the theme and companion app.

General rules:

- Sanitize and escape output where appropriate.
- Avoid unsafe script injection.
- Use minimal permissions in the companion app.
- Validate app webhooks.
- Protect API tokens and secrets.
- Follow Shopify app security requirements.
- Avoid unnecessary external dependencies.

Detailed security rules will be defined in a dedicated security checklist.

---

## 17. AI-Assisted Development Standards

This project is designed to work well with AI coding assistants.

AI assistants should:

- Read relevant documentation before implementing changes.
- Follow the component architecture.
- Avoid inventing undocumented patterns.
- Update documentation when architecture changes.
- Preserve naming conventions.
- Avoid broad refactors without clear reason.
- Keep changes focused and reviewable.
- Prefer existing patterns over new abstractions.

AI-specific rules will be expanded in dedicated AI development documents.

---

## 18. Review Standards

Every meaningful change should be reviewed for:

- Product alignment
- Architecture consistency
- Component reusability
- Performance impact
- Accessibility impact
- Documentation impact
- Naming consistency
- Theme editor UX clarity
- Skin and template compatibility

---

## 19. Testing Standards

Testing requirements should scale with the risk of the change.

Test areas:

- Theme rendering
- Component variants
- Responsive behaviour
- Accessibility
- Performance
- Browser compatibility
- Theme editor settings
- App configuration sync
- Feature enable and disable behaviour

Detailed testing strategy will be defined in separate QA documents.

---

## 20. Versioning and Change Management

The project should use clear versioning once implementation begins.

Recommended versioning approach:

- Documentation drafts: `0.x`
- Initial implementation: `0.x`
- Stable public release: `1.0`

Major architecture decisions should be documented as ADRs.

---

## 21. Contribution Rules

Contributors should:

- Understand the relevant documents before making changes.
- Keep changes scoped.
- Document new components.
- Add or update tests where relevant.
- Avoid introducing inconsistent patterns.
- Explain major decisions through ADRs.

---

## 22. Acceptance Criteria

These development standards will be considered successful when:

- Developers can understand where code and documentation belong.
- Components follow consistent rules.
- Theme settings remain merchant-friendly.
- CSS, Liquid, and JavaScript remain maintainable.
- Accessibility and performance are considered before release.
- AI coding assistants can work safely inside the repository.
- Major architecture decisions are documented.

---

## 23. Open Questions

- Which tooling should be used for formatting and linting?
- Should the theme use a CSS preprocessor or plain CSS with custom properties?
- Should JavaScript be vanilla, bundled modules, or a lightweight framework?
- How should component metadata be stored?
- What should be the first automated test suite?
- Should theme and app live in one monorepo or separate repositories later?

---

## 24. Related Documents

- Document 01 - Vision & Product Strategy
- Document 02 - Product Requirements Document
- Document 03 - Technical Architecture
- Document 04 - Design System
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 07 - Companion App Architecture
- Document 09 - Design Tokens Specification
- Document 31 - Folder Structure
- Document 32 - Coding Standards
- Document 33 - Liquid Standards
- Document 34 - JavaScript Standards
- Document 35 - CSS Architecture
- Document 40 - Testing Guidelines

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Development Standards document |
