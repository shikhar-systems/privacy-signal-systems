# ♻️ Signal Recovery Playbook

This playbook outlines **how to rebuild broken signal journeys** once root cause is identified using ZeroLeak RCA™.

Unlike traditional fixes that patch a tag or tweak a trigger, this recovery process focuses on **system-level repair** — ensuring the **next signal doesn’t just fire, it flows with integrity**.

---

## 🧭 Recovery Strategy Overview

Every signal recovery involves three phases:

1. **Root Clarity**  
   Map the exact failure: where the signal dropped, why, and under what system conditions.

2. **Trustful Redesign**  
   Modify tag logic, dataLayer behavior, sequencing, or consent integration to prevent recurrence.

3. **Replay + Confirm**  
   Use simulated flows to re-trigger the journey and **validate end-to-end signal delivery**.

---

## 🔄 Key Recovery Techniques

| Technique | When to Use |
|----------|-------------|
| `Trigger sequence delay` | When tags fire before required dataLayer push |
| `Consent check listener` | When consent wasn’t resolved before tag load |
| `Cookie readiness guard` | When signals rely on third-party cookies |
| `Redundant endpoint fallbacks` | For ad blockers or redirect-based failures |
| `Custom signal attribution bridge` | For identity split across GA4/Ads/Facebook |

---

## 🧰 Tools Used

- **Browser DevTools** (console, network, cookies)
- **Tag debuggers** (Google Tag Assistant, DataLayer Inspector+)
- **Consent scanners** (OneTrust Debugger, CookieYes Preview)
- **Custom scripts** (to simulate delayed or failed conditions)

---

## 📉 Before Recovery (Common Symptoms)

- Tag fired, but **no network call visible**
- Network call fired, but **no conversion in vendor dashboard**
- GA4 shows event, but **Ads or Meta doesn’t**
- Signal blocked in **Safari or Brave** but not Chrome
- Metrics inconsistent across tools (GA4, CRM, Ads)

---

## ✅ After Recovery (What Success Looks Like)

- Signal fires **only after consent is granted and cookies are ready**
- Network payloads carry **complete, valid data**
- Attribution IDs match across systems
- Vendor dashboards show **synced events**
- CXOs and Product Leads gain **visibility and trust** in data

---

> “We don’t fix signals just to report.  
> We recover them to restore system truth.”

---

📎 All reusable logic templates can be found in: `/patterns/`  
📂 Real-world examples implemented inside: `/10-zero-leak/`
