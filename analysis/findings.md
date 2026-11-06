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

### HOME-007 - Poor Visual Affordance of Homepage Action Cards

- **Page:** Homepage
- **Category:** User Experience / Visual Design
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/button-not-recognisible.png`
- **Observation:** The Donate Us, Become A Volunteer and Join Us cards do not clearly communicate that they are clickable.
- **User impact:** Visitors may not recognize these elements as interactive and may miss important engagement options.
- **Recommendation:** Make the interactive nature of these cards more visually apparent.
- **Proposed solution:** Introduce clear button styling, hover states, visual cues or other recognizable interaction indicators.
- **Status:** Verified

### HOME-008 - Empty Causes Page

- **Page:** Causes
- **Category:** Content / User Experience
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/causes-fullpage-overview.png`
- **Observation:** The Causes page displays "NO RESULTS" and contains substantial unused space.
- **User impact:** Visitors looking for the foundation's causes or initiatives may find no meaningful information or engagement opportunities.
- **Recommendation:** Populate the page with relevant causes or provide a useful empty-state explanation.
- **Proposed solution:** Display available causes with descriptions and relevant calls to action. If no causes are available, provide a meaningful message and alternative navigation.
- **Status:** Verified

### FUNC-001 - Newsletter Subscription Server Error

- **Page:** Homepage (Footer)
- **Category:** Functionality / Backend
- **Severity:** High
- **Original Evidence:** `../screenshot/original/footer-contactUs-textbox-error.png`
- **Observation:** Submitting a valid-format email address produces a Swift_TransportException with HTTP 503. The server reports that local sendmail is disabled.
- **User impact:** Visitors may be unable to subscribe to newsletter updates, preventing the foundation from collecting interested subscribers through this form.
- **Recommendation:** Correct the server-side email delivery configuration and verify successful subscription processing.
- **Proposed solution:** Configure a supported SMTP or mail delivery service, handle delivery errors gracefully and display clear success or failure feedback.
- **Status:** Verified

### FUNC-002 - Contact Form Submission Failure

- **Page:** Contact
- **Category:** Functionality / Backend
- **Severity:** High
- **Original Evidence:** `../screenshot/original/contact-submitButton-error.png`
- **Supporting Page Evidence:** `../screenshot/original/contact-fullpage-overview.png`
- **Observation:** Submitting the contact form produces a Swift_TransportException with HTTP 503. The server reports that local sendmail is disabled.
- **User impact:** Visitors may be unable to contact the foundation through its website, potentially preventing enquiries, support requests and other communication.
- **Recommendation:** Restore reliable contact form submission and provide appropriate confirmation or error feedback.
- **Proposed solution:** Configure a supported email delivery service, implement server-side error handling and test successful message delivery.
- **Status:** Verified

### FUNC-003 - Gallery Lightbox Image Loading Failure

- **Page:** Gallery
- **Category:** Functionality
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/gallery-blur-when-open-image.png`
- **Observation:** Clicking a gallery image blurs the background, but the selected image does not load and the interface appears to remain in a loading state.
- **User impact:** Visitors cannot properly view enlarged gallery images, reducing the usefulness of the gallery.
- **Recommendation:** Investigate and correct the image lightbox loading behaviour.
- **Proposed solution:** Verify image source paths, lightbox configuration and loading/error handling. Ensure the selected image displays correctly and the viewer can be closed.
- **Status:** Verified

### FUNC-004 - Gallery Pagination Not Functioning Correctly

- **Page:** Gallery
- **Category:** Functionality / Pagination
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/gallery-fullpage-overview.png`
- **Observation:** The gallery indicates 10 entries per page but appears to display all images. The pagination controls do not behave as expected.
- **User impact:** Visitors cannot reliably navigate gallery content in manageable pages.
- **Recommendation:** Correct the gallery pagination behaviour and ensure the displayed entry count matches the selected page.
- **Proposed solution:** Review the pagination implementation, page-size configuration and image-list rendering logic.
- **Status:** Verified

### FUNC-005 - Incorrect Social Media Link Destinations

- **Page:** Homepage / Footer
- **Category:** Navigation / External Links
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/facebook-link.png`
- **Additional Evidence:** `../screenshot/original/wrong-instagram.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-footer-outdated-wrongLinks-same-problem-as-header.png`
- **Observation:** Several social media icons do not lead to the expected foundation profiles. The Twitter and Pinterest icons open generic platform homepages, the Instagram icon points to an incorrect destination, and the Facebook destination reports that its content is unavailable.
- **User impact:** Visitors may be unable to find or follow the foundation's official social media accounts, reducing trust and engagement.
- **Recommendation:** Verify and correct all social media destinations.
- **Proposed solution:** Replace incorrect URLs with verified official profile links. Remove links for accounts that are no longer active or available.
- **Status:** Verified

### FUNC-006 - Outdated and Inactive Social Media Icons

- **Page:** Homepage / Footer
- **Category:** Visual Design / Navigation
- **Severity:** Low
- **Original Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/twitter-outdated-logo-annotated.png`
- **Additional Annotated Evidence:** `../screenshot/annotated/unnecessary-google-logo-annotated.png`
- **Observation:** The social media section displays the outdated Twitter bird icon and an unnecessary Google+ icon that redirects to google.com.
- **User impact:** Outdated or irrelevant branding can make the website appear poorly maintained and may confuse visitors about the foundation's active social channels.
- **Recommendation:** Update the social media icon set to reflect the foundation's currently active platforms.
- **Proposed solution:** Replace the outdated Twitter branding where appropriate, remove the inactive Google+ icon and retain only verified, relevant social links.
- **Status:** Verified

### FUNC-007 - Restricted Clickable Area on Category Cards

- **Page:** Categories
- **Category:** Functionality / User Experience
- **Severity:** Medium
- **Original Evidence:** `../screenshot/original/categories-fullpage-overview.png`
- **Annotated Evidence:** `../screenshot/annotated/categories-fullpage-overview-annotated.png`
- **Observation:** Category cards visually appear to be fully interactive, but navigation is triggered only when clicking directly on the category text. Clicking the surrounding card area does not activate the link.
- **User impact:** Visitors may assume the cards are unresponsive, causing confusion and making category navigation less intuitive.
- **Recommendation:** Make the entire category card a clickable target.
- **Proposed solution:** Extend the anchor element to wrap the complete card, including its image and text, while preserving appropriate keyboard accessibility and focus styling.
- **Status:** Verified
