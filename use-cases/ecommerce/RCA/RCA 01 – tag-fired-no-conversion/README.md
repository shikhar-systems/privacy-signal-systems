# 🎯 RCA 01 – Tag Fired but No Conversion Recorded

## 📌 Summary

The tag fired successfully on the Thank You page. GTM preview mode confirmed the trigger fired.  
Network tab showed a status 200 response. Yet the vendor reported no conversions received.

---

## 🧠 Root Cause

- ✅ GTM trigger conditions were met and tag fired
- ✅ Network request appeared with 200 status
- ❌ Custom HTML tag lacked required dynamic parameters
- ✅ Template-based tag worked because it auto-filled required fields

---

## 🔍 Investigation Steps

- Reviewed GTM firing rules and trigger match
- Inspected DevTools → Network tab for request payload
- Compared HTML tag vs working template-based version
- Cross-verified vendor platform logs (zero events received)

---

## 🧱 Fix Applied

- Removed custom HTML tag
- Replaced with official vendor template
- Re-tested with preview, real conversions, and tag diagnostics

---

## ✅ Outcome

- Conversions began reflecting within 1 hour of template switch
- Prevented further loss of tracking from high-value campaign

---

> “Just because a tag fires doesn’t mean data lands.”
