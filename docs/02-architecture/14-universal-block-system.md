# Shopify Theme Framework

**Document ID:** 14  
**Document Title:** Universal Block System  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Universal Block System

## 1. Purpose

This document defines the Universal Block System for the Shopify Theme Framework.

The Universal Block System provides a reusable approach for content blocks that can be used across sections, components, variants, templates, skins, and future premium theme products.

Its purpose is to reduce duplication, improve consistency, simplify merchant editing, and make the component architecture easier to scale.

---

## 2. Block System Vision

The framework should not rebuild the same content controls again and again inside every section.

Common content elements such as headings, text, images, buttons, icons, badges, product cards, FAQs, testimonials, and forms should follow shared rules wherever possible.

The guiding principle is:

```text
Reusable blocks. Consistent editing. Flexible composition.
```

---

## 3. Core Responsibilities

The Universal Block System is responsible for defining:

- Reusable block types
- Block metadata
- Block settings structure
- Block compatibility rules
- Block ordering rules
- Block rendering conventions
- Block styling hooks
- Block accessibility requirements
- Block performance requirements
- Block relationship with components and variants
- Block relationship with presets and templates

---

## 4. What a Block Is

A block is a reusable content or functional unit that can be placed inside a section or component.

Examples:

- Heading
- Text
- Image
- Button
- Product card
- FAQ item
- Testimonial
- Newsletter form

A block should have a clear purpose, predictable settings, and consistent rendering behaviour.

---

## 5. What a Block Is Not

A block should not become a complete page-level system.

A block should not contain unrelated layout, business, or integration logic unless that is its explicit purpose.

A block should not duplicate another existing block with only minor differences.

---

## 6. Block Model

Recommended block model:

```text
Block
  -> Identity
  -> Category
  -> Content Settings
  -> Layout Settings
  -> Design Hooks
  -> Behaviour Settings
  -> Accessibility Rules
  -> Performance Rules
  -> Compatibility Rules
  -> Documentation
```

---

## 7. Required Block Metadata

Each block should define:

| Field | Purpose |
| --- | --- |
| `id` | Stable block identifier. |
| `name` | Human-readable block name. |
| `description` | Short explanation of the block purpose. |
| `category` | Block category. |
| `status` | Lifecycle status. |
| `supportedComponents` | Components that support this block. |
| `supportedVariants` | Variants that support this block, where relevant. |
| `settingsGroups` | Editor setting groups used by the block. |
| `stylingHooks` | CSS or token hooks exposed by the block. |
| `accessibility` | Accessibility requirements. |
| `performance` | Performance notes. |
| `docs` | Related documentation links. |

---

## 8. Example Block Record

```json
{
  "id": "heading",
  "name": "Heading",
  "description": "Primary or supporting heading text used inside components.",
  "category": "content",
  "status": "draft",
  "supportedComponents": ["hero", "image-with-text", "featured-collection", "faq"],
  "supportedVariants": ["centered", "split", "stacked"],
  "settingsGroups": ["content", "design", "responsive", "advanced"],
  "stylingHooks": ["block-heading", "block-heading-text"],
  "accessibility": ["heading-level-control", "semantic-heading-order"],
  "performance": "lightweight",
  "docs": {
    "block": "docs/04-components/blocks/heading-block.md"
  }
}
```

This is a planning example. Final implementation format may evolve during development.

---

## 9. Block Categories

Initial block categories should include:

- Content Blocks
- Media Blocks
- Action Blocks
- Commerce Blocks
- Trust Blocks
- Navigation Blocks
- Form Blocks
- Interactive Blocks
- Utility Blocks

---

## 10. Initial Universal Blocks

### Content Blocks

- Heading
- Text
- Rich Text
- Badge
- Divider
- Icon
- Custom HTML, advanced only

### Media Blocks

- Image
- Video
- Gallery
- Icon Image
- Background Media

### Action Blocks

- Button
- Button Group
- Link
- Call-to-Action Group

### Commerce Blocks

- Product Card
- Product Price
- Product Media
- Product Title
- Product Vendor
- Product Rating
- Add to Cart
- Variant Selector
- Collection Card

### Trust Blocks

- Trust Badge
- Review
- Testimonial
- Guarantee
- Payment Icons
- Shipping Note

### Navigation Blocks

- Menu
- Breadcrumb
- Social Links
- Quick Links

### Form Blocks

- Newsletter Form
- Contact Form
- Search Form
- Form Field
- Checkbox
- Consent Text

### Interactive Blocks

- Accordion Item
- FAQ Item
- Tabs
- Countdown
- Popup Trigger

### Utility Blocks

- Spacer
- Separator
- Custom Liquid, advanced only
- App Block Placeholder

---

## 11. Block Settings Strategy

Block settings should follow the same progressive disclosure model used across the framework.

### Basic Settings

- Text
- Image
- Link
- Button label
- Visibility

### Standard Settings

- Alignment
- Spacing
- Width
- Basic style

### Advanced Settings

- Responsive overrides
- Token overrides
- Conditional visibility
- Behaviour options

### Developer Settings

- Custom classes
- Data attributes
- Debug options
- Integration hooks

---

## 12. Block Compatibility Rules

Not every block should be available inside every component.

Compatibility should be defined through the Component Registry.

Example:

```text
Hero Component
  Allowed Blocks:
    Heading
    Text
    Button Group
    Image
    Video
    Badge

FAQ Component
  Allowed Blocks:
    Heading
    Text
    FAQ Item
    Button Group
```

This prevents confusing or broken editing experiences.

---

## 13. Block Ordering Rules

Components and variants may define recommended block order.

Example Hero order:

```text
Badge
Heading
Text
Button Group
Media
```

Merchants may be allowed to reorder blocks when it does not break the component purpose.

Some blocks may require fixed order for accessibility or functionality.

---

## 14. Required and Optional Blocks

A component or variant may define required and optional blocks.

Example:

```text
Hero Component
  Required:
    Heading
  Optional:
    Badge
    Text
    Button Group
    Image
    Video
```

If a required block is missing, the editor should show a helpful empty state or warning.

---

## 15. Block Presets

Block presets provide ready-made block configurations.

Examples:

- Primary CTA Button
- Secondary CTA Button
- Sale Badge
- Trust Badge Row
- Product Benefit List
- FAQ Objection Item
- Testimonial Quote

Block presets should speed up merchant setup without restricting customisation.

---

## 16. Block and Variant Relationship

Variants may change how blocks are arranged or displayed.

Example:

```text
Centered Hero Variant
  Heading and text are centered.
  Media may appear below content.

Split Hero Variant
  Content blocks appear on one side.
  Media block appears on the other side.
```

The block identity remains the same, while the variant changes the structure.

---

## 17. Block and Skin Relationship

Blocks should be skin-compatible by default.

Skins may change:

- Typography
- Colours
- Spacing
- Radius
- Shadows
- Button style
- Media treatment
- Icon style

Skins should not require separate block implementations.

---

## 18. Block Rendering Rules

Block rendering should be consistent and predictable.

Rules:

- Use semantic HTML where possible.
- Use stable CSS hooks.
- Consume design tokens.
- Avoid hardcoded repeated styling.
- Avoid unnecessary JavaScript.
- Render only enabled blocks.
- Provide safe fallbacks for missing optional content.

---

## 19. Accessibility Requirements

Each block should define accessibility expectations.

Examples:

- Heading blocks should support proper heading levels.
- Image blocks should support alt text.
- Button blocks should use meaningful labels.
- Form blocks should include accessible labels and errors.
- Interactive blocks should support keyboard operation.
- Media blocks should respect reduced motion when applicable.

Accessibility belongs to the block system from the beginning.

---

## 20. Performance Requirements

Blocks should be lightweight by default.

Rules:

- Avoid loading block-specific JavaScript unless needed.
- Lazy-load media where appropriate.
- Avoid rendering empty block wrappers.
- Avoid unnecessary nested markup.
- Keep reusable block CSS minimal.
- Mark heavy blocks clearly in metadata.

Suggested performance levels:

- Lightweight
- Moderate
- Heavy

---

## 21. Shopify Theme Editor UX

Blocks should be easy to understand in the Shopify Theme Editor.

Editor labels should be merchant-friendly.

Examples:

| Internal Block | User-Facing Label |
| --- | --- |
| `heading` | Heading |
| `rich-text` | Text Content |
| `button-group` | Buttons |
| `trust-badge` | Trust Badge |
| `faq-item` | FAQ Item |
| `product-card` | Product Card |

Advanced or technical blocks should be hidden unless the user is in an advanced or developer mode.

---

## 22. Companion App Relationship

The companion app may use block metadata to power:

- Block recommendations
- Preset suggestions
- Template composition
- Feature activation
- Performance guidance
- Accessibility guidance
- AI-assisted page building

The theme should still render blocks independently without requiring the app at runtime.

---

## 23. AI Development Relationship

The Universal Block System should help AI coding assistants produce consistent output.

AI assistants should use block documentation to understand:

- Which blocks exist
- Which components support each block
- What settings each block needs
- What accessibility rules apply
- What styling hooks are available
- What blocks should not be duplicated

---

## 24. Validation Rules

Future validation tooling may check:

- Every block has required metadata.
- Every block has documentation.
- Every supported component reference is valid.
- Every required block is present in presets.
- Every block uses valid styling hooks.
- Every block has accessibility notes.
- Heavy blocks are marked correctly.

---

## 25. MVP Scope

The first version of the Universal Block System should include:

- Heading block
- Text block
- Rich Text block
- Image block
- Video block
- Button block
- Button Group block
- Badge block
- Product Card block
- Collection Card block
- FAQ Item block
- Testimonial block
- Newsletter Form block
- Trust Badge block
- Spacer block

Advanced interactive blocks, app-powered blocks, and custom block libraries can be added later.

---

## 26. Future Enhancements

Future capabilities may include:

- Block marketplace
- Agency block libraries
- AI block recommendations
- Block import/export
- Saved block groups
- Cross-store reusable blocks
- Block performance scoring
- Block accessibility scoring
- Advanced conditional block visibility
- Personalised storefront blocks

---

## 27. Acceptance Criteria

The Universal Block System will be considered successful when:

- Common blocks are reused across multiple components.
- Blocks have consistent settings and styling hooks.
- Components can define supported blocks clearly.
- Variants can arrange blocks without duplicating block logic.
- Skins can style blocks without replacing them.
- Blocks remain accessible and performance-friendly.
- Beginners can use blocks without confusion.
- Advanced users can access deeper block controls when needed.
- AI assistants can understand and reuse existing block patterns.

---

## 28. Open Questions

- Should universal blocks be implemented as Liquid snippets, section blocks, metadata records, or a hybrid system?
- How much block reuse is possible within Shopify section schema limitations?
- Should merchants be able to save custom block groups?
- Should custom blocks be supported in the first release or later?
- Should app blocks be part of the Universal Block System or separate?
- How should block deprecation be handled?

---

## 29. Related Documents

- Document 03 - Technical Architecture
- Document 05 - Component Architecture
- Document 06 - Theme Editor UX Specification
- Document 09 - Design Tokens Specification
- Document 12 - Component Registry Specification
- Document 13 - Variant Engine Specification
- Document 15 - Theme Settings Architecture
- ADR 001 - Adopt Component-First Architecture
- ADR 005 - Prefer Variant-Based Layouts over Duplicate Sections

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Universal Block System document |
