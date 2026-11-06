# Functional Testing Log

**Project:** InAmigos Foundation Website Audit  
**Website:** https://inamigosfoundation.org.in/  
**Test Date:** 6 November 2026

## Newsletter Subscription

### TEST-NEWS-001 — Invalid Email Format

- **Page:** Homepage (Footer)
- **Input:** `notanemail`
- **Expected Result:** Website should reject invalid email addresses.
- **Actual Result:** Browser displays an email validation message: "Enter valid email".
- **Status:** PASS
- **Observation:** Client-side email format validation is functioning.

### TEST-NEWS-002 — Valid-format Email Submission

- **Page:** Homepage (Footer)
- **Input:** `notanemail@temp.com`
- **Expected Result:** Newsletter subscription should be processed and an appropriate confirmation displayed.
- **Actual Result:** Website displays a Swift_TransportException with HTTP 503. The error states that local sendmail is disabled.
- **Status:** FAIL
- **Observation:** The backend email delivery process encounters a server-side configuration error.
- **Evidence:** `../screenshot/original/footer-contactUs-textbox-error.png`

### TEST-NEWS-003 — Duplicate Subscription Feedback

- **Page:** Homepage (Footer)
- **Input:** Previously submitted email address.
- **Expected Result:** Website should display a clear duplicate-subscription message near the newsletter form.
- **Actual Result:** After reloading, the message "This email address already subscribed." appears.
- **Status:** PARTIAL
- **Observation:** The duplicate-subscription message is displayed, but the initial submission error creates uncertainty about whether the subscription was successfully processed. The message also requires manual scrolling to locate.
- **Evidence:** `../screenshot/original/footer-contactUs-textbox-already-subscribed-message.png`
- **Annotated Evidence:** `../screenshot/annotated/footer-contactUs-textbox-annotated.png`

---

## Website-Wide Functional and UX Observations

The following observations were recorded during manual desktop inspection and interaction testing. They include both functional issues and user experience improvement opportunities.

### TEST-001 — Outdated Twitter Branding

- **Page:** Homepage
- **Category:** Visual Design
- **Expected:** Social media icons should reflect current platform branding.
- **Actual:** The website displays the outdated Twitter bird icon.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/twitter-outdated-logo-annotated.png`

### TEST-002 — Facebook Link Failure

- **Page:** Homepage / Footer
- **Category:** Navigation
- **Expected:** Facebook icon should open the foundation's official Facebook profile.
- **Actual:** The Facebook link opens a Facebook page that reports the content is unavailable.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/facebook-link.png`

### TEST-003 — Incorrect Twitter Destination

- **Page:** Homepage / Footer
- **Category:** Navigation
- **Expected:** Twitter/X icon should open the foundation's official profile.
- **Actual:** Opens `https://twitter.com/` instead.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-footer-outdated-wrongLinks-same-problem-as-header.png`

### TEST-004 — Unnecessary Google+ Icon

- **Page:** Homepage / Footer
- **Category:** Visual Design / Navigation
- **Expected:** Social media section should contain relevant, active platform links.
- **Actual:** Google+ icon is displayed and redirects to google.com.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/unnecessary-google-logo-annotated.png`

### TEST-005 — Incorrect Pinterest Destination

- **Page:** Homepage / Footer
- **Category:** Navigation
- **Expected:** Pinterest icon should open the foundation's official profile.
- **Actual:** Opens `https://pinterest.com/` instead.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/homepage-footer.png`
- **Annotated Evidence:** `../screenshot/annotated/homepage-footer-outdated-wrongLinks-same-problem-as-header.png`

### TEST-006 — Incorrect Instagram Destination

- **Page:** Homepage / Footer
- **Category:** Navigation
- **Expected:** Instagram icon should open the foundation's official Instagram profile.
- **Actual:** Link points to an incorrect destination.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/wrong-instagram.png`

### TEST-007 — Poor Visual Affordance of Homepage Action Cards

- **Page:** Homepage
- **Category:** User Experience / Visual Design
- **Expected:** Interactive elements should be visually recognizable as clickable.
- **Actual:** The Donate Us, Become A Volunteer and Join Us cards do not clearly communicate that they are clickable.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/button-not-recognisible.png`

### TEST-008 — Empty Causes Page

- **Page:** Causes
- **Category:** Content / User Experience
- **Expected:** Visitors should see available causes or a meaningful empty-state message.
- **Actual:** Page displays "NO RESULTS" with substantial unused space.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/causes-fullpage-overview.png`

### TEST-009 — Event Links Open in Current Tab

- **Page:** Homepage / Events
- **Category:** Navigation
- **Expected:** Review whether opening event details in a new tab would improve browsing continuity.
- **Actual:** Read More links open in the current tab.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/homepage-events-section.png`

### TEST-010 — Gallery Lightbox Failure

- **Page:** Gallery
- **Category:** Functionality
- **Expected:** Clicking an image should display the selected image correctly.
- **Actual:** Background becomes blurred, but the image does not load and the interface appears to remain loading.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/gallery-blur-when-open-image.png`

### TEST-011 — Volunteers Pagination Layout

- **Page:** Volunteers
- **Category:** Layout / Pagination
- **Expected:** Pagination should maintain a consistent layout across pages.
- **Actual:** The bottom row displays only one volunteer profile despite additional profiles appearing on the following page.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/volunteers-fullpage-overview.png`

### TEST-012 — Gallery Pagination Inconsistency

- **Page:** Gallery
- **Category:** Functionality / Pagination
- **Expected:** Selecting a pagination number should display the corresponding set of images.
- **Actual:** Page indicates 10 entries per page but displays all images. Pagination controls do not behave as expected.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/gallery-fullpage-overview.png`

### TEST-013 — Footer Links Open in Current Tab

- **Page:** Homepage / Footer
- **Category:** Navigation
- **Expected:** Review whether opening selected footer links in new tabs would improve browsing continuity.
- **Actual:** Useful Links open in the current tab.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/homepage-footer.png`

### TEST-014 — Blog Links Open in Current Tab

- **Page:** Blog
- **Category:** Navigation
- **Expected:** Review whether opening article details in new tabs would improve browsing continuity.
- **Actual:** Read More links open in the current tab.
- **Status:** Improvement Required
- **Evidence:** No dedicated blog screenshot captured.

### TEST-015 — Contact Form Submission Failure

- **Page:** Contact
- **Category:** Functionality / Backend
- **Expected:** Valid contact submissions should be processed and confirmation displayed.
- **Actual:** Submission produces a Swift_TransportException with HTTP 503. Server reports that local sendmail is disabled.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/contact-submitButton-error.png`
- **Supporting Page Evidence:** `../screenshot/original/contact-fullpage-overview.png`

### TEST-016 — Restricted Clickable Area on Category Cards

- **Page:** Categories
- **Category:** Functionality / User Experience
- **Expected:** Clicking anywhere within a category card should navigate to the corresponding category.
- **Actual:** Navigation works only when clicking directly on the category text. Clicking the surrounding card area does nothing.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/categories-fullpage-overview.png`
- **Annotated Evidence:** `../screenshot/annotated/categories-fullpage-overview-annotated.png`

### TEST-017 — Incorrect About Page Breadcrumb Label

- **Page:** About Us
- **Category:** Navigation / User Experience
- **Expected:** Breadcrumb should identify the current page as "About Us".
- **Actual:** Breadcrumb displays "Home / Page". Only "Home" is clickable and navigates to the homepage.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/aboutUs-fullpage-overview.png`
- **Annotated Evidence:** `../screenshot/annotated/aboutUs-breadcrumb-heading-mismatch.png`

---

## Blog Page Testing

### TEST-018 — Blog Login Functionality

- **Page:** Blog / Login
- **Category:** Functionality / Authentication
- **Expected:** Registered users should be able to access the login page and authenticate.
- **Actual:** Login page opens and the login process works with registered accounts.
- **Status:** PASS
- **Evidence:** `../screenshot/original/login-fullpage-overview.png`

### TEST-019 — Blog User Registration

- **Page:** Blog / Registration
- **Category:** Functionality / Authentication
- **Expected:** Visitors should be able to access the registration page and register an account.
- **Actual:** Registration page opens and registered accounts can be created.
- **Status:** PASS
- **Evidence:** `../screenshot/original/register-fullpage-overview.png`

### TEST-020 — Password Reset Email Failure

- **Page:** Blog / Forgot Password
- **Category:** Functionality / Authentication / Backend
- **Expected:** Submitting a registered email address should send a password reset link.
- **Actual:** Submission produces a Swift_TransportException with HTTP 503. The server reports that local sendmail is disabled.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/forgotPassword-page.png`
- **Error Evidence:** `../screenshot/original/resetPassword-error.png`

### TEST-021 — Blog Article Navigation

- **Page:** Blog
- **Category:** Navigation / Functionality
- **Expected:** Each Read More button should open its corresponding article.
- **Actual:** All tested Read More buttons successfully open their respective articles in the current tab.
- **Status:** PASS
- **Evidence:** `../screenshot/original/blog-fullpage-overview.png`
- **Supporting Evidence:** `../screenshot/original/single-blog-fullpage.png`

### TEST-022 — Blog Category Filtering

- **Page:** Individual Blog Article
- **Category:** Navigation / Functionality
- **Expected:** Selecting a category should display relevant blog content.
- **Actual:** Selecting a category successfully opens the corresponding filtered results.
- **Status:** PASS

### TEST-023 — Individual Blog Tag URL Generation

- **Page:** Individual Blog Articles
- **Category:** Navigation / Functionality
- **Expected:** Each tag should link to a valid results page using its correct tag slug.
- **Actual:** Some tag links generate URLs with an unwanted leading hyphen. For example, `-sustainability` and `-climate-action` return no results, whereas the corresponding clean slugs work.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/-sustainability-tag.png`, `../screenshot/original/sustainability-tag.png`, `../screenshot/original/-climate-action-tag.png`, `../screenshot/original/climate-tag.png`

### TEST-024 — Project Vikas Tag Link Structure

- **Page:** Project Vikas Blog Article
- **Category:** Navigation / Functionality
- **Expected:** Each post tag should have an individual link leading to its corresponding tag results.
- **Actual:** The entire tag section behaves as one clickable link. Its URL combines all hashtags into a single malformed URL, and the destination returns a 404 error.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/projectVikas-tags.png`, `../screenshot/original/projectVikas-tags-error404.png`

### TEST-025 — Inconsistent Blog Post Tag Presentation

- **Page:** Individual Blog Articles
- **Category:** Visual Design / Consistency
- **Expected:** Post tags should follow a consistent visual presentation and interaction pattern across articles.
- **Actual:** Project Vikas displays tags together in one container, other posts display individual tag boxes, and Animal Protection displays an empty Post Tags section.
- **Status:** Improvement Required
- **Evidence:** `../screenshot/original/projectVikas-tags.png`, `../screenshot/original/MissionLife-tags.png`, `../screenshot/original/Animal Protection-tag.png`
- **Annotated Evidence:** `../screenshot/annotated/projectVikas-tags-annotated.png`, `../screenshot/annotated/MissionLife-tags-annotated.png`, `../screenshot/annotated/Animal Protection-tag-annotated.png`

### TEST-026 — Password Change Without Current-Password Verification

- **Page:** My Profile / Edit Profile
- **Category:** Security / Authentication
- **Expected:** Changing an account password should require verification of the current password or equivalent recent reauthentication.
- **Actual:** The password was successfully changed without entering the current password. After logging out, the old password no longer worked, while the new password successfully authenticated the account.
- **Status:** FAIL
- **Evidence:** `../screenshot/original/myProfile-fullpage-overview.png`
