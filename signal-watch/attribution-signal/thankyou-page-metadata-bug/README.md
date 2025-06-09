# 🛰️ Attribution Signal Anomaly – Thank-You Page Metadata Breaks Conversion Tagging

A broken or stripped metadata layer on the thank-you page caused the conversion tag to fire with incomplete data, leading to missed attribution.

---

## 🧪 What Was Detected

- Tag fired on page load (200 status)  
- Required campaign or referrer values missing in tag payload  
- Thank-you page had missing or corrupted metadata (e.g., JS error, DOM not ready)  
- Impact limited to certain browsers or A/B variants

---

## ⏳ Why This Matters

- Conversion tags rely on dynamic values from page context  
- Even if the tag fires, the data may be garbage or null  
- Tag previews show success, but analytics platforms don’t ingest data

---

## 🔁 RCA Promotion Path

Promoted to RCA after:

✅ Comparing DOM state pre- and post-load  
✅ Reproduced with broken metadata config  
✅ Fix validated by reordering script load and async fallback

---
> “Conversion signals aren’t just about firing — they’re about *what* you fire.”
