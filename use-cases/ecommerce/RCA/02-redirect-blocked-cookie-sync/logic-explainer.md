# 🧠 Logic Explainer – RCA 02: Redirect Blocking Cookie Sync

This Root Cause Analysis documents how a hidden redirect (307 Temporary Redirect) broke identity sync for a 3rd-party marketing pixel. While the tag fired successfully in GTM, the vendor failed to record any conversions. This RCA outlines how the issue was diagnosed using browser tools and resolved through a direct endpoint fix.

---

## 🔍 Root Cause Summary

- A **Custom HTML tag** was deployed via GTM on the `/thank-you` page.
- The tag fired successfully, but conversions were **not visible in the vendor dashboard**.
- Browser DevTools revealed a **307 redirect**, triggered by a security-layered URL (Mimecast-like).
- This redirect **stripped identity parameters and cookies** before reaching the final endpoint.
- As a result, identity sync failed silently.

---

## 🎯 GTM Logic Summary

| Element               | Configuration                                                  |
|------------------------|----------------------------------------------------------------|
| **Tag Type**           | Custom HTML (3rd-party vendor pixel)                           |
| **Trigger Type**       | Page View                                                      |
| **Trigger Condition**  | Page path contains `/thank-you`                                |
| **Consent Control**    | Fires only if **Performance Consent = true** (via OneTrust)    |
| **Initial Behavior**   | 307 redirect → proxy-stripped payload                          |
| **Fix Applied**        | Direct 302 endpoint (no redirect)                              |
| **Outcome**            | Identity preserved → Cookie sync restored → Conversion tracked |

---

## 🛠️ Observed Behavior (Before Fix)

- GTM tag fired correctly on trigger condition.
- Network tab showed a **307 redirect** midstream.
- Final pixel endpoint received request with **missing identifiers**.
- Application tab: Cookie **not set** by vendor domain.
- Vendor: **No conversion or event data** recorded.

---

## ✅ Resolution Logic (After Fix)

- Pixel URL was updated to **direct vendor endpoint** (no intermediate hop).
- DevTools confirmed response code: **302 Found**  
- `Set-Cookie` headers were preserved.
- Vendor successfully registered **conversion events**.

---

## 📸 Included Screenshots

| Screenshot | Description |
|------------|-------------|
| `network-before.png` | 307 redirect interrupting pixel |
| `network-after.png` | Direct call (302) with cookie set |

🗂 Additional GTM and consent screenshots were skipped for privacy and clarity.

---

## 🧭 System Architecture Overview

📎 `system-architecture.png`  

The diagram shows end-to-end flow:## 🧠 System Architecture

The following diagram illustrates the architecture flow from user action to vendor sync, highlighting where the redirect broke the chain and how the fix reestablished cookie syncing.

📎 ![System Architecture - RCA 02](../architecture/system-flow-RCA02.png)

> Covers: Consent gating → GTM trigger → pixel fire → redirect layer → fix → successful sync

---

---

## 🧾 Key Takeaways

- Pixels may “fire” but **still silently fail** due to redirect stripping.
- 307 redirect via secure proxy layers can **break attribution and identity resolution**.
- GTM setups must be validated using **DevTools + consent checks**.
- Redirect-free endpoint routing ensures successful cookie sync and downstream analytics.

---

## 🎥 Loom Video

_Loom video walkthrough is not included for this RCA, as the core behavior is clearly demonstrated through network tab screenshots and documentation.
