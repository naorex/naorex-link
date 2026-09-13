# Add robots.txt and sitemap.xml

Date: 2026-09-10

## Changes

- Added `robots.txt` to allow crawlers to access the public site and advertise the sitemap URL.
- Added `sitemap.xml` with the four public pages currently available on `naorex.link`.
- Updated `README.md` with the new files, their public URLs, and the requirement to keep the sitemap synchronized with public pages.

## Verification

- Confirmed the `robots.txt` content matches the intended crawler and sitemap directives.
- Parsed `sitemap.xml` successfully and confirmed it contains exactly the four intended URLs.
- Confirmed every URL in the sitemap maps to an existing local HTML file.
- Served both files with a local static server and confirmed HTTP 200 responses, expected content types, and unchanged response bodies.
- Ran `git diff --check`.
