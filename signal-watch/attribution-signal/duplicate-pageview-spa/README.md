# 📄 Duplicate Pageview in SPA (Single Page Application)

This issue was observed in Single Page Applications where route changes triggered GA4 `page_view` events multiple times without a real page reload.

---

## 🚨 What Happens

- User clicks to navigate within the app (e.g., from Home to Product page)
- SPA router updates URL but does not reload the page
- GTM/GA4 `page_view` tag fires again — often twice or more
- Session duration and bounce rate data becomes distorted

---

## 💣 Why It’s a Problem

- Inflated session counts and pageviews in GA4
- Campaign performance looks better than it is
- Funnel analysis misleads product, analytics, and growth teams

---

## 🧠 Observed Context

I encountered this during implementation audits for ecommerce SPAs using React and Vue, where pageview tracking was attached to `historyChange` but not properly de-duplicated.

---

## ⏳ RCA Potential

This is now tracked for RCA escalation under:
📁 `/use-cases/ecommerce/gtm-ga4-signal-break/duplicate-pageview-spa/`
