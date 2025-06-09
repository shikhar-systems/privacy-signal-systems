# 🛰️ Attribution Signal Anomaly – Vanity URL Causes UTM Loss

Vanity or shortened URLs often introduce unexpected redirects or stripping behavior that leads to loss of UTM parameters before GA4 can capture them.

---

## 🧪 What Was Detected

- UTM parameters were present in the original ad/click URL  
- Vanity URL used a redirect (e.g. `brand.link/offer` → `site.com`)  
- GA4 `session_source`, `medium`, or `campaign` resolved as `(not set)`  
- GTM firing delayed or fired after redirect finished

---

## ⏳ Why This Matters

- Attribution gaps occur without obvious errors  
- Entire campaign clicks appear as "direct / none" in GA4  
- Loss of media ROI clarity despite technically correct tagging

---

## 🔁 RCA Promotion Path

Promoted to RCA after confirming:

✅ UTM lost after redirect  
✅ No fallback mechanism to persist parameters  
✅ Fix validated by using full redirect-aware UTM preservation

---
> “When links are short, your data shouldn't be.”
