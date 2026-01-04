# Vitalblend Interview Theme - Shopify Developer Implementation

This repository contains the custom theme code for the **Vitalblend** product page, featuring high-fidelity UX and technical improvements as part of a Shopify developer interview.

## 🚀 How to Preview
1. Access the development store: **https://luis-portugal-dev.myshopify.com/**
2. Navigate to the product **Vitalblend Superfood Mix** (or your rebranded product).
3. Use the custom template:
   - Template: `product.vitalblend.json`
   - URL parameter: `?view=vitalblend`

## 🛠 Features Implemented
- **High-Fidelity Product Page:** `main-vitalblend-product.liquid`
  - Vertical image gallery with zoom-on-hover.
  - Custom pill-style variant selectors with icons (using the 🌿 icon for flavor).
  - Native Shopify **Selling Plans** integration for real subscriptions.
  - Custom rounded quantity selector (+/-).
  - Dynamic price calculations (10% discount for subscriptions).
- **Sticky Add to Cart Bar:** Appears automatically as you scroll down for better conversion.
- **Metafield-Driven Sections:**
  - Promotional headlines and instructional steps derived from product metafields/metaobjects.
- **Cross-Sell Section:** `vitalblend-recommendations.liquid` with "Quick Add" AJAX functionality.

## ⚙️ Configuration
- **Theme Editor:**
  - Assign the `vitalblend` template to your product.
  - Customize context and sections via the Section Schema.
- **Data Source:**
  - Content for icons and "How to Use" steps is managed via Product Metafields.

## 📝 Technical Notes
- **Subscription Logic:** This version uses native `selling_plan` parameters. Fallback logic is included to simulate the UX if no selling plans are active in the store.
- **Styling:** Vanilla CSS with custom property tokens (`--vb-` prefix) for a clean, brand-consistent look.

