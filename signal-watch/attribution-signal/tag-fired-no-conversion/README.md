# 🟡 RCA Backlog – Upcoming Releases

This backlog contains strategic RCA use cases that are **finalized but not yet published**.  
They span across industries and reflect deep system-first debugging across GTM, GA4, Consent, Privacy, and AdTech.

---

## 📋 Planned RCA Titles

| RCA ID | Title                                             | Industry        | Audience                          | Status     |
|--------|---------------------------------------------------|------------------|------------------------------------|------------|
| 03     | GA4 'not set' source attribution issue            | gtm-ga4-core     | MarTech, VP Growth                | 🟡 Planned |
| 04     | Custom HTML tag not firing on Thank You page      | ecommerce        | GTM QA, Analytics Engineering     | 🟡 Planned |
| 05     | Template tag firing but vendor sees no conversion | ecommerce        | MarTech, Agency Ops               | 🟡 Planned |
| 06     | Facebook tag blocked due to PII                   | retail-media     | Privacy, MarTech Leads            | 🟡 Planned |
| 07     | Meta pixel leak prevented via server-side GTM     | fintech          | Data Privacy, VP Engineering      | 🟡 Planned |
| 08     | GTM tag fails silently due to consent mismatch    | gtm-ga4-core     | Privacy QA, Data                  | 🟡 Planned |
| 09     | iFrame breaks form submission signal              | ecommerce        | Web QA, CRO                       | 🟡 Planned |
| 10     | UTM parameters stripped after redirect            | retail-media     | AdOps, Campaign Analysts          | 🟡 Planned |
| 11     | Conversion tag fires on incorrect page            | ecommerce        | Analytics QA, GTM Devs            | 🟡 Planned |
| 12     | Broken enhanced ecommerce (product_view event)    | ecommerce        | Ecom Analytics, Product Dev       | 🟡 Planned |
| 13     | GA4 dimension mismatch in BigQuery export         | gtm-ga4-core     | Data Engineering                  | 🟡 Planned |
| 14     | Predictive QA failures missing in analytics       | ai-product       | QA Infra, Platform PMs            | 🟡 Planned |
| 15     | Consent defaults blocking high-value tags         | gtm-ga4-core     | Legal, Compliance, Product Data   | 🟡 Planned |
| 16     | Firebase install events not tracked in GA4        | ai-product       | Mobile Dev, Product Analytics     | 🟡 Planned |
| 17     | Server-side GTM not sending required payload      | fintech          | Data Infra, AdTech Leads          | 🟡 Planned |

📍 Each of these will be published after validation, anonymization, and consent approval where needed.

You can track public releases at: [`RCA-INDEX.md`](./RCA-INDEX.md)

---

## 🔬 Under Signal Watch – AI Anomalies Being Monitored

These cases are in the AI signal watch layer. They’ve not yet been validated into RCA, but show strong potential due to their systemic nature.

| Candidate Title                                       | Source Folder Path                                                   | RCA Readiness     |
|------------------------------------------------------|------------------------------------------------------------------------|--------------------|
| Hallucination from malformed input                   | `/signal-watch/ai-signal/hallucination-from-malformed-input/`         | In Signal Watch    |
| Personalization drift due to consent loss            | `/signal-watch/ai-signal/ai-personalization-drift-due-to-consent-loss/`| In Signal Watch    |

> These issues will be promoted if proven reproducible and materially impactful in production AI systems.
