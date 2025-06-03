# 🛡️ CMP Delay Breaks Tag Control

This issue occurs when the Consent Management Platform (CMP) loads *after* GTM, allowing tags to fire before consent is captured or verified.

---

## 🚨 What Happens

- CMP appears with visual banner  
- But GTM initializes before receiving consent state  
- Tags (GA4, Meta Pixel, LinkedIn, etc.) fire on page load — without confirmed user choice  

---

## 💣 Why It’s a Problem

- Violates GDPR, CPRA if cookies/tags are dropped before consent  
- Vendors with auto-load behavior bypass user intent  
- Generates false signal integrity → pollutes analytics and attribution  
- Legal exposure + user trust erosion  

---

## ✅ Temporary Fix Applied

- Deferred GTM execution using:  
  `window.dataLayer.push({ event: 'cmp_ready' })`  
- Introduced blocking triggers + callback logic to prevent race condition  

---

## ⏳ RCA Potential

**Promotable Use Case**:  
> CMP-GTM Timing Mismatch in Consent-First Platforms

This belongs under:  
🗂️ `signal-watch/consent-signal/` → candidate for `use-cases/ecommerce/` or `use-cases/government/`

> “When CMP lags, GTM leads — and privacy silently fails.”