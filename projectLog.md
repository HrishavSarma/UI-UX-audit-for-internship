## 06 November 2026 — Homepage Audit

### Completed
- Captured full homepage overview.
- Inspected header and navigation.
- Inspected About section.
- Inspected event cards.
- Inspected footer.
- Identified six preliminary design findings.
- Measured announcement bar contrast at approximately 2.11:1.

### Findings
- Announcement bar contrast.
- Header logo sizing.
- About section whitespace.
- Event CTA alignment.
- Footer logo sizing.
- Colour palette consistency.

### Next
- Inspect homepage hero and remaining sections.
- Inspect mobile responsiveness.
- Verify navigation and CTA functionality.
- Begin auditing individual pages.

## 6 November 2026 — Categories Page Audit

### Work Completed
- Inspected the Categories page and tested category card interactions.
- Identified that category navigation works only when clicking directly on the category text.
- Clicking the surrounding card area does not activate navigation.
- Recorded the issue as `TEST-016` in `analysis/functionalTesting.md`.
- Added `FUNC-007` to `analysis/findings.md`.
- Added original and annotated screenshot evidence.

### Key Finding
Category cards visually suggest that the entire card is interactive, but the actual clickable area is restricted to the category text.

### Recommendation
Extend the clickable anchor area to cover the entire category card, including its image and text, while preserving keyboard accessibility and focus styling.

### Status
Finding documented; implementation not undertaken. Changes pending Git commit and push.