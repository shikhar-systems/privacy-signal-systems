
# 📘 ZeroLeak RCA™ Glossary

A shared vocabulary ensures precision when discussing complex signal systems.  
This glossary defines key terms used across the ZeroLeak RCA™ framework and signal integrity investigations.

---

## 🧩 Core Concepts

- **ZeroLeak RCA™**: A signal-first root cause analysis framework designed to detect and resolve silent tracking failures across consent, cookies, GTM, and analytics platforms.
- **Signal Leak**: Any instance where user intent fails to generate a complete, accurate signal in your reporting tools (e.g., GA4, Ads, CDP).
- **Consent Mismatch**: When consent settings (e.g., via CMP tools like OneTrust) do not align with actual tag behavior, resulting in blocked or false signals.
- **Cookie Sync Failure**: Breakdown in the process of syncing identifiers (like client ID or user ID) across tags, systems, or domains.
- **Tag Misfire**: A tag firing at the wrong time, on the wrong page, or under broken trigger logic.
- **Network Interruption**: Redirection errors (307, 302), server downtime, or blocked requests that prevent signal transmission.

---

## 🛠️ System Layers

- **CMP (Consent Management Platform)**: A tool like OneTrust or CookieYes that manages user consent collection and enforcement.
- **GTM (Google Tag Manager)**: A tag orchestration system for managing triggers, variables, and third-party scripts.
- **GA4 (Google Analytics 4)**: Google’s analytics platform, often used as the core reporting destination for behavioral data.
- **CDP (Customer Data Platform)**: A system that aggregates, unifies, and activates user data across platforms (e.g., Segment, mParticle).
- **Tag Template**: A prebuilt or custom configuration inside GTM used to fire tracking pixels or scripts.
- **DataLayer**: A JavaScript object in the browser that stores structured data used by GTM to trigger tags or pass parameters.

---

## 🔍 Debug & RCA

- **Debug Mode**: Special GTM/GA4 mode used to inspect tag behavior in staging or production environments.
- **TRID**: Tracking Request ID — a unique identifier for validating signals across systems.
- **Signal Path**: The full journey of a user action → tag trigger → data layer → request → reporting.
- **Attribution Loss**: The breakdown in mapping user activity to the correct source/medium/campaign.
- **RCA Loop**: A step-by-step analysis that identifies failure origin, propagation, and recovery.

---

## 🧠 Metadata & Strategy

- **PulseGrid**: An internal execution tracker used to manage and classify active RCA cases.
- **CXO-Tier**: RCA loops designed for leadership consumption — mapping ROI, risk, and redesign decisions.
- **System Zone**: Logical segment of a signal path (e.g., Consent Zone, Trigger Zone, Request Zone, Report Zone).

---

> Use this glossary when interpreting public RCA loops, GitHub documentation, or strategic discussions.
