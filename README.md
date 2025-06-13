# 🛒 Shopify Cart Drawer Product Recommendations

## 📌 Overview
This feature modifies the Shopify cart drawer to display up to **4 recommended products** based on a selected collection. Products are displayed only when the drawer is opened and allow inline "Add to Cart" functionality without navigating away from the page.

---

## 🔧 Features
- Displays up to 4 recommended products in the cart drawer.
- Collection is selected via theme settings (admin configurable).
- Uses native Shopify quick add and product-form logic.
- Fully responsive and horizontally scrollable.
- Non-blocking performance (loads instantly with the cart).

---

## ⚙️ Implementation Summary

- **Theme Setting Added:**  
  A `collection` type field was added in `settings_schema.json` under the ID: `cart_recommendation`.

- **Custom Snippet:**  
  A snippet named `cart-recommendation.liquid` was created to render selected products from the chosen collection.

- **Product Card Snippet:**  
  A separate `card-product-cart.liquid` snippet was used to customize how the products look inside the cart drawer.

- **Cart Drawer Modification:**  
  The `cart-recommendation` snippet was rendered just above the footer in the `cart-drawer.liquid` section.

- **Assets Used:**  
  Existing Shopify JS files like `quick-add.js` and `product-form.js` were included to support inline add-to-cart.

---

## 📁 File Structure (Modified / Added)

/snippets
└── cart-recommendation.liquid
└── card-product-cart.liquid

/sections
└── cart-drawer.liquid

/config
└── settings_schema.json (added collection setting)


## 🧪 How to Test

1. Open the Shopify theme editor (Customize).
2. Select a **collection** in the `Cart Recommendation` field.
3. Add a few products to that collection.
4. Open the cart drawer from the storefront.
5. You should see 4 product recommendations below the cart items.
6. Click "Add to Cart" — it should add the item inline and show confirmation.

---


## 🛠 Built With

- Shopify Liquid
- Theme Settings Schema
- Native Shopify product-form / quick-add
- Custom snippets

---

## ✅ Result

This solution allows merchants to visually upsell relevant products inside the cart drawer, increasing the chance of higher order values without affecting the core cart experience.
