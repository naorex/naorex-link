# Fix inquiry button text contrast

Date: 2026-09-20

## Changes

- Fixed the Privacy page's inquiry-form CTA so its text remains the light button-foreground color instead of inheriting the dark-green link color.
- Excluded `.button` links from the Privacy page's normal and hover-only link color rules.
- Checked `README.md`; no update was needed because the inquiry route, form provider, and site behavior documented there did not change.

## Verification

- Served `privacy.html`, `styles.css`, and `tokens.css` locally and confirmed HTTP 200 responses.
- Used Chromium's computed styles to confirm the CTA text is `oklch(0.98 0.004 115)` while its background is `oklch(0.43 0.09 158)`.
- Ran `git diff --check` successfully.

## Knowledge routing

- This is repository-specific visual behavior, so the decision remains in the repository. Shared Knowledge was not changed.
