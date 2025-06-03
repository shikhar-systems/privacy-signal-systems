# 🧠 Product Mismatch in Event Trigger

This issue involves DOM-based event triggers picking up the wrong product ID or name when the `dataLayer` is incomplete or delayed at the time of tag execution.

---

## 🚨 What Happens

- User lands on a product detail page
- GTM tag or GA4 event fires immediately on page load
- Product info (ID, name, price) hasn’t yet rendered via API
- Tag captures incorrect or empty product values

---

## 💣 Why It’s a Problem

- Pollutes product attribution and funnel metrics
- Skews recommendation logic and A/B testing insights
- Undermines trust in ML models and personalization flows

---

## 🧠 Observed Context

Observed on ecommerce SPAs where DOM listeners (e.g., `.product-id`) triggered before asynchronous product data loaded into the page.

---

## ⏳ RCA Potential

Tracked under RCA staging path:  
📁 `/use-cases/ecommerce/predictive-qa-framework/product-mismatch-event-trigger/`

---

> “AI fails when product signals lie. This issue teaches systems to wait.”