# 🧠 Logic Explainer – RCA 02: Redirect Blocking Cookie Sync

This Root Cause Analysis addresses a hidden redirect issue that broke identity sync for a 3rd-party marketing pixel. Although the tag fired in GTM, vendor-side conversions failed due to an unnoticed redirect layer that stripped identity parameters. This RCA documents how the issue was detected, diagnosed, and fixed.

---

## 🔍 Root Cause Summary

- A Custom HTML tag was configured in Google Tag Manager to fire a 3rd-party vendor pixel on the `/thank-you` page.
- The pixel appeared to fire successfully, but no conversions were recorded in the vendor dashboard.
- Investigation revealed a **307 Temporary Redirect** occurring before reaching the final pixel endpoint.
- This redirect layer (e.g. Mimecast or another security gateway) stripped query parameters required for identity sync.
- As a result, the vendor failed to capture cookies or associate the visit with a known user.

---

## 🎯 GTM Logic Summary

| Element               | Configuration                                                  |
|------------------------|----------------------------------------------------------------|
| **Tag Type**           | Custom HTML (3rd-party marketing pixel)                        |
| **Trigger Type**       | Page View                                                      |
| **Trigger Condition**  | Page Path contains `/thank-you`                                |
| **Consent Control**    | Fires only after Performance Consent = `true` (via OneTrust)   |
| **Pixel Endpoint**     | Initially routed via secure proxy (307 redirect)               |
| **Final Fix**          | Updated to direct 302 endpoint (no redirect)                   |
| **Outcome**            | Identity preserved → cookie sync successful → conversion recorded |

---

## 🛠️ Observed Behavior (Before Fix)

- GTM tag fired correctly on the expected page.
- Network tab in DevTools showed a **307 redirect** from a security layer.
- Final pixel endpoint was reached but without the required identity parameters.
- Application tab showed **no cookie set** by the vendor.
- Conversion data was not captured or reflected in vendor analytics.

---

## ✅ Resolution Logic

- Redirect was identified as the root cause through browser network analysis.
- Tag was updated to use the **direct endpoint** (bypassing redirect layer).
- This change prevented query string stripping and allowed vendor to receive the full payload.
- Cookie was successfully set and identity was synced.
- Conversion tracking resumed as expected.

---

## 📸 Screenshots

The following screenshots have been added to this folder:

- `screenshots/gtm-tag-summary.png` – GTM trigger and tag logic summary
- `screenshots/network-before.png` – Network call showing 307 redirect
- `screenshots/network-after.png` – Successful direct call with 302 and cookie set
- `screenshots/consent-status.png` – Consent condition matched (Performance = true)

---

## 🧠 System Architecture

The following diagram illustrates the architecture flow from user action to vendor sync, highlighting where the redirect broke the chain and how the fix reestablished cookie syncing.

📎 ![System Architecture - RCA 02](../architecture/system-flow-RCA02.png)

> Covers: Consent gating → GTM trigger → pixel fire → redirect layer → fix → successful sync

---

## 🧾 Key Takeaways

- Even when a pixel "fires," network inspection is critical to confirm parameter integrity.
- Redirect layers can silently strip identifiers, breaking attribution and costing revenue.
- GTM logic must always be tested with live consent flows + browser tools.
- Fixes must ensure payload reaches the vendor unmodified and at the right time.

---

## 🎥 Loom Video

A Loom walkthrough will soon be added, covering:

- Consent flow validation  
- GTM trigger logic  
- Network debugging  
- Before vs after fix behavior

📎 Video placeholder: `video/rca-02-redirect-cookie-sync.mp4`
