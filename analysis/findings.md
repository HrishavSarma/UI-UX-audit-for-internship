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
- **Severity:** High (confirmed WCAG 2.1 Level AA contrast failure)
- **Contrast:** 2.11:1 (calculated from CSS colour values)
- **Original Evidence:** `../screenshot/original/header-announcement-bar.png`
- **Observation:** The white announcement text (#FFFFFF) is displayed against a green background (#00CC83). The calculated contrast ratio is approximately 2.11:1, which fails WCAG 2.1 Level AA requirements for normal text (minimum 4.5:1).
- **User impact:** Visitors with low vision or reduced contrast sensitivity may find the information difficult to read.
- **Recommendation:** Increase the text/background contrast ratio to at least 4.5:1 for normal text to meet WCAG 2.1 Level AA.
- **Proposed solution:** Consider a darker green background or an alternative text colour that meets the required contrast ratio.
- **Status:** Verified against downloaded homepage HTML and CSS.

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

### ABOUT-001 - Incorrect About Page Breadcrumb Label

- **Page:** About Us
- **Category:** Navigation / User Experience
- **Severity:** Low
- **Original Evidence:** `../screenshot/original/aboutUs-fullpage-overview.png`
- **Annotated Evidence:** `../screenshot/annotated/aboutUs-breadcrumb-heading-mismatch.png`
- **Observation:** The breadcrumb displays "Home / Page" instead of identifying the current page as "About Us". The Home link works correctly.
- **User impact:** Visitors may receive unclear page-location information when using the breadcrumb navigation.
- **Recommendation:** Display the correct current-page title in the breadcrumb.
- **Proposed solution:** Update the breadcrumb label dynamically or configure the About page breadcrumb to display "About Us".
- **Status:** Verified

---

### BLOG-001 - Password Reset Email Failure

- **Page:** Blog / Forgot Password
- **Category:** Functionality / Authentication / Backend
- **Severity:** High
- **Original Evidence:** `../screenshot/original/forgotPassword-page.png`
- **Error Evidence:** `../screenshot/original/resetPassword-error.png`
- **Observation:** Submitting a registered email address through the password reset form produces a Swift_TransportException with HTTP 503. The server reports that local sendmail is disabled.
- **User impact:** Users who forget their passwords may be unable to recover access to their accounts.
- **Recommendation:** Restore reliable password reset email delivery.
- **Proposed solution:** Configure a supported SMTP or email delivery service, implement appropriate error handling and verify that reset links reach registered users.
- **Status:** Verified

### BLOG-002 - Inconsistent Blog Post Tag Presentation

- **Page:** Individual Blog Articles
- **Category:** Visual Design / Consistency
- **Severity:** Low
- **Original Evidence:**
  - `../screenshot/original/projectVikas-tags.png`
  - `../screenshot/original/MissionLife-tags.png`
  - `../screenshot/original/Animal Protection-tag.png`
- **Annotated Evidence:**
  - `../screenshot/annotated/projectVikas-tags-annotated.png`
  - `../screenshot/annotated/MissionLife-tags-annotated.png`
  - `../screenshot/annotated/Animal Protection-tag-annotated.png`
- **Observation:** Blog post tags are presented inconsistently. Project Vikas displays tags together in one container, other posts display individual tag boxes, and Animal Protection has an empty Post Tags section.
- **User impact:** Inconsistent tag presentation reduces visual consistency across article pages and may leave visitors uncertain about the purpose of the empty section.
- **Recommendation:** Standardize tag presentation across all blog articles and avoid displaying empty tag sections.
- **Proposed solution:** Use a consistent tag component and individual tag elements. Hide the Post Tags section when no tags are assigned.
- **Status:** Verified

### BLOG-003 - Incorrect Individual Blog Tag URL Generation

- **Page:** Individual Blog Articles
- **Category:** Navigation / Functionality
- **Severity:** Medium
- **Original Evidence:**
  - `../screenshot/original/-sustainability-tag.png`
  - `../screenshot/original/sustainability-tag.png`
  - `../screenshot/original/-climate-action-tag.png`
  - `../screenshot/original/climate-tag.png`
- **Observation:** Some individual tag links generate URLs with an unwanted leading hyphen. For example, the `-sustainability` and `-climate-action` URLs return no results, while the corresponding clean tag slugs work.
- **User impact:** Visitors may be unable to access relevant articles through affected tag links.
- **Recommendation:** Correct the generation of individual tag URLs.
- **Proposed solution:** Review tag slug generation and ensure each tag link uses the correct registered slug without unintended characters.
- **Status:** Verified

### BLOG-004 - Malformed Tag Link on Project Vikas Article

- **Page:** Project Vikas Blog Article
- **Category:** Navigation / Functionality
- **Severity:** Medium
- **Original Evidence:**
  - `../screenshot/original/projectVikas-tags.png`
  - `../screenshot/original/projectVikas-tags-error404.png`
- **Annotated Evidence:** `../screenshot/annotated/projectVikas-tags-annotated.png`
- **Observation:** The entire Project Vikas tag section behaves as one clickable link. The generated URL combines all hashtags into one malformed URL, and clicking the section leads to a 404 error.
- **User impact:** Visitors cannot use the Project Vikas tags to discover related articles.
- **Recommendation:** Render each tag as a separate functional link.
- **Proposed solution:** Correct the tag markup and URL generation so that each tag has its own anchor element and valid destination.
- **Status:** Verified

---

### SEC-001 - Password Change Without Current-Password Verification

- **Page:** My Profile / Edit Profile
- **Category:** Security / Authentication
- **Severity:** High
- **Original Evidence:** `../screenshot/original/myProfile-fullpage-overview.png`
- **Observation:** An authenticated user can change their account password without supplying the existing password or completing an equivalent reauthentication check.
- **User impact:** Someone with access to an unattended authenticated session could change the account password and prevent the legitimate account owner from logging in.
- **Recommendation:** Require current-password verification or recent reauthentication before allowing password changes.
- **Proposed solution:** Implement server-side current-password verification before processing password updates. Ensure the verification cannot be bypassed by directly submitting a request.
- **Status:** Verified

---

### RESP-001 — Horizontal Overflow in Homepage Hero Section

- **Page:** Homepage
- **Category:** Responsive Design / Layout
- **Severity:** Medium
- **Affected Viewports:** 375px and 768px (confirmed); 430px inspected, but the issue was not separately confirmed.
- **Observation:** The homepage can be manually scrolled horizontally towards the left while the hero section is visible, exposing a blank white area. The page cannot be manually scrolled back towards the right. It automatically returns to its normal alignment when the "Get to Know Us Better" section begins.
- **User Impact:** Unexpected horizontal movement disrupts the browsing experience and exposes blank space beside the page content.
- **Recommendation:** Identify and correct the element causing horizontal overflow in the hero section.
- **Proposed Solution:** Inspect the hero container, slider dimensions, image sizing, positioning and overflow rules at responsive breakpoints.
- **Status:** Verified through manual responsive testing.
