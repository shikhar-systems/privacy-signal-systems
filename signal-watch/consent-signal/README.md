# 🛡️ Consent Signal — Pre-RCA Integrity Layer

This folder tracks **pre-RCA anomalies** where user consent is:

- Missing
- Misfired
- Contextually invalid  
—even when the tags “seem” to work.

These silent failures often go unnoticed in GTM/GA4 setups — but they corrupt everything downstream.

---

## 🚨 Common Consent Signal Failures

- Tags fire **before explicit opt-in**
- CMP appears on-screen but **fails to store consent status**
- Region-based logic **bypasses consent enforcement**
- Consent data layer not ready before GTM loads  
- GTM templates behave differently than custom HTML under consent

---

## 🧨 Why This Matters

| Signal Breakdown                      | System Consequence                        |
|--------------------------------------|--------------------------------------------|
| Premature tag firing                 | Legal violations (GDPR, CPRA, etc.)        |
| Inconsistent consent status          | Inauditable data flows                     |
| Consent not stored or surfaced       | Breaks trust with regulators + users       |
| Misaligned GTM behavior              | Non-compliant analytics or marketing fire  |

> “Consent isn’t a popup — it’s a contract. If it’s broken, every signal is suspect.”

---

## 📍 Escalation to RCA

These issues escalate to formal RCA when:

✅ Impact spans legal, analytics, and marketing  
✅ Inconsistencies are reproducible across geographies/devices  
✅ Signal loss traces back to CMP, GTM, or dev-side integration gaps  
✅ The business can’t prove consent-backed tracking when audited

Promoted RCA examples:

- `/use-cases/ecommerce/tag-fired-no-conversion/`  
- `/use-cases/gtm-ga4-core/consent-mismatch-silent-tag-failure/`

---

> “If consent is unclear, every downstream signal is already broken.”
