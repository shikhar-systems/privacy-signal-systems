# 🧾 Glossary — ZeroLeak RCA™

This glossary defines key terms used across the **ZeroLeak RCA™** framework, GitHub documentation, and Root Cause Analysis (RCA) flows.

It ensures clarity for readers from cross-functional backgrounds — executives, product owners, analysts, engineers, and compliance teams.

---

## 📚 Key Terms

| Term | Definition |
|------|------------|
| **ZeroLeak RCA™** | A privacy-first, real-world Root Cause Analysis system that dissects silent signal failures across digital stacks. |
| **Signal** | A unit of traceable digital behavior (clicks, form submits, purchases, etc.) collected for analytics, marketing, or compliance. |
| **Signal Leak** | A loss, delay, or distortion in expected signal flow due to consent, cookie, tag, or code issues. Often invisible in dashboards. |
| **Consent Mode** | A system (e.g., OneTrust, CookieYes) that governs data collection based on user consent — blocking or enabling tracking behavior. |
| **Tag Misfire** | When a tag (e.g., Google Ads, Meta Pixel) fires at the wrong time, on the wrong page, or with wrong data — creating attribution gaps. |
| **Attribution Mismatch** | When signal flow breaks between systems (Ads ↔ Analytics ↔ CRM), resulting in fragmented user journeys and unreliable metrics. |
| **RCA Loop** | A single, closed diagnostic and resolution cycle for a signal failure — including bug, impact, fix, and documentation. |
| **Architecture-Level Failure** | A signal issue caused not by isolated bugs, but by gaps in cross-stack design (e.g., misaligned dataLayer, redirect logic, or multi-tag conflicts). |
| **System-First Thinking** | Approach where RCA is not just about debugging, but diagnosing systemic flaws and realigning trust infrastructure. |
| **PulseGrid** | Internal RCA execution tracker (used privately for prioritization, tracking, visibility). |

---

## 🧠 Bonus Insight

The language of RCA is evolving — this glossary reflects the *ZeroLeak* shift from surface bugs to **invisible architectural trust failures**.

