# 🔒 Dark Pattern in Consent Timer

This issue captures a deceptive UX pattern where **consent banners auto-accept** all categories after a countdown — **without explicit user interaction**.

---

## 🚨 What Happens

- User lands on the page
- Consent banner shows a 5-second timer
- If no action is taken, **all consent categories are auto-accepted**
- No opt-in, no granular control — just passive timeout

---

## 💣 Why It’s a Problem

- Violates **active consent** principles under GDPR and similar laws
- Creates **legal ambiguity** and audit risk for regulated sectors
- May be flagged as **dark pattern** by UX activists and privacy watchdogs
- Damages trust in platforms handling sensitive data (finance, health, education)

---

## 🧠 Strategic Context

This tactic is increasingly seen in:
- AdTech-heavy ecommerce portals
- EdTech platforms targeting minors
- Finance portals using third-party pixels
- Sites trying to balance growth + compliance via UX shortcuts

---

## ⏳ RCA Potential

This will be escalated as part of a flagship RCA Loop:
📁 `/use-cases/ecommerce/trust-signal/dark-pattern-consent-timer/`

Title: **“Dark Patterns in Consent UX: Timer-Based Auto-Accept”**

---

> “The most dangerous breach of consent isn’t code — it’s a timer pretending to be permission.”