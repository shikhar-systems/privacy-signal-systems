### Leadership Summary

**What went wrong:**  
Conversion tag was firing prematurely on page load rather than after actual form submission.

**Impact:**  
False positives in conversion tracking, misattributing intent. This could mislead leadership about actual lead quality and user journey effectiveness.

**Fix:**  
GTM trigger modified to only fire upon form submission success (`gtm.formSubmit`) using visibility or event listener logic.

**Visibility Gain:**  
Signals that conversion truly happened, increasing CXO trust in reporting accuracy.

**RCA Type:**  
Intent Breakage via Trigger Misfire