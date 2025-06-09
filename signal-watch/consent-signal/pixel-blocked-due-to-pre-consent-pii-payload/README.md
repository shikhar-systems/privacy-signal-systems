# 🚫 Consent Signal – Pixel Blocked Due to Pre-Consent PII

A Facebook/Meta or other pixel was fired with personally identifiable data (PII) **before user consent was captured**, causing vendor to block or drop the payload.

---

## 🔍 What Was Observed

- Email, user ID, or click ID passed before consent  
- CMP initialized after tag fired  
- Vendor rejected the request due to policy violation  
- No error visible in browser — only seen in vendor dashboard

---

## 🚦 Why It Matters

- High-risk regulatory exposure (GDPR, Meta TOS)  
- May silently invalidate entire campaign segments  
- Can damage retargeting, custom audience quality

---

## ⏳ RCA Promotion Path

Promoted to RCA 06:  
`/use-cases/retail-media/rca-06-pixel-blocked-pre-consent/`

> “PII leakage doesn’t always break your site — just your compliance.”
