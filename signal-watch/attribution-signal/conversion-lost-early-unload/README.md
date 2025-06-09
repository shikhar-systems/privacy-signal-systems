# 🛰️ Attribution Signal Anomaly – Conversion Tag Lost Due to Early Page Unload

Some ad platform conversion tags were firing correctly but were dropped due to the user navigating away too fast — before the tag fully transmitted data.

---

## 🧪 What Was Detected

- GTM showed tag fired on thank-you page  
- Network call was aborted or had `(pending)` status  
- Common in high-speed redirect setups or fast mobile connections  
- Conversion platform showed no event captured

---

## ⏳ Why This Matters

- GTM + Preview = ✅  
- Real-world = ❌ (dropped mid-flight)  
- Impacts post-purchase tracking and ad spend optimization

---

## 🔁 RCA Promotion Path

Promoted to RCA after:

✅ Confirmed via DevTools → pending/aborted XHR  
✅ Added `navigator.sendBeacon()` + delay technique  
✅ Vendor-side logs confirmed receipt post-fix

---
> “When conversions vanish faster than the page — check the unload.”
