# 🛰️ Attribution Signal Anomaly – Session Drift via Long Redirect Chains

When a click passes through multiple redirects (e.g. email → redirect → proxy → site), session attribution may drift or reset, leading to broken GA4 tracking.

---

## 🧪 What Was Detected

- Original UTM present in first redirect  
- Intermediate redirectors caused new session on arrival  
- GA4 showed fresh session with `(not set)` or wrong source  
- Redirect chain >3 hops confirmed with DevTools

---

## ⏳ Why This Matters

- Attribution breaks at scale — especially in email and affiliate campaigns  
- ROAS and source tracking appears lower than reality  
- In multi-touch flows, first touch is never logged

---

## 🔁 RCA Promotion Path

Promoted to RCA after:

✅ Redirect chain traced and confirmed  
✅ Session drift reproduced consistently  
✅ Fix added: UTM passthrough + sessionStorage fallback + short redirect

---
> “Too many redirects and your source dies in traffic.”
