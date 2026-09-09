# Expand the Luck Wealth Simulator detailed guide

Date: 2026-09-09

## Changes

- Expanded `apps/luck-wealth-simulator.html` from a short introduction into a detailed educational guide.
- Added implementation-based explanations of all adjustable parameters, result metrics, wealth concentration, redistribution, and model limitations.
- Added a page index, comparison procedure, and prominent links to the live Simulator.
- Changed the portal card link to `詳しい解説を読む` while preserving the separate `アプリを開く` action.
- Added responsive guide styles using the existing Garden theme and design tokens.
- Updated `README.md` to describe the route as a detailed guide rather than an introduction.
- Updated Hallmark project memory for the Conversational FAQ structure.

## Source reviewed

- Reviewed `https://luck-wealth-simulator.naorex.link/` and its delivered JavaScript to verify parameter ranges, random pairing, wager calculation, per-round redistribution, seeded reproducibility, presets, and displayed result metrics.

## Verification

- Parsed all four HTML files and confirmed that IDs are unique.
- Checked 64 local references, including page anchors, with no missing targets.
- Confirmed the home page, detailed guide, `styles.css`, and `tokens.css` return HTTP 200 from a local static server.
- Confirmed every referenced CSS custom property is defined and all modified JSON is valid.
- Confirmed the required parameter, metric, limitation, link, and CTA text is present.
- Verified WCAG contrast ratios for body, muted, accent, CTA, hover, and focus colour pairs.
- Rendered the detailed guide at 320, 375, 414, 768, and 1280 CSS pixels and visually reviewed full-page captures at mobile and desktop widths.
- Scanned the home page and detailed guide at 81 widths from 320 through 1920 CSS pixels; found no horizontal overflow or wrapped primary navigation, footer, card action, guide-index, or CTA labels.
- Confirmed the complete hero and primary CTA fit within a 1280×800 viewport.
- Completed the Hallmark 58-gate slop review and ran `git diff --check`.
