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

This was encountered during implementation audits for ecommerce SPAs using React and Vue,  
where `page_view` tracking was attached to router events like `historyChange` or `popState`  
without logic to prevent duplicate firing.

---

## 🧩 Suspected Root Cause

Pageview event is bound to SPA router changes (`historyChange` or `popState`) without deduplication.  
There is no check for:
- Same path as previous view
- Already-fired flag
- Elapsed minimum time

This is common in setups using built-in GA4 tag templates in GTM without custom debounce control.

---

## ⏳ RCA Potential

This is now tracked for RCA escalation under:  
📁 `/use-cases/ecommerce/gtm-ga4-signal-break/duplicate-pageview-spa/`

---

> “One click. Two pageviews. Zero trust in your session data.”