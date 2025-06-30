# RCA-01: Tag Fired on Form Submit Page Before User Submission

## Summary
A tag meant to fire after form submission was incorrectly firing on page load, before the user actually submitted the form. This caused false conversion reporting.

## Signal Category
- trust-signal
- intent-integrity

## Status
✅ Fixed (Tag sequencing corrected)

## Fix Summary
Switched from a "Page View - Contact Page" trigger to a "Form Submission Success" trigger to ensure the signal is real.

## Screenshot
See `screenshots/contact-form-submit-event-fire--before.png`
