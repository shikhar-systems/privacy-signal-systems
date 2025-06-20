# 🎯 RCA 02 – Redirect Blocked Cookie Sync (307 ➜ 302 Fix)

A vendor marketing pixel was firing from GTM and appeared normal in the browser — but conversions were **not being registered** on the vendor dashboard.

Upon inspection, the root issue was traced to a **307 redirect** triggered by a security-layer (Mimecast), which silently **broke the cookie sync process** — cutting off identity propagation mid-flight.

Further analysis revealed this issue was technically identical to [RCA 01 – Tag Fired but No Conversion Recorded](https://github.com/shikhar-systems/privacy-signal-systems/tree/main/use-cases/ecommerce/RCA/01-tag-fired-no-conversion). Both have now been **merged** under this RCA.

---

## 🔍 Observed Behavior

- ✅ GTM tag triggered correctly  
- 🔁 Network tab showed `307 Temporary Redirect`  
- 🔒 Destination URL was routed via Mimecast  
- 🚫 Vendor dashboard reported **no conversions**  
- 🍪 No cookies were set (cookie sync interrupted)

---

## 🧠 Root Cause

- ❌ 307 redirect broke the **identity sync** process  
- ❌ Cookie headers were **stripped** at redirect level  
- ✅ GTM and trigger logic were accurate  
- 🤐 No errors in console or network — signal dropped silently

---

## 🛠️ Fix Applied

- Switched to **direct vendor pixel endpoint** (bypassed Mimecast)  
- Redirect changed from `307 ➜ 302`  
- Vendor system immediately began capturing conversions  
- Cookie sync restored via `Set-Cookie` (browser behavior confirmed)

---

## ✅ Outcome

| Before Fix                   | After Fix                    |
|-----------------------------|------------------------------|
| 🔁 307 redirect (Mimecast)  | ✅ 302 direct endpoint        |
| ❌ Cookie sync failed        | ✅ Cookie set successfully    |
| 🚫 Conversions not tracked   | 📈 Conversions tracked        |
| 🤐 Silent signal break       | 🔄 Full signal restored       |

---

## 🔐 Related Technical Files

- [`logic-explainer.md`](./logic-explainer.md) – Trigger + redirect logic  
- [`architecture.md`](./architecture.md) – Consent-aware tag architecture  
- [`impact.md`](./impact.md) – Attribution loss + revenue risk  
- [`solution.md`](./solution.md) – Fix + redirect handling playbook  
- 📸 Screenshots: 307 → 302 redirect sequence, GTM firing

---

## 🧭 RCA 01 Status

> This RCA **absorbs and replaces**  
> [`RCA 01 – Tag Fired but No Conversion Recorded`](https://github.com/shikhar-systems/privacy-signal-systems/tree/main/use-cases/ecommerce/RCA/01-tag-fired-no-conversion)

---

> _“Redirects may look harmless — until they silently drop your signal.”_

📍 _RCA independently executed and validated by system investigator_
