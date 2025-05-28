# 🧩 GTM–GA4 Signal Break Use Cases

This folder contains use cases where signal integrity breaks between Google Tag Manager (GTM) and Google Analytics 4 (GA4). These are direct causes of revenue leakage, misattribution, inflated events, or broken funnels — all traced through Root Cause Analysis (RCA).

---

## 🛠️ RCA Category

**Type:** Technical signal transmission failure  
**Stack:** GTM + GA4 + client-side routing + DOM interaction  
**Symptoms:** Inaccurate event data, session inflation, attribution loss

---

## 🎯 Use Cases in This Folder

| Folder Name                    | Summary |
|--------------------------------|---------|
| `not-set-campaign-medium/`     | UTM/referrer lost → `(not set)` in GA4 source/medium |
| `duplicate-pageview-spa/`      | SPA navigation triggers multiple `page_view` events in GA4 |

---

## 📊 Why These Matter

- Affect paid marketing spend attribution (Google Ads, Meta)
- Misguide growth and conversion rate decisions
- Break trust in session, funnel, and user journey reports

---

## 🔍 RCA Contents

Each use case includes:

- `README.md` — public summary  
- `architecture.md` — consent → signal → RCA mapping *(available on request)*  
- `impact.md` — how much money or trust is lost *(available on request)*  
- `solution.md` — system fix, not patch *(available on request)*

---

> “Broken signals don't just hurt data — they break decision-making. These RCAs fix them at the root.”
