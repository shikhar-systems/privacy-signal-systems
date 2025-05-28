# 🎯 `not set` in Medium or Campaign (GA4/GTM)

This is one of the most common attribution bugs that we observed across multiple digital products during previous roles.

---

## 🚨 What Happens

- `(not set)` appears in `session_medium`, `session_campaign`
- Occurs when UTMs are dropped, overwritten, or delayed
- Seen on redirects, vanity URLs, or incorrect GTM triggers

---

## 💣 Why It’s a Problem

- Wipes out campaign-level attribution
- Marketing teams can’t justify spend
- Analytics funnels lose source clarity

---

## ✅ What Was Done

- Built real-time “UTM validator” inside GTM to catch live loss
- Created fallback logic to preserve first-touch UTMs in cookie
- Added alert in Tag Assistant if UTMs dropped before event

---

## ⏳ RCA Potential

This forms the foundation of the full RCA use case:  
📁 `/use-cases/ecommerce/gtm-ga4-signal-break/not-set-campaign-medium`
