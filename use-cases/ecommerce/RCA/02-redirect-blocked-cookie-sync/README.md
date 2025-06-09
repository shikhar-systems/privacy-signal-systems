# 🎯 RCA 02 – Redirect Blocked Cookie Sync (307 ➜ 302 Fix)

## 📌 Summary

A marketing pixel was installed to capture post-click conversions.  
In the original implementation, the destination URL was rewritten by a security layer (`Mimecast`), causing a `307 Temporary Redirect` — blocking cookie sync and data handoff.

---

## 🧠 Root Cause

- ❌ URL included an intermediate security redirect (Mimecast)
- 🔁 The request was downgraded to 307 Temporary Redirect
- 🧱 Cookie sync failed due to cross-domain and redirect protection
- ✅ When URL was updated to direct endpoint, server returned 302 (standard redirect), and data flowed

---

## 🔍 Investigation Steps

- Inspected DevTools → Network tab (noted 307 status)
- Compared current vs earlier tag code (Mimecast-encoded vs clean URL)
- Verified request payload and headers across redirects
- Validated vendor endpoint was being hit but not parsing data pre-fix

---

## 🛠️ Fix Applied

- Removed intermediate URL encoding (Mimecast sanitization layer)
- Implemented direct call to vendor endpoint
- Re-verified with DevTools → status changed to 302
- Awaiting vendor confirmation of data receipt

---

## ✅ Outcome

- Cookie sync restored (302 accepted as valid in vendor specs)
- Vendor expected to confirm real-time conversions shortly

---

> “Redirects may look harmless — until they start silencing your pixels.”
