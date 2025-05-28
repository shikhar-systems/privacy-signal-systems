# 🧠 RCA: Product Mismatch in Event Trigger

GA4 receives the wrong product ID when tags fire before the DOM or data layer is fully ready — often during API-based product page loads.

---

## 🧠 Summary

- **Symptom:** Incorrect product or null value in GA4 events  
- **Stack:** GTM + SPA + delayed product data layer  
- **Root Cause:** Event tag fires before DOM/dataLayer is ready  
- **Fix Type:** Predictive DOM readiness logic

---

## 💼 Job Context

Observed in product detail pages during SPA transitions. I added conditional waits and fallback extraction logic to ensure the correct product payload was sent.

---

## 📊 Business Impact

- Broken ecommerce reporting  
- Misguided product performance insights  
- Loss of trust in merchandising/AI systems

---

## 📁 RCA Files

- `architecture.md` — signal delay trace  
- `impact.md` — product view distortion quantified  
- `solution.md` — DOM readiness check framework  

🔐 *Available on request*
