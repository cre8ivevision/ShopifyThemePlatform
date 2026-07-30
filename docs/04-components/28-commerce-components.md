# Shopify Theme Framework

**Document ID:** 28  
**Document Title:** Commerce Components  
**Version:** 0.1 (Draft)  
**Status:** Draft  
**Last Updated:** July 30, 2026

---

# Commerce Components

## 1. Purpose

This document defines Commerce Components for the Shopify Theme Framework.

Commerce components support shopping actions, cart behaviour, checkout preparation, product purchase confidence, and revenue-related storefront flows.

---

## 2. Component Vision

Commerce components should make buying simple, trustworthy, and fast.

```text
Reduce friction. Increase confidence. Protect performance.
```

---

## 3. Initial Commerce Components

- Cart Drawer
- Cart Page Components
- Add to Cart
- Dynamic Buy Buttons
- Product Recommendations
- Recently Viewed Products
- Product Badges
- Shipping Message
- Free Shipping Bar
- Trust Badges
- Payment Icons
- Discount Message

---

## 4. Supported Variants

- Minimal cart
- Drawer cart
- Full cart page
- Sticky add to cart, advanced
- Quick add
- Upsell recommendation, future
- Free shipping progress, future

---

## 5. Supported Blocks

- Product Line Item
- Price
- Quantity Selector
- Remove Button
- Checkout Button
- Discount Message
- Shipping Message
- Trust Badge
- Product Recommendation
- Payment Icons

---

## 6. Settings Strategy

Basic settings:

- Cart type
- Show checkout button
- Show notes
- Show trust badges

Advanced settings:

- Cart drawer behaviour
- Upsell placement
- Free shipping threshold
- Sticky add to cart
- Recommendation display
- Cart performance options

---

## 7. Accessibility Requirements

- Cart drawer must manage focus.
- Cart updates must be announced where appropriate.
- Quantity controls must be keyboard accessible.
- Checkout buttons must be clear.
- Error states must be understandable.

---

## 8. Performance Requirements

- Cart drawer scripts load only when enabled.
- Recommendations should not block core purchase flow.
- Avoid heavy upsell logic by default.
- Keep cart interactions resilient.

---

## 9. MVP Scope

First release should include Add to Cart, Cart Page basics, optional Cart Drawer, Product Badges, Trust Badges, and Payment Icons.

---

## 10. Related Documents

- Document 16 - Feature Manager Architecture
- Document 18 - Performance Engine
- Document 24 - Product Components

---

## Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 0.1 | July 30, 2026 | Initial Draft | First Commerce Components specification |
