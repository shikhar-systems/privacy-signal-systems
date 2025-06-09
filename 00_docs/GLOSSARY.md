# 📚 GLOSSARY — Signal Systems & RCA Terminology

This glossary supports strategic clarity for all collaborators — from product and compliance to engineering and data science. These terms appear across the RCA library, `signal-watch/` folders, and system-level diagnostics.

---

## 🔁 Signal System Terms

| Term              | Definition                                                                 |
|-------------------|---------------------------------------------------------------------------|
| **Signal**        | Any user, device, or platform behavior converted into a data point — e.g., click, view, opt-in, conversion. |
| **Broken Signal** | A signal that is delayed, suppressed, overwritten, or misclassified — often silently. |
| **Consent Signal**| The metadata emitted by CMPs (Consent Management Platforms) to reflect user privacy choices — can be delayed or contextually invalid. |
| **Trust Signal**  | A platform action that users interpret as fair, private, and expected — even if technically compliant, misalignment can break trust. |
| **Attribution Signal** | Data points used to track where a user came from — source, medium, campaign, etc. Loss or distortion of these disrupts ROI visibility. |

---

## ⚙️ RCA-Specific Terms

| Term               | Definition                                                                 |
|--------------------|----------------------------------------------------------------------------|
| **RCA (Root Cause Analysis)** | The process of isolating systemic failures causing data loss, platform bugs, or legal risk — with reproducible findings. |
| **RCA Promotion**  | When a signal anomaly is validated, mapped to impact, and elevated into a full RCA use case. |
| **Silent Failure** | A bug or misfire that doesn’t produce console errors or alerts — but damages data quality or business insight. |
| **System-linked Issue** | A problem that originates from architecture or logic layers — not just UI or implementation. |

---

> “A system-first thinker doesn’t chase errors — they follow broken signals to root truths.”
