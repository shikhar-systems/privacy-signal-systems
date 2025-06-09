# 🎯 RCA 02 – Redirect Blocked Cookie Sync (307 ➜ 302 Fix)

In this case, a vendor pixel was firing, but no cookie sync or user matching occurred. After tracing network behavior, a hidden redirect (307) was found to be the silent blocker — caused by a Mimecast-encoded security URL.

---

## 🔍 What Was Observed

- Pixel fired → but status code was `307 Temporary Redirect` ❌  
- URL was encoded via security proxy (Mimecast)  
- No data received by vendor — cookies unsynced  

---

## 🧠 Root Cause

- ❌ Redirect via Mimecast stripped cookie headers  
- 🔁 307 response failed to reach vendor endpoint  
- ✅ Direct endpoint (302) restored cookie sync behavior

---

## 🛠️ Fix Applied

- Replaced Mimecast-altered URL with clean vendor endpoint  
- Verified response changed to `302 Found`  
- Vendor endpoint began registering signal receipt

---

## ✅ Outcome

- Restored cookie sync required for conversion correlation  
- Pixel started responding as per spec  
- Awaiting final vendor confirmation (no data leaks observed)

---

## 🔐 Files Available on Request

- `architecture.md` – Redirect path breakdown + cookie sync logic  
- `impact.md` – Missed conversion attribution + sync loss  
- `solution.md` – Security bypass and redirect best practices  

---

> “Redirects may look harmless — until they silence your pixels.”

📍 RCA independently validated by system analyst  
