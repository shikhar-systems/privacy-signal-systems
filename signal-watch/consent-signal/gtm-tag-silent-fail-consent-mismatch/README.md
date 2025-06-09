# 🛑 Consent Signal – GTM Tag Silent Failure from Consent Mismatch

GTM tag appears to fire correctly — but due to timing or missing consent state, the actual signal is blocked or ignored by the downstream platform.

---

## 🔍 What Was Observed

- CMP loaded after GTM fired the tag  
- Consent state not yet available in `dataLayer`  
- Vendor rejected request due to undefined opt-in  
- GTM showed "fired", but no network payload sent or accepted

---

## 🚦 Why It Matters

- Falsely signals success in QA and preview  
- Leads to major gaps in attribution, remarketing, or analytics  
- Damages trust between analytics and compliance teams

---

## ⏳ RCA Promotion Path

Promoted to RCA 08:  
`/use-cases/gtm-ga4-core/rca-08-tag-fails-consent-mismatch/`

> “Consent timing bugs don’t scream — they silently erase data.”
