# 🔐 Consent Signal – Pixel Leak Avoided via Server-Side GTM Redesign

Client-side tags risk leaking user data before consent. A server-side GTM shift was used to control the fire path based on verified opt-in.

---

## 🔍 What Was Observed

- Tag fired before consent confirmed  
- Vendor pixel captured user-level data (e.g., click ID, email)  
- Risk of PII or ad tracking violation  
- Refactored to server-side endpoint that honors consent token

---

## 🚦 Why It Matters

- Prevents unauthorized marketing data from reaching platforms  
- Supports regulatory compliance (GDPR, CPRA)  
- Improves trust with privacy, legal, and infosec stakeholders

---

## ⏳ RCA Promotion Path

Promoted to RCA 07:  
`/use-cases/fintech/rca-07-server-side-consent-guardrail/`

> “The best consent enforcement happens where the browser can't lie.”
