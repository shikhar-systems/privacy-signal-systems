# 🧠 Quantity Overfire Due to DOM Triggers

In this issue, the event tracking `quantity` or `add_to_cart` fires multiple times due to DOM listeners reacting to layout shifts or component re-renders.

---

## 🚨 What Happens

- User increases quantity or clicks "Add to Cart"
- DOM-based trigger responds more than once
- `add_to_cart` or `quantity` event is fired multiple times
- Tracking platforms receive inflated counts

---

## 💣 Why It’s a Problem

- Falsifies ecommerce insights and sales forecasting
- Distorts marketing ROI and product demand logic
- Breaks logic in bundle AI or dynamic pricing strategies

---

## 🧠 Observed Context

Seen on ecommerce SPAs using Angular/Vue — UI components re-rendered subtly on quantity changes, unintentionally retriggering DOM listeners bound to form elements.

---

## ⏳ RCA Potential

Escalated for system-level RCA under:  
📁 `/use-cases/ecommerce/predictive-qa-framework/quantity-overfire-due-to-dom/`

---

> “A single quantity update should reflect one intent. Not three signals.”