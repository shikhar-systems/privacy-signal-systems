# 🎯 Signal Break Across National Digital Subdomains

This use case highlights attribution challenges observed when users navigate across platforms managed by different public service domains.

---

## 🚨 What Happens

- A user begins their journey on one national platform → transitions to another (e.g., ID services → welfare services)
- Analytics session breaks; referrer is lost
- Campaigns, service discovery, or form completions get misattributed

---

## 💣 Why It’s a Problem

- Disrupts continuity in digital public service funnels
- Undermines cross-agency performance measurement
- Obscures full-funnel engagement insights critical to citizen-centric policy

---

## 🔍 Why It Occurs

- Subdomains are treated as separate analytics properties
- No shared identity or session stitching across platforms
- Referrer headers suppressed due to security or privacy policies

---

## 🧠 Strategic Context

This is a system-level architecture gap — not a tool limitation.  
It signals the need for:

- Inter-agency signal continuity frameworks  
- Unified session attribution governance  
- Consent-aligned tracking standards in national digital ecosystems

---

## ⏳ RCA Potential

This case will be developed under:

📁 `/use-cases/government/gtm-ga4-signal-break/cross-platform-signal-loss/`

It aligns with national digital transformation goals that require **cross-platform trust**, **signal reliability**, and **interoperable measurement models**.

---

> “When signals break across platforms, citizens lose continuity — and systems lose insight.”