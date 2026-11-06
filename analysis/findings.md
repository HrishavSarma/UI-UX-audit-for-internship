
# Website Audit Findings

**Project:** InAmigos Foundation Website Analysis  
**Website:** https://inamigosfoundation.org.in/  
**Audit date:** 6 November 2026

## Severity Classification

| Level | Meaning |
|---|---|
| Critical | Prevents essential functionality or access |
| High | Significantly affects usability or trust |
| Medium | Creates friction or inconsistency |
| Low | Minor improvement opportunity |

## Finding Template

### [ISSUE-ID] Finding Title

- **Page:**
- **Category:**
- **Severity:**
- **Evidence:** Screenshot filename
- **Observation:**
- **User impact:**
- **Recommendation:**
- **Proposed solution:**
- **Status:** Identified / Verified / Resolved

---

## Findings

### HOME-001 - Insufficient Contrast in Announcement Bar
- **Page:** Homepage
- **Category:** Visual Design / Accessibility
- **Severity:** High (WCAG AA contrast failure, pending verification against live CSS)
- **Contrast:** Approximately 2.11:1 (sampled from screenshot)
- **Original Evidence:** `../screenshot/original/header-announcement-bar.png`
- **Observation:** The white announcement text is displayed against a highly saturated green background. The colour combination may not provide sufficient contrast for comfortable reading.
- **User impact:** Visitors with low vision or reduced contrast sensitivity may find the information difficult to read.
- **Recommendation:** Verify the foreground/background contrast ratio against WCAG 2.2 AA requirements.
- **Proposed solution:** Consider a darker green background or an alternative text colour that meets the required contrast ratio.
- **Status:** Identified

### HOME-002 - Undersized Header Logo
- **Page:** Homepage
- **Category:** Branding / Visual Design
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/header-navigation.png`
- **Annotated Evidence:** `../screenshot/annotated/header-navigation-annotated.png`
- **Observation:** The organization logo occupies a relatively small area within the navigation bar.
- **User impact:** Brand visibility and recognition are reduced, particularly for first-time visitors.
- **Recommendation:** Increase the displayed logo size while preserving its aspect ratio and navigation spacing.
- **Proposed solution:** Adjust the logo dimensions and header alignment.
- **Status:** Identified

### HOME-003 - Unbalanced Whitespace in About Section
- **Page:** Homepage
- **Category:** Layout / User Experience
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/homepage-about-section.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-about-section-annotated.png`
- **Observation:** The About section contains a long text column alongside an image positioned near the top of its column, leaving a substantial unused area below the image.
- **User impact:** The section feels visually unbalanced and creates inefficient use of available screen space.
- **Recommendation:** Reconsider the two-column layout, image dimensions and content hierarchy.
- **Proposed solution:** Introduce a better-balanced image and text arrangement, with shorter paragraphs and clearly separated content.
- **Status:** Identified

### HOME-004 - Inconsistent Event Card CTA Alignment
- **Page:** Homepage
- **Category:** Layout / Consistency
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/homepage-events-section.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-events-section-annotated.png`
- **Observation:** Event cards have different content heights, resulting in their Read More buttons appearing at different vertical positions.
- **User impact:** The inconsistent alignment reduces visual consistency and makes the card section appear less organized.
- **Recommendation:** Standardize card heights and internal content layout.
- **Proposed solution:** Use a flexible card layout with a consistent content area and bottom-aligned call-to-action buttons.
- **Status:** Identified

### HOME-005 - Undersized Footer Logo
- **Page:** Homepage
- **Category:** Branding / Visual Design
- **Severity:** Low
- **Original Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-footer-annotated.png`
- **Observation:** The organization logo appears relatively small within the footer column.
- **User impact:** The organization's branding becomes less prominent in the footer.
- **Recommendation:** Increase logo visibility and maintain consistent branding across header and footer.
- **Proposed solution:** Adjust logo dimensions while maintaining appropriate spacing.
- **Status:** Identified

### HOME-006 - Opportunity to Improve Colour Palette
- **Page:** Homepage
- **Category:** Visual Design / Accessibility
- **Severity:** Low
- **Original Evidence:** `../screenshot/original/homepage-full-overview.png`
- **Observation:** The website relies heavily on bright green accents, white backgrounds and dark sections. The overall combination could benefit from a more consistent colour hierarchy.
- **User impact:** Inconsistent colour application can reduce visual cohesion and make important interface elements less distinguishable.
- **Recommendation:** Establish a cohesive colour system with defined primary, secondary, background and accent colours.
- **Proposed solution:** Develop a refined colour palette and verify text and interactive-element contrast against WCAG 2.2 AA.
- **Status:** Identified
