# 🛰️ Signal Watch — Pre-RCA Intelligence

The `/signal-watch/` folder acts as a **staging zone** for signal-level anomalies that are detected but not yet validated into Root Cause Analysis (RCA) cases.

These are early indicators — symptoms that something may be wrong at the **consent**, **trust**, **attribution**, or **AI signal** level.

---

## 🔍 Why This Exists

Most broken signals are either:

- ❌ Ignored as edge cases, or  
- ❌ Patched without root-cause visibility  

`/signal-watch/` prevents this by:

- ✅ Logging anomalies before they get buried  
- ✅ Providing structured folders by signal type  
- ✅ Giving system teams early visibility before RCA confirmation  

---

## 🗂️ Folder Structure

| Folder               | What It Captures                                                |
|----------------------|-----------------------------------------------------------------|
| `consent-signal/`     | Invalid, missing, or misaligned consent signals                 |
| `trust-signal/`       | Signals that affect user trust (e.g., dark patterns, trick UX)  |
| `attribution-signal/` | Misattribution, missing referrers, "not set" or UTM corruption  |
| `ai-signal/`          | Signals that can corrupt AI models or personalization layers    |

---

## 🚦 When Does a Signal Get Promoted?

A signal anomaly becomes a formal RCA-backed use case when it is:

✅ Reproducible  
✅ Mapped to a system/platform flaw  
✅ Linked to measurable business or compliance risk  
✅ Solvable through architecture, tag config, or GTM redesign  

---

## 🧠 Use This Folder To:

- Build a proactive QA pipeline for signal health  
- Spot patterns before they become failures  
- Keep leadership aware of silent data leaks  

> “Every critical RCA starts as a weak signal. This folder helps us listen early — and act intelligently.”
