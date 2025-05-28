# 🎯 RCA: `(not set)` in Campaign or Medium

In GA4, the `(not set)` value often appears in `session_medium` or `session_campaign`, breaking attribution. This RCA investigates how GTM misconfiguration, redirect delays, or interstitial pages drop UTM parameters before tag execution.

---

## 🧠 Summary

- **Symptom:** GA4 shows `(not set)` in acquisition reports  
- **Stack:** GTM + GA4 + landing page redirect or JS frameworks  
- **Root Cause:** UTM dropped or overwritten before tag fires  
- **Fix Type:** System-level fallback + UTM persistence logic

---

## 💼 Job Context

This issue was observed in multiple paid media tracking audits. I led its RCA, implemented storage-based fallback logic, and validated the repair through GA4, BigQuery, and CRM matchback.

---

## 📊 Business Impact

- ROAS misreporting of ₹20L–₹1Cr+  
- Inaccurate channel performance decisions  
- Overbilling risk in performance media

---

## 📁 RCA Files

- `architecture.md` — full signal path  
- `impact.md` — revenue + ROI breakdown  
- `solution.md` — persistent UTM storage design  

🔐 *Available on request*
