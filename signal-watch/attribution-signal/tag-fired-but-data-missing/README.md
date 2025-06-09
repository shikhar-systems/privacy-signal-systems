# 🛰️ Trust Signal Anomaly – Tag Fired but Data Missing

This anomaly was observed when GTM and browser DevTools showed a tag firing with status 200 — but no conversion was recorded by the vendor.

At a glance, everything appeared functional. But deeper inspection showed that the tag was **missing required dynamic parameters**, making it invisible to the vendor system.

---

## 🧪 What Was Detected

- ✅ GTM Trigger fired  
- ✅ Network call returned 200  
- ❌ Vendor showed zero conversions  
- 🔍 Only the native tag template injected required variables

---

## ⏳ Why This Matters

- Creates a **false sense of security** in QA  
- Can silently waste entire campaigns  
- Undetectable in standard GTM preview unless compared line-by-line

---

## 🎯 RCA Promotion

This anomaly was escalated to full RCA once:

✅ Custom vs Template tags were compared  
✅ Dynamic variable injection was verified as the issue  
✅ Vendor data started flowing post-fix

---

🔁 Promoted to RCA:  
[`/use-cases/ecommerce/RCA/01-tag-fired-no-conversion`](../../../use-cases/ecommerce/RCA/01-tag-fired-no-conversion/)

---

> “Sometimes the most dangerous tag is the one that says it worked — but didn’t.”
