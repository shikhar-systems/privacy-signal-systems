# 🎯 RCA 02 – Redirect Blocked Cookie Sync (307 ➜ 302 Fix)

In this case, a vendor marketing pixel appeared to fire normally. However, conversions were missing from the vendor dashboard. After inspecting network behavior, we uncovered a silent redirect — a `307 Temporary Redirect` caused by a security-layered URL (Mimecast) — that was **breaking cookie sync**.

---

## 🔍 Observed Behavior

- ✅ Pixel fired (visible in GTM & Network tab)
- 🔁 Returned **307 Temporary Redirect**
- 🔒 URL wrapped via **Mimecast security proxy**
- 🚫 Vendor dashboard showed **no matched conversions**
- 🍪 No cookie was set or synced

---

## 🧠 Root Cause

- ❌ **307 Redirect** interrupted identity propagation
- ❌ Cookie headers **stripped by Mimecast** redirect
- 🔍 Intermediate hop → broke sync with vendor server
- 🧪 No errors in browser, yet **signal silently dropped**

---

## 🛠️ Fix Applied

- Replaced the redirect-wrapped URL with **direct pixel endpoint**
- 307 → 302 (server-side status confirmed)
- Network call showed:  
  `Status: 302` and `Set-Cookie: ✅`
- Vendor immediately **registered conversions**

---

## ✅ Outcome

| Before Fix | After Fix |
|------------|-----------|
| 🔁 307 redirect | ✅ 302 direct endpoint |
| ❌ Cookie sync failed | ✅ Cookie set successfully |
| 🚫 Conversions not tracked | 📈 Conversions tracked correctly |
| 🔒 Signal break (invisible) | 🔄 Full signal restored |

---

## 🔐 Related Technical Assets

- [`architecture.md`](./architecture.md) – Redirect path + consent-aware GTM flow
- [`logic-explainer.md`](./logic-explainer.md) – Trigger + consent + redirect fix logic
- [`impact.md`](./impact.md) – Attribution + identity mismatch analysis
- [`solution.md`](./solution.md) – Redirection risk mitigation playbook

> _“Redirects may look harmless — until they silence your pixels.”_

📍 _RCA independently executed and validated by system analyst_
