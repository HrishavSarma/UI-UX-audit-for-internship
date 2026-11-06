# Website Improvement Recommendations

**Project:** InAmigos Foundation Website Audit  
**Website:** https://inamigosfoundation.org.in/  
**Date:** 6 November 2026

## 1. Objective

This document proposes practical improvements to the InAmigos Foundation website based on the findings recorded during the desktop audit and functional testing.

Recommendations are prioritised according to their impact on website functionality, visitor experience, accessibility and visual consistency.

## 2. Priority Classification

| Priority | Meaning |
|---|---|
| High | Issues affecting essential website functionality or visitor communication |
| Medium | Issues affecting navigation, usability, content access or interaction |
| Low | Visual refinements and minor improvements |

---

## 3. High-Priority Recommendations

### REC-001 — Restore Newsletter Subscription Functionality

**Related Finding:** FUNC-001

**Issue:** Newsletter submissions produce a server-side Swift_TransportException (HTTP 503) because local sendmail is disabled.

**Recommended Actions:**
- Configure a supported SMTP or email delivery service.
- Verify that valid subscriptions are processed successfully.
- Display a clear confirmation message after successful submission.
- Handle server-side failures gracefully without exposing technical error details.
- Test invalid, valid and duplicate email submissions.

**Expected Outcome:** Visitors can subscribe reliably, and the foundation can collect newsletter registrations without exposing server errors.

### REC-002 — Restore Contact Form Functionality

**Related Finding:** FUNC-002

**Issue:** Contact form submissions fail with a Swift_TransportException (HTTP 503).

**Recommended Actions:**
- Configure a reliable email delivery service.
- Validate form fields on both the client and server sides.
- Display clear success and failure messages.
- Prevent technical server exceptions from being exposed to visitors.
- Verify that submitted enquiries reach the foundation's intended email address.

**Expected Outcome:** Visitors can contact the foundation reliably through its website.

### REC-010 — Restore Password Reset Functionality

**Related Finding:** BLOG-001

**Issue:** Password reset submissions fail with a Swift_TransportException (HTTP 503).

**Recommended Actions:**
- Configure a supported SMTP or email delivery service.
- Verify that reset emails reach registered users.
- Ensure reset links are valid and expire appropriately.
- Display clear confirmation and failure messages.
- Avoid exposing technical server exceptions to visitors.

**Expected Outcome:** Users can reliably recover access to their accounts.

---

### REC-014 — Secure Account Password Changes

**Related Finding:** SEC-001

**Issue:** Authenticated users can change their passwords without verifying their existing password.

**Recommended Actions:**
- Require current-password verification before password changes.
- Perform verification on the server.
- Consider recent reauthentication for sensitive account operations.
- Invalidate or review existing sessions after credential changes.
- Display appropriate confirmation and error messages.

**Expected Outcome:** Unauthorized password changes through unattended authenticated sessions are made more difficult.

## 4. Medium-Priority Recommendations

### REC-003 — Fix Gallery Image Viewer

**Related Finding:** FUNC-003

**Issue:** The gallery lightbox opens, but the selected image does not load correctly.

**Recommended Actions:**
- Inspect image source paths and lightbox configuration.
- Verify that image assets load correctly.
- Implement appropriate loading and error states.
- Ensure visitors can close the image viewer and return to the gallery.

**Expected Outcome:** Visitors can open and view gallery images without encountering an indefinite loading state.

### REC-004 — Correct Gallery Pagination

**Related Finding:** FUNC-004

**Issue:** The gallery indicates 10 entries per page but appears to display all images, and pagination controls do not behave as expected.

**Recommended Actions:**
- Review the pagination implementation.
- Ensure the selected page displays the corresponding images.
- Make the displayed entry count consistent with the selected page size.
- Verify navigation between pages.

**Expected Outcome:** Visitors can navigate gallery content in manageable and predictable groups.

### REC-005 — Correct Social Media Destinations

**Related Finding:** FUNC-005

**Issue:** Several social media icons lead to generic or unexpected destinations.

**Recommended Actions:**
- Verify the foundation's official social media profile URLs.
- Replace generic platform homepage links with verified profile destinations.
- Investigate the Facebook destination that reports unavailable content.
- Remove links for accounts that are no longer active or available.

**Expected Outcome:** Visitors can reach the foundation's intended social media profiles.

### REC-006 — Improve Homepage Action Card Affordance

**Related Finding:** HOME-007

**Issue:** The Donate Us, Become A Volunteer and Join Us cards do not clearly communicate that they are clickable.

**Recommended Actions:**
- Introduce recognizable button or card interaction styling.
- Add hover and focus states.
- Improve visual separation between the cards and surrounding content.
- Ensure the entire intended interactive area responds consistently to clicks.

**Expected Outcome:** Visitors can more easily identify and use important engagement options.

### REC-007 — Improve Causes Page Content

**Related Finding:** HOME-008

**Issue:** The Causes page displays "NO RESULTS" with substantial unused space.

**Recommended Actions:**
- Verify whether causes are available in the website's content management system.
- Display relevant causes with descriptions and supporting images.
- Provide clear calls to action where appropriate.
- If no causes are available, replace the empty result with a meaningful message and alternative navigation.

**Expected Outcome:** Visitors receive useful information instead of an uninformative empty page.

### REC-011 — Correct Individual Blog Tag URLs

**Related Finding:** BLOG-003

**Issue:** Some individual blog tag links contain an unwanted leading hyphen, resulting in empty search results.

**Recommended Actions:**
- Review how tag slugs are generated.
- Remove unintended leading characters from tag URLs.
- Verify that generated URLs match registered tag slugs.
- Test all individual tag links across multiple articles.

**Expected Outcome:** Visitors can access relevant articles through valid individual tag links.

### REC-012 — Correct Project Vikas Tag Link Structure

**Related Finding:** BLOG-004

**Issue:** The entire Project Vikas tag section is one link containing multiple hashtags, leading to a 404 error.

**Recommended Actions:**
- Render each tag as an independent link.
- Generate a valid URL for each tag.
- Ensure the clickable area corresponds to the individual tag.
- Test each tag separately.

**Expected Outcome:** Visitors can navigate to relevant content through individual Project Vikas tags.

---

### REC-016 — Improve Login and Account Access Discoverability

**Related Finding:** AUTH-001

**Issue:** Visitors cannot easily locate the login and registration pages through the primary navigation. The login page was discovered through an individual blog article's comment section.

**Recommended Actions:**
- Add a clearly visible Login link to the main navigation or an account menu.
- Provide a Register link alongside the login option.
- Ensure the login page provides an accessible Forgot Password link.
- Maintain consistent access to account-related pages across the website.
- Verify that all account links work correctly on desktop and mobile layouts.

**Expected Outcome:** Visitors can easily discover and access login, registration and password recovery without navigating through an individual blog article.

### REC-015 — Fix Responsive Homepage Horizontal Overflow

**Related Finding:** RESP-001

**Issue:** The homepage exhibits horizontal overflow around the hero section at mobile and tablet viewport widths.

**Recommended Actions:**
- Inspect the hero section and carousel container dimensions.
- Identify elements extending beyond the viewport.
- Review image sizing, positioning and responsive width rules.
- Correct overflow without hiding legitimate content.
- Verify the layout at mobile, tablet and desktop breakpoints.

**Expected Outcome:** The homepage remains aligned within the viewport without unintended horizontal scrolling.


## 5. Low-Priority Recommendations

### REC-008 — Update Social Media Branding

**Related Finding:** FUNC-006

**Recommended Actions:**
- Replace outdated Twitter branding with the appropriate current platform branding if the account is active.
- Remove the inactive Google+ icon.
- Maintain consistent icon sizing, spacing and visual style.

**Expected Outcome:** The social media section looks current and contains relevant platforms.

### REC-009 — Improve Homepage Visual Consistency

**Related Findings:** HOME-002, HOME-003, HOME-004, HOME-005, HOME-006

**Recommended Actions:**
- Increase header and footer logo visibility while maintaining aspect ratio.
- Rebalance the About section's image and text layout.
- Standardise event card heights and align their call-to-action buttons.
- Establish a consistent colour palette with clearly defined primary, secondary and accent colours.
- Verify colour contrast against WCAG 2.2 AA requirements.

**Expected Outcome:** The homepage presents a more cohesive visual identity, improved content hierarchy and consistent layout.

### REC-013 — Standardize Blog Post Tag Presentation

**Related Finding:** BLOG-002

**Recommended Actions:**
- Use a consistent tag layout across all blog articles.
- Standardize tag spacing, backgrounds and typography.
- Make individual tags consistently identifiable as links.
- Hide the Post Tags section when no tags are assigned.

**Expected Outcome:** Blog articles have a consistent tag presentation and avoid displaying empty tag sections.

---

## 6. Additional Usability Improvements

The following observations are documented in the functional testing log. They are opportunities for improvement rather than confirmed functional defects.

| Test ID | Observation | Recommendation |
|---|---|---|
| TEST-009 | Event links open in the current tab | Consider whether opening external event destinations in a new tab would improve browsing continuity. |
| TEST-011 | Volunteers pagination produces an uneven final row | Review card-grid alignment and spacing across pagination pages. |
| TEST-013 | Footer links open in the current tab | Consider new-tab behaviour for selected external links where appropriate. |
| TEST-014 | Blog Read More links open in the current tab | Consider new-tab behaviour where it improves browsing continuity. |

Internal links should generally retain conventional same-tab navigation unless there is a specific usability reason to do otherwise.

---

## 7. Recommended Implementation Order

| Order | Recommendation | Priority |
|---|---|---|
| 1 | Restore contact form functionality (REC-002) | High |
| 2 | Restore newsletter subscription functionality (REC-001) | High |
| 3 | Restore password reset functionality (REC-010) | High |
| 4 | Secure account password changes (REC-014) | High |
| 5 | Fix gallery image viewer (REC-003) | Medium |
| 6 | Correct gallery pagination (REC-004) | Medium |
| 7 | Correct social media destinations (REC-005) | Medium |
| 8 | Improve homepage action card affordance (REC-006) | Medium |
| 9 | Improve Causes page content (REC-007) | Medium |
| 10 | Correct individual blog tag URLs (REC-011) | Medium |
| 11 | Correct Project Vikas tag link structure (REC-012) | Medium |
| 12 | Improve Login and Account Access Discoverability (REC-016) | Medium |
| 13 | Fix responsive homepage horizontal overflow (REC-015) | Medium |
| 14 | Update social media branding (REC-008) | Low |
| 15 | Improve homepage visual consistency (REC-009) | Low |
| 16 | Standardize blog post tag presentation (REC-013) | Low |
