## Leadership Summary

- **Problem:** A key GA4 tag fired on the wrong page (product page instead of thank-you page).
- **Impact:** Misattributed conversions, inaccurate analytics, loss of team trust.
- **Root Cause:** Trigger conditions were too broad and didn’t validate user journey intent.
- **Fix:** Introduced a more reliable trigger using `dataLayer.pageType === 'thank-you'`.
- **Lesson:** Intent-aligned tracking is critical for budget, analytics, and leadership confidence.
