# 🔒 Login Page Pixel Fire

This issue was observed during login flows where tracking pixels (e.g., Meta or GA4) were firing before or during user authentication screens.

---

## 🚨 What Happens

- Login or OTP screen triggers `PageView` or `Lead` events
- Happens due to universal tag or hardcoded pixel in SPA templates

---

## 💣 Why It’s a Problem

- Violates user expectations of privacy
- Can be flagged as "surveillance-like" behavior
- Creates audit issues, especially for finance, healthcare, or education domains

---

## ✅ What Was Done

- Audited GTM templates and moved tags under conditional triggers
- Implemented custom triggers based on login route exclusion logic
- Validated via GA4 DebugView and Meta Events Manager

---

## ⏳ RCA Potential

May escalate if found across journeys like registration, payments, or contact forms.
