# 🛰️ signal-watch — Early Signal Drift & RCA Candidates

This folder tracks **early-stage signal integrity issues** — before they graduate into full RCA loops.

It serves as a **signal radar** for engineers, analysts, and system architects to monitor, prioritize, and escalate anomalies across **consent, cookie, network, and AI signal zones**.

---

## 🚧 What Qualifies as a Signal-Watch Item?

- Breaks intent but hasn’t yet triggered a full investigation
- Lacks stakeholder urgency but silently damages attribution or trust
- Inconsistent or edge-case behavior observed in user journey, analytics, or tag flow
- Emerging signal classes — including AI hallucinations, chat signal mismatches, or ID-sync failures

---

## 🔍 Strategic Benefit

Having this layer helps teams:

- Detect signal **drift** before total failure
- Avoid repeating **low-context bug reporting**
- Separate **false alarms** from real architectural leaks
- Maintain a **repeatable RCA loop pipeline** without chaos

---

## 🧭 Signal Categories

| Signal Class     | Folder                     | Description |
|------------------|----------------------------|-------------|
| Consent Signal   | `consent-signal/`          | Triggered or blocked flows due to banner, toggle, or region logic |
| Cookie Signal    | `cookie-signal/`           | Issues from sync gaps, mismatches, or cookie storage failure |
| Trust Signal     | `trust-signal/`            | Misfired tags, accidental triggers, or breach of user intent |
| Attribution ID   | `id-signal/`               | Broken tracking due to mismatched, missing, or recycled IDs |
| AI Signal        | `ai-signal/`               | Drift in chatbot, recommender, or signal injection behavior |
| QA & Predictive  | `qa-signal/`               | Breaks caught via debug mode or predictive mismatch patterns |

---

## ✅ Finalized RCA Use Cases

These issues have now been upgraded to formal RCA loops under the `10-zeroleak/` vault:

| RCA ID | Signal Class       | Title                                                                 |
|--------|---------------------|------------------------------------------------------------------------|
| RCA-01 | Trust Signal        | Tag Fired Before Form Submission — False Conversion Recorded          |
| RCA-02 | Cookie Signal       | Redirect Blocked Cookie Sync — Attribution Loss                       |
| RCA-03 | Trust Signal        | Tag Fired on Wrong Page — Intent Breakage                            |
| RCA-04 | Trust Signal        | Pinterest Tag Fired — But No Signal Captured                         |
| RCA-05 | ID Signal           | Same User, Different ID — Broken Journey Attribution                  |

---

## 🔭 In-Progress Observations (Signal-Watch Candidates)

| Observation ID | Signal Class     | Description |
|----------------|------------------|-------------|
| SW-06          | Consent Signal   | Opt-out toggle delays blocking on Safari vs Chrome                 |
| SW-07          | AI Signal        | Chatbot Hallucination from Malformed Input                         |
| SW-08          | AI Signal        | Personalization Drift After Consent Change                         |
| SW-09          | ID Signal        | Ads vs GA4 Attribution Using Different ID Systems                  |
| SW-10          | Trust Signal     | GTM Debug Mode Left Enabled in Production                          |
| SW-11          | Cookie Signal    | Subdomain Cookie Conflict — Purchase Not Mapped                    |
| SW-12          | Attribution Gap  | Incorrect Currency Sent to Ads — Budget Misreporting               |
| SW-13          | QA Signal        | GTM Container 404 on Blog Subdomain — Tags Missing                 |

> These will be upgraded to RCA loops based on impact, reproducibility, and leadership value.

---

## 🧠 Who Should Use This Folder?

- RCA Architects tracking evolving system fragility
- Growth, Ads, or Analytics teams catching drop-offs without obvious bugs
- AI and Privacy Signal Engineers preparing RCA-ready payloads
- Directors, VPs, and Consultants reviewing system health with context

---

## 📌 Reminder

Only **signal-aware minds** catch these before they explode.  
Signal-watch is where **silent chaos gets scoped** — before it hurts brand, trust, or revenue.
