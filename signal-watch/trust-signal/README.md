# 🛡️ Trust Signal — Root Layer

**Trust signals** represent the **invisible contracts** between systems and users — where user intent, tag behavior, and platform promises must stay aligned.

This folder houses all finalized signal-level observations that impact user trust, system predictability, or perception of brand integrity.

---

## 🧠 Signal Definition

A **trust signal** is broken when:

- A tag fires **too early or too late**, misaligning with user actions
- Data collection violates **user expectation or context**
- The system behaves inconsistently across journeys (A vs B user)
- An analytics or marketing system **reports data that didn’t truly occur**

---

## 📁 What’s Inside

Each file here is a finalized, public signal-level observation that broke trust and required an RCA:

| File | Description |
|------|-------------|
| `SW01-tag-fired-on-wrong-page.md` | A tag fired on a page **before user intent was confirmed** — breaking attribution and trust |
| `SW02-pixel-blocked-due-to-unexpected-pii-disclosure.md` | A tag was blocked because it tried to send **PII without proper safeguards** |

> 💡 Each observation is backed by a full RCA in the `10-zero-leak/` folder once confirmed and simulated.

---

## 🔄 Observation Lifecycle

Signal observations evolve through these phases:

1. `in-progress/` → Initial hypothesis or partial bug clue  
2. `signal-watch/trust-signal/` → Finalized observation affecting trust  
3. `10-zero-leak/` → Full RCA use case with architecture, logic, and resolution

This layered approach keeps early-stage ideas and live RCA loops **cleanly separated**.

---

## 🔐 ZeroLeak RCA™ Compliance

All signals here are part of the **ZeroLeak RCA™** methodology — ensuring:

- Clear signal loss visibility  
- Human + system-level impact analysis  
- Traceable recovery recommendations  

---

© 2025 Shikhar. ZeroLeak RCA™ is a trademarked system. Unauthorized use, duplication, or redistribution is prohibited.
