# 🛡️ Consent Signal

This folder logs pre-RCA issues where **user consent is missing, misfired, or contextually invalid**.

---

## 🚨 Examples of Consent Signal Issues

- Tracking fires before user gives explicit consent
- Consent banner triggers but doesn't store status
- Region-based logic bypasses consent for specific geos
- Consent data layer not available to tag manager on time

---

## 🔍 Why It Matters

- Violates user trust and privacy laws (GDPR, CPRA, etc.)
- Pollutes downstream signals that rely on valid consent
- Leads to audit failure and legal risk

---

> “If consent is unclear, every downstream signal is already broken.”