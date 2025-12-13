# VitalBlend - Shopify Developer Interview

This repository contains the theme code for the VitalBlend product page implementation.

## 🚀 How to Preview
1. Access the development store (URL de tu tienda).
2. Navigate to the product **VitalBlend Superfood Mix**.
3. Ensure the URL parameter `?view=vitalblend` is used if the template isn't assigned by default.
   - Example: `https://[tu-tienda].myshopify.com/products/vitalblend-superfood-mix?view=vitalblend`

## 🛠 Features Implemented
- **Custom Liquid Section:** `main-vitalblend-product.liquid` built from scratch (no Dawn code copied).
- **Variant Logic:** Custom JS to handle variant switching using "Pill" selectors instead of dropdowns.
- **Subscription UI:** - Mocked "Subscribe & Save" functionality.
  - Toggles pricing and shows frequency selector.
  - Passes `Shipping Frequency` as a Line Item Property to the cart.
- **Metafields:**
  - `custom.promotional_headline` for the sub-header.
  - `custom.how_to_use_steps` (Metaobject) for the instructional steps.

## ⚙️ Configuration
- Go to **Theme Editor > VitalBlend Product**.
- You can customize the "Subscribe" text and Button colors via the Section Settings schema.
- "You May Also Like" section is configured via the `VB Recommendations` section settings (select a collection).

## 📝 Notes
- Since I didn't have a Selling Plan API available, the subscription logic is a UI simulation that passes data to the cart properties, as allowed in the "Acceptable alternative" instructions.