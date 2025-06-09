# 🧩 Ecommerce RCA Library

This folder contains validated Root Cause Analysis (RCA) use cases related to tracking, attribution, and consent signal failures in ecommerce platforms.

Each case reflects a **real-world system failure** that impacted production data integrity — often silently.

---

## 🧠 RCA themes covered include:

- Missing or broken conversion signals  
- GTM trigger misfires or misconfigurations  
- Consent layers interfering with analytics or media pixels  
- Redirects blocking cookie sync or user ID propagation  
- Gaps between browser-side tags vs vendor-side capture

---

## ✅ Live RCA Use Cases

| RCA ID | Title                                              | Status  |
|--------|----------------------------------------------------|---------|
| 01     | Tag fired but no conversion recorded               | 🟢 Live |
| 02     | Redirect blocked cookie sync (307 ➜ 302 fix)       | 🟢 Live |

🔍 Each folder includes a public `README.md` and references to deeper RCA layers.

---

📌 Upcoming ecommerce RCAs are tracked in [`/use-cases/RCA-BACKLOG.md`](../../RCA-BACKLOG.md)

---

## 🔐 Additional RCA Layers (Available on Request)

Each RCA folder may include these depth files, shared selectively with qualified professionals:

- `architecture.md` — Signal → Trigger → Redirect → Data handoff flow  
- `impact.md` — Business loss, missed conversions, or compliance risks  
- `solution.md` — Fix design and system-level mitigation strategy

> Request access via GitHub Issues or LinkedIn if you're a VP, system architect, or compliance lead reviewing signal integrity.
