# 🛡️ Language Switch Breaks Consent Layer

On multilingual platforms, switching language resets or misfires the consent layer.

---

## 🚨 What Happens

- User gives consent in Hindi → switches to English
- CMP reloads but previous status lost or re-triggers
- Some tags fire again or get blocked inconsistently

---

## 💣 Why It’s a Problem

- Affects vernacular user experience
- Breaks trust in platforms serving Bharat / multilingual users
- Can lead to double-firing or misattribution

---

## ⏳ RCA Potential

Ideal for a future RCA under “Multilingual Consent Failures in National-Scale Platforms”
