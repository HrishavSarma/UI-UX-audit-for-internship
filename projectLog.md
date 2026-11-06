# Project Milestone Journal

**Project:** InAmigos Foundation Website Audit  
**Website:** https://inamigosfoundation.org.in/  
**Project Period:** November 2026

This journal records significant project milestones, important findings, decisions and outstanding work. Detailed audit observations, test results and recommendations are maintained in their respective documents.

---

## 06 November 2026 — Project Initialization

### Completed
- Established the website audit project and created its GitHub repository.
- Organized the repository into documentation, analysis, screenshot and report directories.
- Created the initial README and project documentation structure.
- Established Git version control and pushed the initial project structure.

### Key Decision
Use separate documents for findings, functional testing, test cases and recommendations rather than combining all audit information into one file.

### Status
Project structure established and version-controlled.

---

## 06 November 2026 — Initial Homepage Audit

### Completed
- Captured full-page and section-specific homepage screenshots.
- Inspected the header, announcement bar, navigation, About section, events and footer.
- Created original and annotated screenshot evidence.
- Identified six preliminary homepage design findings (`HOME-001` to `HOME-006`).
- Sampled announcement bar contrast at approximately 2.11:1.

### Key Findings
- Announcement bar contrast.
- Header logo sizing.
- About section whitespace.
- Event card CTA alignment.
- Footer logo sizing.
- Colour palette consistency.

### Key Decision
Record visual observations separately from functional test results, with screenshot evidence supporting the findings.

### Status
Initial homepage findings documented and pushed to GitHub.

---

## 06 November 2026 — Functional and Cross-Page Testing

### Completed
- Tested newsletter email validation and subscription behaviour.
- Tested social media destinations and footer navigation.
- Inspected the Causes, Gallery and Volunteers pages.
- Tested gallery image viewing and pagination.
- Tested Contact form submission.
- Recorded 18 functional and UX observations, including three newsletter tests.
- Captured screenshots for significant issues.

### Key Findings
- Newsletter and Contact form submissions encounter server-side HTTP 503 email delivery errors.
- Several social media destinations are incorrect or unavailable.
- Gallery image viewing and pagination do not behave as expected.
- Causes page displays an empty result state.
- Homepage action cards have unclear clickable affordance.
- Additional navigation and layout improvements were identified.

### Important Decision
Distinguish confirmed functional defects from usability preferences. For example, opening an internal link in the current tab is not automatically treated as a defect.

### Status
Initial functional testing recorded in `analysis/functionalTesting.md` and test scenarios documented in `analysis/testCases.md`.

---

## 06 November 2026 — Evidence Organization and Documentation

### Completed
- Organized original and annotated screenshots into separate directories.
- Redacted sensitive hosting and personal information from relevant evidence screenshots.
- Corrected screenshot filenames and organized the evidence collection.
- Added relative screenshot references to the functional testing log.
- Verified evidence filenames against the repository directory structure.

### Key Decision
Keep original screenshots unchanged as supporting evidence and maintain separate annotated versions for highlighting observations.

### Status
Screenshot evidence organized and evidence references added to the functional testing log.

---

## 06 November 2026 — Findings Register Expansion

### Completed
- Expanded `analysis/findings.md` from six preliminary homepage findings to fourteen documented findings.
- Added functional findings for newsletter submission, Contact form, Gallery behaviour and social media issues.
- Added findings for the empty Causes page and homepage action cards.
- Assigned severity levels and documented user impact, recommendations and proposed solutions.

### Key Decision
Use unique issue identifiers (`HOME-` and `FUNC-`) to connect findings with supporting test records.

### Status
Findings register committed and pushed to GitHub.

---

## 06 November 2026 — Recommendations and Prioritization

### Completed
- Created `analysis/recommendations.md`.
- Developed nine prioritized recommendations linked to the findings register.
- Grouped improvements into High, Medium and Low priorities.
- Established a recommended implementation order.
- Separated usability improvement opportunities from confirmed functional defects.

### Key Decision
Prioritize essential visitor communication and website functionality before visual refinements.

### Status
Recommendations documented and pushed to GitHub.

---

## 06 November 2026 — Categories Page Audit

### Completed
- Inspected category card interactions.
- Identified that navigation works only when clicking directly on the category text.
- Captured original and annotated screenshot evidence.
- Recorded the issue as `TEST-016` in `analysis/functionalTesting.md`.
- Added `FUNC-007` to `analysis/findings.md`.

### Key Finding
Category cards visually suggest that the entire card is interactive, but the actual clickable area is restricted to the category text.

### Recommendation
Extend the clickable anchor area to cover the entire category card, including its image and text, while preserving keyboard accessibility and focus styling.

### Status
Finding documented. Corresponding documentation and evidence changes are awaiting commit and push.

---

## Outstanding Work

- Continue auditing remaining individual website pages.
- Inspect homepage sections not yet covered.
- Test navigation, links and interactive elements across the website.
- Evaluate mobile and tablet responsiveness.
- Conduct further accessibility and technical checks.
- Add newly verified findings and supporting evidence.
- Update recommendations as the audit progresses.
- Prepare the final report after the audit is complete.
- Complete the required Drive and internship submission steps.