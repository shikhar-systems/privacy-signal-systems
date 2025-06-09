# 🎯 RCA 01 – Tag Fired but No Conversion Recorded

A common yet deceptive failure: GTM shows the tag fired, DevTools reports a 200 status — but the vendor reports zero conversions. This RCA captures the invisible fault line between browser firing and vendor data ingestion.

---

## 🔍 What Was Observed

- GTM tag preview showed trigger match ✅  
- Network call showed 200 OK ✅  
- Vendor dashboard showed 0 conversions ❌  

---

## 🧠 Root Cause

- ❌ Custom HTML tag lacked required dynamic parameters
- ✅ Template-based tag worked because it injected metadata automatically
- 🧪 Comparing both tags showed missing variables on the custom version

---

## 🛠️ Fix Applied

- Deprecated custom HTML tag  
- Switched to platform’s native tag template  
- Live test confirmed proper data ingestion within 1 hour

---

## ✅ Outcome

- Conversions began flowing
- Tag health monitoring established
- Prevented silent loss from paid campaign clicks

---

## 🔐 Files Available on Request

- `architecture.md` – Trigger logic → Tag config → Signal handoff  
- `impact.md` – Campaign ROI impact + vendor reporting gap  
- `solution.md` – Mitigation flow + trigger hardening  

---

> “Just because a tag fires doesn’t mean the data lands.”

📍 RCA documented and validated by system investigator  
