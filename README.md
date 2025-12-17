# VitalBlend - Shopify Developer Interview

This repository contains the custom theme code for the VitalBlend product page implementation.

## 🚀 How to Preview
1. Access the development store here: **https://luis-portugal-dev.myshopify.com/**
2. Navigate to the product **VitalBlend Superfood Mix**.
3. **Note:** The `vitalblend` template has been assigned as the default for this product. However, you can also force the view using the query parameter:
   - URL: `https://luis-portugal-dev.myshopify.com/products/vitalblend-superfood-mix?view=vitalblend`

## 🛠 Features Implemented
- **Custom Liquid Section:** `main-vitalblend-product.liquid` built from scratch (no reliance on default theme sections).
- **Advanced Variant Logic:**
  - Custom JavaScript to handle variant switching using "Pill" selectors.
  - **Dynamic Image Switching:** Product image updates automatically based on the selected variant.
  - URL parameter updates without page reload (`window.history.replaceState`).
- **Subscription UI (Simulation):**
  - Custom "Subscribe & Save" toggle widget.
  - Dynamically updates the price display.
  - Passes `Shipping Frequency` as a Line Item Property to the cart for backend processing.
- **Metafields & Metaobjects:**
  - `custom.promotional_headline` for the sub-header.
  - `custom.how_to_use_steps` (Metaobject) for the instructional steps section.
- **Cross-Sell Section:** Independent section (`vitalblend-recommendations`) driven by collection data.

## ⚙️ Configuration
- **Theme Editor:**
  - Go to **VitalBlend Product** template.
  - Customize texts, colors, and subscription labels via the Section Schema.
  - "You May Also Like" section content is managed by selecting a Collection in the section settings.

## 📝 Technical Notes
- **Subscription Logic:** As the Native Subscription API (Selling Plans) requires a backend App installation not available in this test environment, the subscription logic is a **Frontend UI simulation**. It captures the user's intent and passes the frequency data to the cart properties, fulfilling the "Acceptable alternative" requirement.
- **Price in Cart:** Due to Shopify's security restrictions, the cart line-item price cannot be modified via frontend JavaScript alone. In a production environment, this would be handled by the `selling_plan_id`.