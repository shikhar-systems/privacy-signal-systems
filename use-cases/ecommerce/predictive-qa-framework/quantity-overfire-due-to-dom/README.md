# 🔄 RCA: Quantity Overfire Due to DOM

Quantity events in GA4 (e.g. `add_to_cart`) may overfire when DOM listeners react to visual or layout updates, especially in dynamic frameworks like React/Vue.

---

## 🧠 Summary

- **Symptom:** Quantity >1 in GA4 even when user clicked once  
- **Stack:** GTM + DOM listeners + SPA re-render cycles  
- **Root Cause:** DOM changes trigger listeners multiple times  
- **Fix Type:** Event throttling + fire-on-intent design

---

## 💼 Job Context

Observed during cart tracking audits for dynamic UIs. Implemented quantity change gating logic to track only user-intended interactions.

---

## 📊 Business Impact

- Inflated cart value metrics  
- Discrepancy between frontend/cart systems and GA4  
- Ad budget misalignment based on false demand

---

## 📁 RCA Files

- `architecture.md` — DOM & GTM trigger map  
- `impact.md` — quantity mismatch loss model  
- `solution.md` — intent-based trigger setup  

🔐 *Available on request*
