# 🔒 Login Page Pixel Fire

This issue captures a privacy-compromising behavior where **tracking pixels fire on login or authentication screens** — often unintentionally.

---

## 🚨 What Happens

- User lands on **Login** or **OTP verification** screen
- Pixels (e.g., Meta PageView, GA4 events) fire before authentication
- Caused by:
  - Hardcoded tracking pixels in SPA templates
  - Universal GTM triggers without route-level exclusion

---

## 💣 Why It’s a Problem

- Breaks user expectations of **confidentiality during authentication**
- May be interpreted as **surveillance** by users, media, or regulators
- Triggers **audit flags** in finance, healthcare, education, and public sector platforms
- Violates principles of **minimization** and **contextual integrity**

---

## ✅ What Was Done

- Audited GTM setup and removed universal triggers
- Added route-based conditional logic to defer pixel firing
- Validated behavior using:
  - ✅ GA4 DebugView  
  - ✅ Meta Events Manager  
  - ✅ Tag Assistant recordings on auth routes

---

## ⏳ RCA Potential

Strong candidate for escalation under:
📁 `/use-cases/ecommerce/trust-signal/login-page-pixel-fire/`  
Especially when combined with similar issues in:
- Registration flows  
- Checkout/payment gateways  
- Sensitive user action screens

---

> “Trust isn’t broken by pixels — it’s broken by *where* they fire.”