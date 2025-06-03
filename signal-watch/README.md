# 🛰️ Signal Watch — Pre-RCA Intelligence

The `signal-watch/` folder acts as a **staging zone** for signal-level anomalies that are detected but not yet validated into full RCA-backed use cases.

These are early indicators — symptoms that something may be wrong at the consent, signal, or attribution level.

---

## 🔍 Why This Exists

Most broken signals are either:
- Ignored as edge cases, or
- Patched without root-cause visibility

`signal-watch/` prevents this by:
- Logging anomalies before they get buried
- Providing structured folders by signal type
- Giving system teams early visibility before RCA confirmation

---

## 🗂️ Folder Structure

| Folder               | What It Captures                                       |
|----------------------|--------------------------------------------------------|
| `consent-signal/`     | Invalid, missing, or non-contextual consent signals    |
| `trust-signal/`       | Signals that affect user trust (e.g., dark patterns)   |
| `attribution-signal/` | Misattribution, missing referrers, `not set` values    |
| `ai-signal/`          | Signals that may corrupt AI training or personalization|

---

## 🚦 When Does a Signal Get Promoted?

A signal anomaly in this folder becomes a formal RCA-backed **use case** when:

✅ It’s reproducible  
✅ It has platform/system impact  
✅ It can be mapped to business/compliance loss  
✅ It can be resolved through system architecture or GTM redesign

---

## 🧠 Use This Folder To:

- Build a proactive QA pipeline for signal health  
- Spot patterns before they become failures  
- Keep leadership aware of silent data leaks

> “Every critical RCA starts as a weak signal. This folder helps us listen early — and act intelligently.”