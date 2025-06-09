# 🚫 Trust Signal – Pixel Blocked Due to Unexpected PII Disclosure

A third-party marketing or analytics pixel was fired with personally identifiable information (PII) **before user consent was established**, leading the vendor to block or drop the request.

---

## 🔍 What Was Detected

- GTM tag fired immediately on page load  
- PII (e.g. email, click ID) passed in the request  
- CMP initialized **after** the tag fired  
- Vendor-side dashboard showed dropped/blocked status

---

## 🎯 Why It Violates Trust

- User unaware that sensitive data was passed early  
- PII leaked without user action or confirmation  
- Undermines trust in system transparency and safety

---

## 🚦 RCA Promotion Path

Promoted to:  
📁 `/use-cases/retail-media/rca-06-pixel-blocked-pre-consent/`

> “A blocked pixel is sometimes the only thing protecting user trust.”
