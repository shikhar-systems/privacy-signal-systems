# 🎯 UTM Loss via Interstitial or CAPTCHA Pages

This use case explores a common attribution failure in **security-first flows**, where interstitial screens disrupt the UTM signal flow before analytics tools can record campaign data.

---

## 🚨 What Happens

- User clicks a UTM-tagged campaign URL
- Redirects through CAPTCHA, Cloudflare, or age-verification pages
- Interstitial does not preserve query parameters
- Final page loads without UTMs → GA4 shows `(not set)` for medium/campaign

---

## 💣 Why It’s a Problem

- Breaks last-touch attribution, misrepresenting performance
- Causes **under-reporting of high-performing ads**
- Misguides **media planning, ROAS optimization**, and budget allocation
- Reduces **trust in data pipelines** for CMOs and growth leaders

---

## 🧠 Root Cause (Strategic View)

- Security or compliance logic interrupts the URL structure
- Final page gets clean URL, but analytics tags miss UTM context
- No fallback mechanism to rehydrate lost parameters

---

## ✅ What Was Done

- **First-touch UTM capture** into cookie/localStorage  
- **JavaScript-based UTM rehydration** on final page load  
- **Push to dataLayer** if UTMs are missing in URL but found in cookie

---

## ⏳ RCA Potential

This case is being escalated into the full RCA loop:  
📁 `/use-cases/ecommerce/gtm-ga4-signal-break/utm-loss-interstitial-captcha/`

It supports a future framework titled:  
🧩 **"Campaign Attribution RCA Stack"** — connecting consent, routing, and signal hydration strategies for enterprise-grade attribution integrity.

---

> “Interstitials protect the platform — but silently break the signal. Attribution RCA fixes that gap with system logic.”