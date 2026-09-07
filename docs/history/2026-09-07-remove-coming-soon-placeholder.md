# Remove portal coming-soon placeholder

Date: 2026-09-07

## Changes

- Removed the "COMING SOON / More tools" placeholder card from the Apps section of the portal.
- Removed the now-unused `.muted-card` CSS rule.

## Verification

- Confirmed that no `COMING SOON`, `More tools`, or `muted-card` references remain in the portal files.
- Parsed the HTML files with Python's standard-library HTML parser.
- Checked the repository diff for whitespace errors.

## Documentation

- Reviewed `README.md`; no update was needed because the existing project structure and instructions for adding an app remain accurate.
