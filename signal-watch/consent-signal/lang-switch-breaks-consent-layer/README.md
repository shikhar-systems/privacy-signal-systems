# 🛡️ Language Switch Breaks Consent Layer

On multilingual platforms, switching language resets or misfires the consent layer.

---

## 🚨 What Happens

- User gives consent in Hindi → switches to English  
- CMP reloads but previous status is lost or re-triggers  
- Some tags fire again or get blocked inconsistently  

---

## 💣 Why It’s a Problem

- Affects vernacular user trust and experience  
- Breaks consistency on platforms serving Bharat / multilingual users  
- Can cause double-firing, underfiring, or incorrect attribution  

---

## ⏳ RCA Potential

Ideal for future RCA under:  
**“Multilingual Consent Failures in National-Scale Platforms”**

This fits under:  
🗂️ `signal-watch/consent-signal/` → Promotable to `use-cases/government/` or `use-cases/ecommerce/` depending on context.

> “When language changes, consent logic must persist — or systems break trust without warning.”