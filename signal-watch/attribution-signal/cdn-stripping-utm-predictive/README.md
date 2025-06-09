# 🛰️ Predictive QA – CDN Strips UTM Parameters at Edge

An upstream CDN or edge layer silently stripped or failed to forward UTM parameters during redirect or preflight processing, causing campaign loss.

---

## 🧪 What Was Detected

- UTMs present in original request  
- CDN (e.g., Akamai, Cloudflare) rewrote or dropped query string  
- GA4 page loaded without `utm_campaign`, `utm_source`  
- No redirect visibly shown in browser

---

## ⏳ Why This Matters

- Failure is invisible at client-side  
- Entire campaign spends become “direct” or misattributed  
- QA cannot catch it without server-side header tracing

---

## 🔁 RCA Promotion Path

Promoted to RCA after:

✅ Detected pattern across multiple geos/CDN PoPs  
✅ Vendor confirmed edge config rule  
✅ Fix validated by CDN header override or redirect passthrough setting

---
> “CDNs are fast — sometimes too fast for attribution.”
