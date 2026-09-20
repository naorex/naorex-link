# Add the Japan Tide Navi introduction page

Date: 2026-09-20

## Changes

- Added `apps/japan-tide-navi.html` as a practical introduction and usage guide for 潮位なび.
- Explained observation-point selection, the graph and hourly summaries, saved target tides, data provenance, and safety limitations.
- Added an optimized WebP product capture at `assets/japan-tide-navi-overview.webp` with intrinsic dimensions and descriptive alternative text.
- Added 潮位なび as the first, full-width app on the home page, with the live app as the primary action and the guide as a secondary action.
- Updated the Privacy page to cover 潮位なび browser storage and API requests, and added the guide to `sitemap.xml`.
- Added token-based Workbench styles while retaining the existing Garden theme, site navigation, footer, and static HTML/CSS architecture.
- Updated Hallmark project memory for the new page.
- Checked and updated `README.md` because the new public route, asset, homepage content, and privacy behavior made the previous documentation incomplete.
- Checked `tokens.css` and left it unchanged because the existing Garden tokens cover every new style.

## Source reviewed

- Reviewed the deployed `https://japan-tide-navi.naorex.link/` interface and its delivered JavaScript bundle on 2026-09-20.
- Verified the station filters, station search, daily graph, hourly averages, high/low summaries, target-tide marker, local-storage keys, API request parameters, and retry behavior before writing the guide.
- Verified the app's attribution to the Japan Coast Guard's 海しる data and reflected its non-guarantee and safety limitations in the page copy.
- Used a current capture of the public app for the guide image; no protected environment files or secret values were read or copied.

## Verification

- Parsed all six HTML files and checked local references, page anchors, unique IDs, heading order, external-link safety attributes, JSON, XML, and referenced CSS custom properties.
- Served the site locally and confirmed HTTP 200 responses and the expected MIME types for the home page, guide, WebP asset, shared styles, Privacy page, existing app guide, and sitemap.
- Confirmed that the product capture is a valid 1340×910 WebP image and is 42,312 bytes.
- Rendered the new guide at 320, 375, 414, 768, and 1280 CSS pixels and the home page at mobile and desktop widths; visually reviewed the mobile, desktop, and 1280×800 fold captures.
- Confirmed that the desktop hero, facts, primary action, and start of the real product capture fit within a 1280×800 viewport.
- Found no horizontal overflow, clipped content, wrapped primary action, placeholder copy, fabricated interface, or unsupported product claim.
- Completed the Hallmark 58-gate review with passing contrast, slop, honesty, chrome, token, responsive, icon, and mobile checks.
- Ran `git diff --check` with no whitespace errors.
