# Add inquiry form

Date: 2026-09-15

## Changes

- Replaced the pending inquiry-form notice in `privacy.html` with the published Google Forms link.
- Documented that the form uses Google Forms and that the submitted inquiry category, email address, and inquiry details are used to handle the inquiry and make necessary contact.
- Updated the Privacy policy's last-updated date to September 15, 2026.
- Added an `お問い合わせ` footer link on every published HTML page, routing visitors through `privacy.html#contact` before they open the external form.
- Reused the existing button, focus, interaction, spacing, and Garden-theme styles without changing `styles.css` or `tokens.css`.
- Kept `sitemap.xml` unchanged because no new public page or route was added.

## Documentation

- Checked `README.md` as required for the public-behavior change.
- Updated its Privacy policy section because the previous text said the form URL was still pending.
- Recorded the active form URL, the centralized Privacy-page route, and the requirement to keep the policy aligned with future changes to form fields or their purposes.
- Kept this repository-specific contact configuration in local documentation; Shared Knowledge was not changed.

## Verification

- Confirmed that `https://forms.gle/AsNeetvYUisTbYwm9` redirects to a published Google Form and returns HTTP 200.
- Confirmed the public form title and the visible fields for inquiry category, email address, and inquiry details.
- Parsed all five HTML pages and verified every local link and fragment target, including each footer's contact link.
- Verified the exact external form URL, `target="_blank"`, and `rel="noopener noreferrer"`, and confirmed that no pending-form copy remains.
- Served the site locally and received HTTP 200 responses for all five HTML pages, `styles.css`, and `tokens.css`.
- Rendered all five pages at 320, 375, 414, and 768 CSS pixels. Confirmed no horizontal overflow and no wrapped contact button or footer-link labels.
- Confirmed that `#contact` is visible after fragment navigation at every tested width.
- Visually reviewed the Privacy page at mobile and tablet widths and retained the existing editorial hierarchy and Garden theme.
- Ran the applicable Hallmark honesty, chrome, token, responsive, mobile, and accessibility gates for the changed surface with no failures.
- Ran `git diff --check` successfully.
