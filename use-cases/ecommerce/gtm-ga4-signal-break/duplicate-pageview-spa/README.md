# 📄 RCA: Duplicate `page_view` in SPA

In Single Page Applications (SPA), GTM may fire `page_view` multiple times as users navigate routes, even when the page isn't reloaded. This causes inflated session counts and misreported engagement.

---

## 🧠 Summary

- **Symptom:** Multiple `page_view` hits on one route  
- **Stack:** SPA (React/Vue) + GTM + GA4  
- **Root Cause:** History change listener triggers without de-duplication  
- **Fix Type:** One-time fire logic + virtual pageview tagging

---

## 💼 Job Context

I found this in SPA ecommerce builds where routing triggers were not scoped properly. I implemented route-change filters and custom flags to prevent overfire.

---

## 📊 Business Impact

- 10–20% session inflation  
- Bounce rate anomalies  
- Misleading time-on-page and user flow data

---

## 📁 RCA Files

- `architecture.md` — routing + trigger flow  
- `impact.md` — funnel-level distortion explained  
- `solution.md` — one-time fire rule + router validation  

🔐 *Available on request*
