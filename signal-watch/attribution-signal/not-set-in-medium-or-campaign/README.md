# 🎯 `not set` in Medium or Campaign (GA4/GTM)

This is one of the most common attribution bugs observed across ecommerce and digital platforms — and it silently destroys campaign ROI clarity.

---

## 🚨 What Happens

- `(not set)` appears in `session_medium`, `session_campaign`, or `source`
- Typically caused by:
  - UTMs being dropped during redirect
  - UTMs overwritten by misfired tags
  - Delayed GTM trigger on page load
- Frequently seen in:
  - Vanity URLs
  - Third-party clickthroughs
  - Interstitial pages or consent layers

---

## 💣 Why It’s a Problem

- Wipes out critical attribution data in GA4
- Makes it impossible for marketing to justify spend
- Affects funnel analysis, channel optimization, and ROAS tracking

---

## ✅ What Was Done

- Built a **real-time UTM validator** inside GTM (via custom JS + Lookup Table)
- Implemented **fallback logic** to preserve UTMs in cookies across redirects
- Set up **Tag Assistant alerts** to catch when UTMs are missing or overwritten

---

## ⏳ RCA Potential

This bug has been promoted into full RCA form under:

📁 `/use-cases/ecommerce/gtm-ga4-signal-break/not-set-campaign-medium/`

---

> “If attribution dies at the source, even perfect dashboards are lies.”