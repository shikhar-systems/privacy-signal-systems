# RCA 03: Tag Fired on Wrong Page – Intent Break

> When the signal fires, but the intent doesn’t match.

This RCA investigates a common but critical failure: a tag fired on the wrong page, leading to broken analytics intent, misattributed performance, and poor user targeting.

We identify the root cause, simulate the bug, and share a safer dataLayer-based solution.

🔧 RCA Category: **Intent Signal Break**  
📊 Impacted Layer: **Trigger Logic + Tag Execution**  
🧠 Solution: Use `dataLayer.pageType === 'thank-you'` for reliable targeting

➡️ For executive summary, see [`leadership-summary.md`](./leadership-summary.md)
