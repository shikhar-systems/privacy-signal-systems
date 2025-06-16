# 📉 Impact – Silent Drop in Conversion Attribution

### 🎯 What Went Wrong:
- The pixel fired visually and logged a 307 response.
- However, the redirect **stripped cookie headers** due to the security proxy (Mimecast).
- As a result, no user identity was passed to the vendor.

### 🔍 Why It Mattered:
- Conversions **were not attributed** back to campaigns.
- Analytics and performance metrics showed an artificial drop.
- Campaign effectiveness appeared **underreported**.
- Identity sync failure led to **retargeting inefficiencies**.

### 💡 Real-World Implication:
> A redirect can silently break identity sync without triggering any error in the GTM or browser logs — causing revenue-impacting attribution loss.
