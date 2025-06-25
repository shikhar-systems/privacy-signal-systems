## Leadership Summary

- **Problem:** A conversion tag failed silently due to a 307 redirect that broke cookie sync.
- **Impact:** Agency-side conversions were not recorded — even though the tag fired.
- **Root Cause:** Redirect prevented key cookies from being exchanged, blocking attribution.
- **Fix:** Identified redirect behavior, switched to a more stable pixel placement + endpoint.
- **Lesson:** Successful tag fire ≠ successful signal delivery. Cookie sync failures are invisible yet critical.
