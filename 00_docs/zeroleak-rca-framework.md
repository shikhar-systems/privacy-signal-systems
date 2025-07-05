# 🧠 ZeroLeak RCA™ Framework

This document explains the **ZeroLeak RCA™** methodology — a system-resilient framework for tracing, understanding, and resolving digital signal failures across consent, cookies, tags, and network layers.

---

## 🔄 RCA Lifecycle Flow

```mermaid
flowchart TD
    A[User lands on site] --> B[Consent Banner Shown]
    B -->|Accepts| C[Consent Captured in CMP - OneTrust or CookieYes]
    C --> D[GTM Fires Tags Based on Consent]
    D --> E[Signals Sent to GA4, Ads, Pixels]
    E --> F[Data Logged in GA4 / BigQuery / CDPs]
    F --> G[Signal Quality Evaluated]
    G --> H[ZeroLeak RCA™ Detects Silent Failures]
    H --> I[Recovery Pattern Matched & Applied]
```

---

## 🔍 RCA Depth Flow (From User to Signal Recovery)

```mermaid
graph TD
    A[User Action → Click/View/Submit]
    B[Tag Triggered via GTM]
    C[Consent & Cookie Check]
    D[DataLayer Value Check]
    E[Network Request Sent]
    F[Data Captured in GA4 / Ads / CDP]
    G[Signal Appears in Report?]
    G -->|No| H[ZeroLeak RCA™ Triggered]
    H --> I[Consent · Cookie · Tag · Network Diagnosis]
    I --> J[Recovery Action Suggested or Implemented]
    A --> B --> C --> D --> E --> F --> G
```

---

## 🛠️ Why This Framework

- Tags may fire, but **signals may silently drop** due to consent, cookie, or dataLayer gaps.
- Traditional QA checks often **miss root-cause chains** behind broken journeys or misattributed conversions.
- ZeroLeak RCA™ introduces a **multi-layered, system-first debugging model**.

---

## 💎 Key Features

- Consent-respecting and signal-aware
- Cross-layer (CMP → GTM → GA4 → BigQuery → Report)
- Business-resonant RCA — connects tech to impact
- Designed for analysts, engineers, and growth leaders
- Pluggable into existing QA & audit ecosystems

---

## 📌 Outputs

- Architecture Diagram (Mermaid → PNG)
- Root Cause → Signal Path Mapping
- Leadership RCA Summary
- Monetization Risk View
- Persona & Industry Impact Snapshot
- Recovery Checklist & Verification Logic

---

> “We don’t debug tags. We repair truth.”
