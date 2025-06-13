# 🔍 GTM Logic Explainer

## Trigger Setup
- Page View – Consent Given (Performance Category)
- URL Match: `/thank-you` page
- Consent framework: OneTrust

## Tag Type
- Custom HTML tag firing 3rd-party pixel URL

## Observed Behavior
- Tag fired via GTM as expected
- Network tab showed 307 redirect
- Application tab showed no cookie

## Issue
- Redirect interrupted cookie sync
- Identity not passed downstream to vendor

## Fix Logic
- Updated pixel to direct 302 endpoint
- No intermediate hop → no identity drop
