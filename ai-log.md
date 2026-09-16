---- Prompt ----

You are assisting with a small, public static portfolio website.

Project context:
- Purpose: present a student's skills and projects to internship reviewers.
- Existing system: an HTML/CSS/JavaScript portfolio template.
- Allowed changes: content, styling, and small front - end corrections only.
- Do not add: a backend, login system, analytics tracker, or external data
  collection.

Acceptance criteria:
1. All generic references on the template site must be replaced with specific information based on my resume.
2. All links must lead to the correct destination.
3. The site must include my current roles, interests, and a couple of projects.
4. Must look nice on both horizontally and vertically oriented screens.
5. It should include links where applicable, like to my LinkedIn and project sites.

Constraints:
- Do not invent education, work history, awards, links, or technical skills.
- Preserve required license and attribution.
- Keep the site usable on mobile screens.
- Maintain readable contrast, keyboard navigation, meaningful link text,
  and useful image alternative text.
- Do not expose private information.

First provide:
1. A file - by - file implementation plan.
2. Any Assumptions or risks.
3. A proposed test checklist.
4. Any questions that must be answered before implementation.

Do not modify files until the plan is reviewed.





---- AI Response ----

## 1. File-by-file implementation plan

I’ll tailor the exact plan after reviewing the repository and resume. For a typical static portfolio, the work would be:

### `index.html` or other HTML pages

- Replace all template names, biographies, roles, headings, calls to action, project descriptions, and placeholder text with resume-supported information.
- Include:
    - A concise introduction
    - Current roles
    - Professional or technical interests
    - A skills section
    - A small selection of projects
    - Education and experience where appropriate
    - LinkedIn, project, and other verified links
- Remove unused generic sections rather than filling them with invented content.
- Correct page navigation and external-link destinations.
- Improve semantic structure with landmarks and logical heading levels.
- Ensure controls and links are keyboard accessible and have meaningful labels.
- Add useful alternative text to informative images; use empty alternative text for purely decorative images.
- Avoid publishing private details such as a home address, personal phone number, or unnecessary identifiers.
- Preserve all required licensing and attribution.

### Main stylesheet, such as `css/style.css`

- Adapt the existing visual system without replacing the template architecture.
- Improve typography, spacing, hierarchy, and consistency.
- Ensure sufficient foreground/background contrast.
- Add or correct responsive layouts for:
    - Narrow portrait phones
    - Landscape phones
    - Tablets
    - Desktop and wide screens
- Prevent horizontal overflow, clipped content, oversized headings, and overlapping navigation.
- Preserve visible keyboard-focus indicators.
- Respect reduced-motion preferences when animations are present.
- Ensure hover-only effects also work with keyboard focus and touch input.

### JavaScript files, such as `js/main.js`

- Make only small front-end corrections.
- Repair mobile navigation, section scrolling, filters, or other existing template interactions if needed.
- Avoid adding tracking, remote data collection, accounts, or backend dependencies.
- Confirm interactions work by keyboard and do not depend solely on pointer hover.
- Remove obsolete code only when it is clearly unused and removal will not break template behavior.

### Image and media assets

- Replace generic template images with user-provided or already-authorized assets.
- Optimize large files for web delivery while preserving acceptable quality.
- Use suitable dimensions or responsive-image markup where practical.
- Avoid publishing images containing private or sensitive information.
- Retain attribution for assets whose licenses require it.
- If no project image is available, use a text-led layout or an existing licensed visual rather than inventing project screenshots.

### Site metadata and supporting files

Depending on what exists:

- Update the page title, description, social-sharing metadata, favicon references, and site author information.
- Update the résumé link only if a public résumé file is provided and approved for publication.
- Check `README.md`, license files, attribution comments, and template credits; preserve all required notices.
- Review deployment/configuration files only for broken static paths—not to add services, analytics, or data collection.
- Check `404.html`, manifest files, or additional pages for leftover template references.

### Repository-wide review

- Search all source files for generic template names, sample companies, placeholder links, dummy projects, lorem ipsum, default social handles, and unused stock content.
- Verify relative paths and capitalization, including behavior on case-sensitive hosting.
- Keep changes limited to content, styling, accessibility, responsive behavior, and small front-end fixes.

## 2. Assumptions and risks

### Assumptions

- The existing project files and resume will be provided for review.
- Resume content is approved as the authoritative source for biography, education, experience, roles, projects, and skills.
- Only explicitly supplied or verifiable URLs will be published.
- Existing template libraries will remain unless they are broken, unnecessary, insecure, or incompatible with the requested changes.
- The site will continue to be deployed as a static website.
- Current template license and attribution terms permit customization.

### Risks

- **Missing links:** A resume may name LinkedIn, GitHub, or projects without including exact URLs. I will not infer handles or destinations.
- **Private information:** The resume may contain an address, phone number, private email address, or internal links unsuitable for a public site. These require an explicit publication decision.
- **Conflicting information:** Repository content and resume details may disagree. The resume will be treated as authoritative unless instructed otherwise.
- **Limited project evidence:** Some projects may lack descriptions, screenshots, repositories, or live sites. I will include only supported facts and available links.
- **Unlicensed media:** Resume or repository images may not have clear publication rights. Unverified assets should not be added.
- **Template dependencies:** Removing apparent placeholders or scripts could affect navigation or layout. Existing behavior should be tested before deletion.
- **Responsive complexity:** Highly decorative template sections can behave poorly in landscape or on narrow screens and may need simplification.
- **Outdated “current” roles:** A dated resume may not accurately identify current roles. This must be confirmed before the site describes them as current.
- **Automated accessibility limits:** Automated checks cannot establish full accessibility; keyboard and visual review are still necessary.

## 3. Proposed test checklist

### Content

- [ ] Every generic name, role, biography, project, company, quote, statistic, and call to action has been replaced or removed.
- [ ] Every factual claim is supported by the supplied resume or explicit user information.
- [ ] Current roles are accurately identified.
- [ ] Interests are included using user-approved wording.
- [ ] At least two supported projects are presented, if the source material provides them.
- [ ] No education, employment, awards, links, or technical skills have been invented.
- [ ] No private information is exposed.
- [ ] Required license notices and attribution remain intact.

### Links

- [ ] Header and in-page navigation links reach the intended sections.
- [ ] LinkedIn and other profile links use exact approved URLs.
- [ ] Project repository and live-site links reach the correct projects.
- [ ] Email links, if included, use an approved public address.
- [ ] No placeholder `#`, example-domain, or template-author links remain unless intentionally required.
- [ ] Relative paths work from the deployed site location.
- [ ] Link text describes the destination—for example, “View ProjectName source code,” not “Click here.”
- [ ] External links do not create inaccessible or surprising behavior.

### Responsive layout

Test at minimum:

- [ ] 320 × 568 portrait
- [ ] 375 × 667 portrait
- [ ] 667 × 375 landscape
- [ ] 768 × 1024 tablet portrait
- [ ] 1024 × 768 tablet landscape
- [ ] 1440 × 900 desktop
- [ ] A wide desktop viewport

At each size:

- [ ] No unintended horizontal scrolling.
- [ ] Text remains readable without zooming.
- [ ] Navigation remains usable.
- [ ] Images scale without distortion.
- [ ] Cards, buttons, and headings do not overlap or clip.
- [ ] Long URLs, project names, and role titles wrap safely.
- [ ] Touch targets are reasonably sized and separated.
- [ ] Important content is not hidden because of screen orientation.

### Accessibility and interaction

- [ ] The document has a descriptive title and valid language declaration.
- [ ] Heading levels form a logical hierarchy.
- [ ] Header, navigation, main content, and footer use semantic landmarks.
- [ ] All interactive elements are reachable and operable by keyboard.
- [ ] Focus indicators are clearly visible.
- [ ] Focus order follows the visual and reading order.
- [ ] A keyboard user is not trapped in the mobile menu or other interface.
- [ ] Informative images have useful alternative text.
- [ ] Decorative images use empty alternative text or appropriate CSS treatment.
- [ ] Text and controls meet appropriate Web Content Accessibility Guidelines contrast targets.
- [ ] Information is not conveyed by color alone.
- [ ] Animation respects `prefers-reduced-motion`.
- [ ] The page remains usable at 200% browser zoom.
- [ ] Browser-console review shows no significant errors.

### Technical and deployment

- [ ] HTML and CSS validation reveals no material errors.
- [ ] JavaScript initializes without runtime errors.
- [ ] All local files load without 404 errors.
- [ ] Asset paths work with case-sensitive hosting.
- [ ] No backend, login, analytics, tracker, cookies, or external data collection has been added.
- [ ] No secrets, unpublished documents, source maps containing sensitive data, or private contact data are committed.
- [ ] Existing license and attribution files/comments are preserved.
- [ ] A production/deployed build receives a final link and layout check.

## 4. Questions that must be answered before implementation

1. **Please provide the portfolio project files or repository and the resume to use as the source of truth.**
2. **Which roles are current as of September 2026, and what exact interests should the site emphasize?**
3. **What are the exact approved public URLs for LinkedIn and any GitHub, project repository, live demo, or personal-domain links?**
4. **Which two or more projects should receive priority, and are their descriptions and technologies documented in the resume or repository?**
5. **Which contact details, if any, are approved for public display?** In particular, should the site publish an email address, résumé PDF, or neither?
6. **Are all supplied profile photos, project images, logos, and screenshots authorized for public use?**
7. **Where will the static site be hosted, and does it use a root domain or subdirectory?** This affects asset and navigation paths.

No files will be modified until this plan has been reviewed and the required source materials and answers are available.