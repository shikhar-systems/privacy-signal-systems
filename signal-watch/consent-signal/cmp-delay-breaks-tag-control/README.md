# 🛡️ CMP Delay Breaks Tag Control

This issue occurs when the Consent Management Platform (CMP) loads *after* GTM, allowing tags to fire before consent is captured or verified.

---

## 🚨 What Happens

- CMP fires with visual banner
- But GTM doesn't receive updated consent status in time
- Tags fire on page load regardless of user choice

---

## 💣 Why It’s a Problem

- Violates GDPR, CPRA if cookies/tags are dropped without prior consent
- Tag vendors may auto-load (Meta Pixel, GA4, LinkedIn)
- Creates false signal integrity and legal exposure

---

## ✅ What Was Done

- Deferred GTM script using a `window.dataLayer.push({event: 'cmp_ready'})` logic
- Added blocking triggers and resolved race condition via callback

---

## ⏳ RCA Potential

Ideal for RCA promotion in enterprise sites with multiple CMP-GTM sync issues.
