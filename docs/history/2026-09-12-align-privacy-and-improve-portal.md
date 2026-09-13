# Align privacy policy and improve portal structure

Date: 2026-09-12

## Changes

- Removed the commented AdSense script template from `privacy.html`; the Privacy page no longer contains advertising code or a Publisher ID.
- Defined the policy scope as `naorex.link` and site-operated subdomains, including Luck Wealth Simulator.
- Distinguished the Simulator's current AdSense tag from possible future advertising on other pages.
- Clarified Cookie use, Google's data use and personalized-ad controls, hosting logs, Google Fonts, external links, and browser-side Simulator processing without claiming that an analytics product is in use.
- Replaced the unsupported claim that the GitHub profile provides a contact method with an honest pending-form notice and routed `about.html` to the Privacy contact section.
- Reworked `index.html` into a site-purpose hero, a full-width Featured App explanation, a short About section, and the existing About/Privacy/GitHub footer.
- Added concrete Simulator capabilities and retained separate links to the detailed guide and live app, with the guide as the primary action.
- Preserved the Garden theme, existing navigation and footer, and static HTML/CSS architecture while updating the Hallmark project history.
- Updated `README.md` to match the current advertising, Privacy, contact, and portal behavior.

## Source reviewed

- Reviewed the repository HTML, CSS, README, sitemap, and existing project history.
- Reviewed the deployed `https://naorex.link/privacy.html` and `https://luck-wealth-simulator.naorex.link/` responses on 2026-09-12.
- Confirmed that the deployed Simulator loads an AdSense tag, while the portal repository does not contain active advertising or analytics code.
- Checked Google's AdSense required-content guidance and partner-site data-use explanation when revising the policy wording.

## Verification

- Parsed all four HTML files and checked 38 local links and anchors, all referenced CSS variables, the Hallmark JSON log, and `sitemap.xml`.
- Confirmed that `privacy.html` contains no AdSense script, Publisher ID, `adsbygoogle` marker, or Google Analytics assertion.
- Confirmed that the revised portal contains the required Hero, Featured App, About, and footer content, with no Coming Soon copy, empty card, phantom page link, or advertisement.
- Served the site locally and received HTTP 200 responses for the home, Privacy, About, and Luck Wealth Simulator guide pages.
- Rendered and visually reviewed the home page at desktop and mobile sizes and the Privacy page at mobile size.
- Checked the home and Privacy layouts at 320, 375, 414, 768, 1280, and 1920 CSS pixels; no horizontal overflow, out-of-viewport element, or wrapped navigation/action affordance was found.
- Confirmed WCAG AA contrast for core text and controls; measured ratios ranged from 4.24:1 for the focus indicator to 16.82:1 for primary text.
- Ran the Hallmark slop, honesty, chrome, token, responsive, icon, and mobile gates with passing results for the implemented surface.
- The external inquiry-form URL remains the only unmet completion item because it has not yet been provided.

## Follow-up required

- Replace the pending-form notice in `privacy.html` with the real external inquiry form link after its public URL is provided.
- Do not treat the contact-method completion criterion as satisfied until that URL is present and reachable.
