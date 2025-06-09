# 🎯 Attribution Signal — Pre-RCA Layer

This folder captures signal-level breakdowns where **source, campaign, or channel attribution silently fails** — long before revenue impact is obvious.

These issues often hide in plain sight, masked by “valid” pageviews or triggered tags — yet they quietly destroy performance insights.

---

## 🚨 Common Attribution Signal Failures

- `(not set)` in GA4 for source / medium / campaign  
- Referrer dropped due to redirects, interstitials, or iFrames  
- UTMs lost across session flow or overwritten by late-firing tags  
- Attribution cookies expired or blocked before conversion  
- Ad platform and landing page misaligned on ID capture  

---

## 💣 Why This Matters

| Signal Breakdown                      | Strategic Consequence                      |
|--------------------------------------|--------------------------------------------|
| Missing UTMs or source data          | ROI visibility collapses                   |
| Incorrect referrer or medium         | Wrong funnel attribution                   |
| Session stitching failure            | Broken multi-touch tracking                |
| Late tag firing                      | Lost conversion credit                     |

> Attribution signal loss doesn’t raise alerts — it erases insight.

---

## 🧭 Escalation Path to RCA

These issues move from anomaly to Root Cause Analysis when:

✅ Reproducible across platforms or campaigns  
✅ Affecting spend justification or CRO strategy  
✅ Mappable to architecture: GTM, consent, redirect, or tag delay  
✅ Causes business misinterpretation at the leadership level

Promoted RCA examples are tracked under:

- `/use-cases/ecommerce/not-set-campaign-medium/`
- `/use-cases/ecommerce/redirect-blocked-cookie-sync/`

---

> “If attribution fails, every growth decision is already flawed.”
