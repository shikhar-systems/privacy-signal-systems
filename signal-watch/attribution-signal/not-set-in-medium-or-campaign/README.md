# 🎯 RCA Candidate – `(not set)` in GA4 Medium or Campaign

One of the most silently destructive attribution bugs in modern marketing analytics.  
`(not set)` appears in `session_medium`, `session_campaign`, or `source` fields — and erases the ability to track ROI.

---

## 🚨 What’s Going Wrong

This issue typically shows up when:

- UTMs are dropped during redirect (e.g., vanity → destination)
- Tags overwrite UTM parameters before GA4 reads them
- GTM fires too late due to heavy consent layers or slow DOM

Most common environments:

- Branded/shortened URLs (e.g., mysite.link/deal → mysite.com)
- Third-party tools or CRMs inserting interstitials
- Single Page Apps with reload or hashchange quirks

---

## 💣 Why It Matters

- Attribution blind spots — marketing ROI vanishes
- Channel optimization breaks — media spend looks wasted
- GA4 reports become misleading — decision-makers lose trust

---

## 🛠️ What We Built to Catch & Prevent It

- ✅ A **Real-Time UTM Validator** (custom JS + GTM Lookup Table)
- ✅ A **UTM Fallback Mechanism** (preserves values via cookie/sessionStorage)
- ✅ **Tag Assistant alerts** when `utm_campaign`, `utm_medium`, or `source` is missing

---

## ⏳ RCA Promotion Status

This issue has been promoted into formal RCA investigation under:

📁 `/use-cases/ecommerce/RCA/03-not-set-campaign-medium/`

(If not yet published, it’s tracked in `/RCA-BACKLOG.md`)

---

> “If attribution dies at the source, even perfect dashboards are lies.”
