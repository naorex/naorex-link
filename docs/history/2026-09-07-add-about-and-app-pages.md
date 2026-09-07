# Add About and Luck Wealth Simulator introduction pages

Date: 2026-09-07

## Changes

- Added `about.html` with the site's purpose, published content, operating policy, operator identity, GitHub link, and contact method.
- Added `apps/luck-wealth-simulator.html` describing the live simulation, its adjustable conditions, observable results, and educational-purpose limitation.
- Added About links to the navigation and footer of `index.html`, `privacy.html`, and the app introduction page.
- Linked the portal's app card to both the introduction page and the live app.
- Added shared design tokens and responsive content-page styles while preserving the portal's existing green and neutral visual language.
- Updated `README.md` for the new routes, project structure, design tokens, and current AdSense configuration.

## Source reviewed

- Reviewed `https://luck-wealth-simulator.naorex.link/` to verify the app name, yard-sale model, adjustable conditions, displayed results, and educational disclaimer used in the introduction.

## Verification

- Confirmed `about.html`, the app introduction page, `styles.css`, and `tokens.css` return HTTP 200 from a local static server.
- Confirmed all local HTML links resolve and all referenced CSS custom properties are defined.
- Parsed all HTML files with Python's standard-library HTML parser.
- Verified WCAG contrast ratios for text, accent, CTA text, and focus-ring colour pairs.
- Rendered all four pages in headless Chrome at 320, 375, 414, 768, 1280, and 1920 CSS pixels.
- Confirmed there is no horizontal overflow and navigation, footer, and CTA labels remain on one line at each tested width.
- Visually reviewed mobile and desktop captures of both new pages and mobile captures of the updated existing pages.
- Ran `git diff --check`.
