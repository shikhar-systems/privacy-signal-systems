# 🧭 Architecture Overview — ZeroLeak RCA™

> A high-level walkthrough of how signals flow — and silently fail — in real-world systems, and how ZeroLeak RCA™ detects and recovers them.

---

## 🎯 CXO Summary

In today’s signal economy, every click, view, and submit triggers a cascade of logic across consent tools, tag managers, cookies, and analytics systems. When this logic fails silently — due to misfired tags, blocked scripts, or missing user IDs — it breaks attribution, erodes trust, and loses revenue.

ZeroLeak RCA™ brings **real-time traceability** and **root cause intelligence** to this invisible battlefield.

---

## 🔄 ZeroLeak RCA™ Flow: Consent to RCA

```mermaid
flowchart TD
    A[User lands on site] --> B[Consent Banner Displayed]
    B -->|Accepts| C[Consent Captured in CMP such as OneTrust]
    C --> D[Tags Fired via GTM/GTM 360]
    D --> E[Signal Sent to GA4, Ads, Pixels]
    E --> F[Data Enters Reporting Layer: GA4, BQ, CDP]
    F --> G[Signal Quality Evaluated]
    G --> H[ZeroLeak RCA™ Detects Failure or Success]
    H --> I[Signal Recovery Initiated if Needed]
```

---

## 🔍 Signal RCA Trigger Flow (Failure Detected)

```mermaid
graph TD
    A[User Action: Click, View, Submit]
    B[Tag Trigger in GTM]
    C[Cookie & Consent Check]
    D[DataLayer Integrity Check]
    E[Network Request Fired]
    F[Analytics Logging: GA4, Ads, etc.]
    G[Signal Visible in Report?]
    H[ZeroLeak RCA™ Triggered]
    I[Root Cause Mapping: Consent · Cookie · Tag · Network]
    J[Recovery Pattern Suggested]

    A --> B --> C --> D --> E --> F --> G
    G -->|No| H --> I --> J
```

---

## 🧱 Layer Mapping

| Stage | Layer |
|-------|-------|
| Consent Banner | UX / Browser |
| CMP + Consent Mode | Compliance Layer |
| GTM + Tags | Signal Execution Layer |
| Network + Cookies | Transport Layer |
| GA4 + CDP | Analytics Layer |
| RCA System | Intelligence & Recovery |

---

## 🧠 Why This Matters

- Shows **where** signals break and **why**
- Helps **CxOs** map signal failures to lost revenue
- Equips **architects** to build leak-proof systems
- Turns debugging into **strategic system design**

---

## 💡 Bonus Insight

“The most expensive leaks don’t show up in your error logs.  
They hide in your attribution, trust, and consent pipelines.”

---

## 📁 Location

This architecture is visualized as both live Mermaid code (above) and downloadable PNGs inside:

`/visuals/architecture/`

For diagram variants, check:  
`/use-cases/10-zero-leak/RCA-01/visuals/`
