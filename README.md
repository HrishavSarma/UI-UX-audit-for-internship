# InAmigos Foundation — Website UI/UX Audit

A website usability, functionality and visual-design audit conducted as **Task 2 of the InAmigos Foundation internship**.

**Website:** https://inamigosfoundation.org.in/  
**Repository:** https://github.com/HrishavSarma/UI-UX-audit-for-internship  
**Audit period:** 6–7 November 2026

## Project Overview

This project evaluates the InAmigos Foundation website from a visitor's perspective, identifying usability issues, functional problems, navigation inconsistencies, visual-design concerns and responsive-layout issues.

The audit was conducted through manual inspection and interaction testing. Findings are documented with severity classifications, user impact, recommendations and supporting screenshot evidence.

## Audit Summary

| Metric | Result |
|---|---:|
| Total findings | 23 |
| High severity | 5 |
| Medium severity | 13 |
| Low severity | 5 |
| Functional test cases | 31 |
| Tests passed | 5 |
| Tests failed | 14 |
| Improvement required | 11 |
| Partial results | 1 |

## Audit Scope

The audit covered the following website areas:

- Homepage and navigation
- About Us and Causes
- Categories
- Contact
- Gallery
- Volunteers
- Events
- Blog listing and individual articles
- Login and registration
- Password recovery
- My Profile and Edit Profile

### Testing Activities

- Manual visual inspection
- Navigation and hyperlink testing
- Form submission and validation testing
- Account and authentication-flow testing
- Gallery lightbox and pagination testing
- Blog tag and category navigation testing
- Responsive viewport inspection
- Screenshot-based evidence collection

## Key Findings

Some of the significant issues identified include:

- Newsletter and contact form submissions encountering server-side email delivery errors.
- Password reset email delivery failure.
- Password changes not requiring current-password verification.
- Login and registration options being difficult to discover.
- Gallery image loading and pagination issues.
- Incorrect or unavailable social media destinations.
- Restricted clickable areas on category cards.
- Homepage horizontal overflow at certain viewport widths.
- Inconsistent blog tag presentation and malformed tag URLs.
- Insufficient announcement-bar text contrast based on the downloaded homepage CSS.

Refer to the detailed findings register for all documented observations.

## Repository Structure

```text
UI-UX-audit-for-internship/
│
├── analysis/
│   ├── findings.md
│   ├── functionalTesting.md
│   ├── testCases.md
│   └── recommendations.md
│
├── screenshot/
│   ├── original/
│   └── annotated/
│
├── designs/
│
├── reports/
│
├── README.md
└── projectLog.md
```

### Directory Description

| Directory / File | Purpose |
|---|---|
| `analysis/findings.md` | Documented audit findings and their severity |
| `analysis/functionalTesting.md` | Actual functional and usability test observations |
| `analysis/testCases.md` | Test scenarios and expected behaviour |
| `analysis/recommendations.md` | Suggested corrective actions and implementation priorities |
| `screenshot/original/` | Original screenshot evidence |
| `screenshot/annotated/` | Screenshots with visual annotations |
| `designs/` | Design-related materials |
| `reports/` | Final audit deliverables |
| `projectLog.md` | Project milestones, decisions and progress |

## Screenshot Evidence

The repository maintains two separate screenshot collections:

- **Original:** Unmodified screenshots captured during website inspection.
- **Annotated:** Screenshots with highlights or markings to make specific observations easier to identify.

Evidence is referenced from the findings and functional testing documents using relative file paths.

## Deliverables

The project includes:

- Detailed findings register
- Functional testing log
- Test-case documentation
- Prioritized recommendations
- Original and annotated screenshot evidence
- Final website audit report in Word and PDF formats

## Limitations

- The audit was conducted manually.
- No automated accessibility, performance, load or penetration-testing suite was performed.
- Some observations have specific evidence limitations documented in the final report.
- The audit identifies issues and recommends improvements; website remediation was not part of the work.
- Findings should not be interpreted as a complete security or accessibility certification.

## Project Status

The website audit findings, testing records, recommendations and supporting evidence have been documented and version-controlled in this repository.

The repository serves as the supporting technical record for the final audit report.

---

**Prepared as part of the InAmigos Foundation internship — November 2026.**