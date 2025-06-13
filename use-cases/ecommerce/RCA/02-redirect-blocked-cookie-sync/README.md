# 🎯 RCA 02 – Redirect Blocked Cookie Sync (307 ➜ 302 Fix)

In this case, a vendor pixel was firing, but no cookie sync or user matching occurred. After tracing network behavior, a hidden redirect (307) was found to be the silent blocker — caused by a Mimecast-encoded security URL.

---

## 🔍 What Was Observed

- Pixel fired, but returned **307 Temporary Redirect**
- URL was encoded via **security proxy (Mimecast)**
- Vendor dashboard showed **no conversion data**
- **Cookies remained unsynced**

---

## 🧠 Root Cause

- ❌ **Redirect via Mimecast** stripped cookie headers
- 🔁 307 response interrupted identity sync
- ✅ Direct endpoint using **302 Found** restored signal flow

---

## 🛠️ Fix Applied

- Replaced security-encoded URL with **clean vendor endpoint**
- Verified **302 response** from pixel server
- Vendor began **registering conversion events** successfully

---

## ✅ Outcome

- Cookie sync restored → conversion correlation possible
- Vendor response status: ✅ Compliant and tracked
- No data leaks or PII issues observed

---

## 🔐 Related Files (Available)

- `architecture.md` – Redirect path breakdown + sync logic
- `impact.md` – Missed attribution explanation
- `solution.md` – Security proxy bypass & redirect practices

> “Redirects may look harmless — until they silence your pixels.”

📍 *RCA independently validated by system analyst*
