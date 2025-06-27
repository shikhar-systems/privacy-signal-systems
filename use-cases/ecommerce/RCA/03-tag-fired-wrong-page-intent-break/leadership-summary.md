## Executive Narrative (≈ 90 sec)

**Symptom** — Conversions spiked across every channel.  
**Root Cause** — Regex trigger `Page Path matches ^/summary/order-received/` fired a Google Ads conversion tag on *all* pages.  
**Cost** — Ad budgets shifted toward false winners (**$1 500 in 24 h**).  
**Fix** — Restricted trigger strictly to `/order-received`, re-processed seven days of Ads data.  
**Result** — MLRI 72 → 3, attribution integrity restored.

> “Guessing doesn’t scale. Signal does.” – Shikhar 2.0
