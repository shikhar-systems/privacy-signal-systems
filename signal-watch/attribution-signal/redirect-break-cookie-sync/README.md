# 🛰️ Attribution Signal Anomaly – Redirect Break Blocks Cookie Sync

This anomaly was observed when a vendor pixel returned a `307 Temporary Redirect` instead of completing cookie sync. The redirect, modified by a security proxy (Mimecast), silently prevented attribution linkage.

---

## 🧪 What Was Detected

- Pixel fired successfully from GTM  
- Status was `307 Temporary Redirect`  
- Target URL was a rewritten endpoint (Mimecast secured)  
- Vendor received no user match or signal  
- Cookie sync was silently broken

---

## ⏳ Why This Matters

- 307 status blocks headers like cookies in many browsers  
- Attribution systems rely on synced IDs to connect clicks to conversions  
- Marketing team saw zero conversions despite valid GTM firing

---

## 🎯 RCA Promotion

This anomaly was escalated into full RCA once:

✅ 302-based direct endpoint restored signal reception  
✅ Vendor confirmed restored cookie sync  
✅ Behavior was reproducible and architecture-driven

---

🔁 Promoted to RCA:  
[`/use-cases/ecommerce/RCA/02-redirect-blocked-cookie-sync`](../../../use-cases/ecommerce/RCA/02-redirect-blocked-cookie-sync/)

---

> “Attribution isn’t just about the click — it’s about the cookie handshake after it.”
