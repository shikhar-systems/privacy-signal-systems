# 🛡️ Consent Signal

This folder logs **pre-RCA anomalies** where user consent is missing, misfired, or contextually invalid — even if tags appear to work.

---

## 🚨 Common Consent Signal Failures

- Tags fire **before explicit opt-in**
- CMP triggers visually, but **status isn’t stored**
- Region-based logic silently **bypasses consent in certain geos**
- GTM loads **before consent layer sets required data**

---

## 🔍 Why It Matters

- Violates **privacy frameworks** (GDPR, CPRA, etc.)  
- Pollutes attribution, personalization, and analytics signals  
- Creates invisible **compliance risk** and weakens system trust

---

> “If consent is unclear, every downstream signal is already broken.”
