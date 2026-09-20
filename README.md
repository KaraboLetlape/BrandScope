# BrandScope — Part 2: CSS Styling and Responsive Design

## Student Information

- **Student Name:** Karabo Letlape
- **Student Number:** ST10514955
- **Course:** Diploma in Software Development
- **Module:** WEDPOE
- **Project:** BrandScope Website
- **Part:** Part 2 — Designing the Visuals: CSS Styling and Responsive Design

---

## 1. Project Overview

BrandScope is a South African streetwear resale website created to showcase curated branded clothing and accessories. The original Part 1 project included a homepage, category sections, featured products and individual product pages.

Part 2 builds on that foundation by introducing a dedicated external stylesheet, improved visual consistency, CSS Grid/Flexbox layouts, interactive states and responsive behaviour for desktop, tablet and mobile screen sizes.

---

## 2. Part 1 Feedback / Corrections

The Part 1 implementation was reviewed while preparing Part 2. The following technical improvements were made:

1. Consolidated the website styling into the external `css/style.css` file.
2. Removed duplicated/invalid CSS content that had been embedded inside the homepage markup.
3. Removed local Windows `file:///` links and replaced them with relative website links so the project works when uploaded to GitHub.
4. Corrected the JavaScript reference to the existing `javascript/script.js` file.
5. Corrected navigation so the same relative links work from the homepage and product pages.
6. Improved semantic organisation of the category and product sections.
7. Added responsive image markup using `<picture>`, `srcset` and `sizes`.
8. Added keyboard focus states and clearer interactive states for links, buttons and form controls.

> **Note:** The original lecturer's written Part 1 feedback was not included in the uploaded project archive. Therefore, the changelog records the concrete technical corrections made during the Part 2 revision rather than inventing lecturer comments.

---

## 3. CSS Styling for Desktop Solution

### 3.1 External Stylesheet

All website pages now link to:

```text
css/style.css
```

The stylesheet contains the shared visual system for the homepage and individual product pages.

### 3.2 Base Styles and CSS Reset

The stylesheet includes:

- Universal `box-sizing` reset.
- Removal of inconsistent default heading and paragraph margins.
- Responsive image defaults.
- Shared CSS custom properties for colours, spacing, width and shadows.
- A consistent Arial/Helvetica font stack.
- Base font size and line-height.
- Keyboard focus styling.

### 3.3 Typography

Typography uses:

- `font-family`
- `font-size`
- `font-weight`
- `line-height`
- `letter-spacing`
- `clamp()` for responsive heading sizes

This creates a consistent hierarchy between hero text, section headings, product information and supporting text.

### 3.4 Layout

The website uses CSS Grid and Flexbox.

Examples include:

- Four-column desktop category grid.
- Four-column desktop product grid.
- Two-column desktop About section.
- Two-column desktop Contact section.
- Two-column desktop product detail layout.
- Flexbox navigation and footer groups.

---

## 4. Visual Styling

The BrandScope visual system uses a black, white and grey streetwear-inspired colour palette.

Visual CSS includes:

- `background-color`
- `color`
- `border`
- `border-radius`
- `box-shadow`
- gradients
- image overlays
- transitions
- transforms

Interactive states include:

- `:hover`
- `:focus-visible`
- `:focus`
- `:active`

For example, product and category cards move slightly upward on hover, while navigation links receive an animated underline.

---

## 5. Responsive Design

### 5.1 Breakpoints

The stylesheet uses three practical layout ranges:

| Screen type | Breakpoint | Main changes |
|---|---:|---|
| Desktop | Above 1000px | Multi-column grids and two-column content layouts |
| Tablet | 641px–1000px | Two-column grids and stacked content sections |
| Mobile | 640px and below | Single-column grids, wrapped navigation and smaller spacing/type |

### 5.2 Relative Units

Relative and responsive units are used throughout the stylesheet, including:

- `%`
- `rem`
- `em`
- `vw`
- `vh`
- `svh`
- `clamp()`

These values allow spacing and typography to adapt to the available viewport.

### 5.3 Responsive Images

The category images use:

- `<picture>`
- `<source media>`
- `srcset`
- `sizes`

Mobile-sized image variants were created for the category assets so smaller screens can request a more appropriate image resource.

---

## 6. Browser Developer Tools Testing

The website should be tested using Chrome Developer Tools.

Recommended viewport evidence:

1. **Desktop:** 1440 × 900
2. **Tablet:** approximately 768 × 1024
3. **Mobile:** approximately 390 × 844

For each viewport, verify:

- Navigation remains usable.
- Text does not overflow.
- Category cards change from four columns to two and then one.
- Product cards change from four columns to two and then one.
- About and Contact sections stack on smaller screens.
- Product detail pages stack correctly.
- Images remain contained within their cards.
- Form controls remain usable.
- Hover/focus interactions remain accessible.

### Screenshot Evidence

Save screenshots in:

```text
screenshots/
├── desktop-1440.png
├── tablet-768.png
└── mobile-390.png
```

These screenshots should be inserted into this README after testing in Chrome Developer Tools.

---

## 7. Updated Project Structure

```text
BRANDSCOPE/
│
├── brandscope.html
├── product-Aape.html
├── product-C.P company.html
├── product-Nike.html
├── product-stussy.html
├── product-tnf supreme.html
│
├── css/
│   └── style.css
│
├── images/
│   ├── Beanies/
│   ├── Caps/
│   ├── Hoodies/
│   ├── Jackets/
│   ├── Pants/
│   ├── Sweaters/
│   └── T-Shirts/
│
├── javascript/
│   └── script.js
│
├── screenshots/
│   └── [desktop/tablet/mobile evidence]
│
└── README.md
```

---

## 8. Changelog

### Version 2.0 — Part 2

- Created and implemented a single external stylesheet at `css/style.css`.
- Added a CSS reset and shared CSS custom properties.
- Standardised typography, spacing and colour usage.
- Rebuilt desktop layouts using CSS Grid and Flexbox.
- Added responsive desktop, tablet and mobile breakpoints.
- Added relative units including `rem`, `%`, `vw`, `vh` and `clamp()`.
- Added hover, focus and active interaction states.
- Improved category-card image behaviour and overlays.
- Added responsive `<picture>`, `srcset` and `sizes` markup to category images.
- Generated smaller mobile image variants for category assets.
- Corrected local `file:///` navigation links so the website works when hosted in a repository.
- Corrected the JavaScript file reference.
- Corrected navigation between the homepage and product pages.
- Improved product detail layouts for smaller screens.
- Improved contact form styling and focus behaviour.
- Added reduced-motion support for users who prefer less animation.
- Updated README documentation for Part 2.
- Added testing instructions and required screenshot evidence locations.

---

## 9. Suggested Git Commit Messages

Use descriptive commits such as:

```text
feat: add external CSS stylesheet for BrandScope
style: improve desktop layout and typography
feat: add responsive tablet and mobile breakpoints
feat: add responsive images with srcset and picture
fix: replace local file URLs with relative links
fix: correct JavaScript reference
docs: update README for Part 2
test: document desktop tablet and mobile testing
```

---

## 10. References

The following technical references were used to guide the CSS and responsive implementation:

1. MDN Web Docs — CSS.
2. MDN Web Docs — CSS Grid Layout.
3. MDN Web Docs — Flexbox.
4. MDN Web Docs — CSS Media Queries.
5. MDN Web Docs — Responsive images.
6. MDN Web Docs — `<picture>`, `srcset` and `sizes`.

External product and image sources used for the original BrandScope content remain part of the project's existing research/materials and should be retained according to the referencing requirements for the module.

---

## 11. Submission Checklist

Before submitting Part 2:

- [ ] Confirm all HTML pages open correctly.
- [ ] Confirm all pages use `css/style.css`.
- [ ] Confirm product links work.
- [ ] Test desktop layout.
- [ ] Test tablet layout.
- [ ] Test mobile layout.
- [ ] Capture desktop screenshot.
- [ ] Capture tablet screenshot.
- [ ] Capture mobile screenshot.
- [ ] Place screenshots in the `screenshots/` folder.
- [ ] Update the README with the screenshot evidence.
- [ ] Commit the changes with descriptive commit messages.
- [ ] Push the changes to the remote GitHub repository.
- [ ] Copy the GitHub repository URL into the LMS submission.

## 12. GitHub Repository

**Repository URL:** Add the existing BrandScope GitHub repository URL here before submission.
