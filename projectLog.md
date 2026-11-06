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
Finding documented, evidence captured, committed and pushed.

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
## 06 November 2026 — About Us Page Audit

### Completed
- Inspected the About Us page layout and content.
- Tested breadcrumb navigation.
- Confirmed the Home breadcrumb link navigates correctly.
- Identified the incorrect current-page breadcrumb label: "Page" instead of "About Us".
- Recorded `TEST-017` in `analysis/functionalTesting.md`.
- Added `ABOUT-001` to `analysis/findings.md`.
- Captured original and annotated screenshot evidence.

### Key Finding
The About Us breadcrumb displays "Home / Page" instead of "Home / About Us".

### Status
Finding documented, evidence captured, committed and pushed.

---

## 06 November 2026 — Blog Page Audit

### Completed
- Inspected the Blog listing and individual article pages.
- Tested login and registration functionality.
- Tested password recovery and identified a server-side email delivery failure.
- Verified that all tested Read More links open their corresponding articles.
- Confirmed that category filtering works.
- Identified incorrect leading-hyphen slugs on some individual tag links.
- Identified a malformed combined tag link on the Project Vikas article that leads to a 404 error.
- Compared tag presentation across Project Vikas, Mission Life and Animal Protection articles.
- Captured original and annotated screenshot evidence.
- Recorded Blog functional tests (`TEST-018` to `TEST-025`).
- Added four Blog findings (`BLOG-001` to `BLOG-004`).
- Added recommendations for password recovery, tag navigation and tag presentation.

### Key Findings
- Password reset submissions fail with a server-side HTTP 503 email delivery error.
- Some individual tag URLs contain an unwanted leading hyphen.
- Project Vikas uses one malformed link for its entire tag section.
- Blog post tag presentation is inconsistent.

### Important Decisions
- Blog pagination was not recorded as a defect because the listing displays 10 entries with 10 entries per page. No additional entries were established.
- Category filtering and article navigation were verified as working.
- Mobile and tablet responsiveness will be assessed during the dedicated responsive audit.
- Tag URL generation problems were documented separately from visual tag presentation.

### Status
Blog audit documented. Evidence captured. No website implementation undertaken.

---

## 06 November 2026 — Account Security Testing

### Completed
- Inspected the My Profile password-change functionality.
- Tested changing the account password without entering the current password.
- Confirmed the password update succeeded.
- Verified that the old password stopped working after the change.
- Verified that the new password successfully authenticated the account.
- Captured and sanitized screenshot evidence.
- Recorded `TEST-026` in `analysis/functionalTesting.md`.
- Added `SEC-001` to `analysis/findings.md`.
- Added `REC-014` to `analysis/recommendations.md`.

### Key Finding
The account password can be changed without current-password verification.

### Recommendation
Require server-side current-password verification or equivalent recent reauthentication before processing password changes.

### Status
Security weakness verified and documented. No implementation undertaken.

06 November 2026 — Responsive Audit

Record:
- Main website pages inspected at 375px.
- Additional homepage checks at 430px and 768px.
- Existing desktop findings checked against mobile layouts.
- RESP-001 and TEST-027 documented.
- No screenshot evidence captured for this phase.
- No website implementation undertaken.

### 07 November 2026 — Announcement Bar Contrast Verification

- Inspected homepage inline CSS and external stylesheet.
- Confirmed text colour (#FFFFFF) and background colour (#00CC83).
- Verified contrast ratio of approximately 2.11:1.
- Confirmed failure against WCAG 2.1 Level AA requirements.
- Updated HOME-001 from pending verification to verified.

### 07 November 2026 — Account Access Discoverability Audit

- Identified and documented the lack of an obvious Login / Register entry point in the primary navigation.
- Traced the login discovery path through Blog → Individual Article → Comment Section → `LOGGED IN`.
- Confirmed that Register and Forgot Password are accessible from the login page.
- Added finding AUTH-001, test TEST-028 and recommendation REC-016.
- Updated the audit totals and final report.
