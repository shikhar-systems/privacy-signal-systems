# 🎯 UTM Lost Due to Interstitial or Captcha Pages

This issue was seen in security-first flows where interstitials (e.g., Cloudflare, CAPTCHA, age-gates) cause UTM parameters to be dropped before analytics tags load.

---

## 🚨 What Happens

- User comes via UTM-tagged ad link
- Redirect to interstitial page strips query string
- Final landing page shows `(not set)` in GA4 reports

---

## 💣 Why It’s a Problem

- Campaign ROAS gets misreported
- Paid marketing budgets get reallocated incorrectly
- Ad platforms under-attribute or overcharge

---

## ✅ What Was Done

- Stored UTM on first touch in cookies/localStorage
- Rehydrated them on final load via JS
- Also pushed to dataLayer on confirmation

---

## ⏳ RCA Potential

Strong candidate for a “Campaign Attribution RCA Stack”
