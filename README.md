# BrandScope — Part 3: Interactive Features, SEO and Deployment

## Student and project details
- **Student:** Karabo Letlape
- **Student number:** ST10514955
- **Module:** WEDPOE — Web Development (Introduction)
- **Project:** BrandScope
- **Assessment:** Part 3

## 1. Project overview
BrandScope is a South African streetwear resale showcase based in Johannesburg. It presents curated branded clothing and accessories, product details, contact information and ways for visitors to enquire about products. Part 3 extends the responsive Part 2 website with functional interaction, search, an image lightbox, an interactive map, enquiry handling, accessibility improvements and SEO metadata.

## 2. Part 2 feedback and improvements
The Part 2 archive did not contain the lecturer's written feedback. This document therefore does not invent feedback. The following implementation improvements were made while extending the project:
- Preserved the existing BrandScope visual identity, homepage, five product pages, stylesheet and original product photography.
- Converted image filenames to lowercase, descriptive, hyphen-separated names and updated their references.
- Added descriptive alternative text to content images and lazy loading to product images.
- Replaced decorative product image backgrounds in the featured collection with semantic image elements.
- Added accessible labels, live status feedback and keyboard-operable controls.
- Kept the responsive CSS layout and added styles for the new Part 3 features.

## 3. Interactive elements
- Header search icon scrolls to and focuses the product search field.
- Product cards include an **Add to Enquiry** control.
- The enquiry bag opens and closes, displays selected products, supports removing an item, updates its item count and creates a WhatsApp enquiry message.
- Navigation links and product links connect the homepage and product detail pages.
- Product/category images open in the image viewer.

## 4. Interactive map
The Contact section includes a responsive, embedded Google Maps view for Johannesburg, South Africa. The map is loaded in an iframe with a descriptive title and lazy loading. An internet connection is required for the embedded map to load.

## 5. Gallery lightbox
The image viewer supports:
- Opening images from the category grid, featured products and individual product pages.
- Previous and next image navigation on the homepage.
- Closing with the close button, by clicking the backdrop, or with the Escape key.
- Left and right arrow-key navigation.
- Descriptive alternative text and captions.
- Focus return to the image that opened the viewer.

## 6. Dynamic content and search
The product search filters the five featured product cards while the visitor types. Matching is case-insensitive and searches the visible product and brand text. A live status message reports the number of matching products. The Clear button restores all products.

## 7. Search engine optimisation (SEO)
Every HTML page includes:
- A unique, descriptive title.
- A page-specific meta description.
- Relevant meta keywords.
- Author and robots metadata.
- Open Graph title, description and type metadata.

Image improvements:
- Descriptive, lowercase, hyphenated filenames.
- Meaningful `alt` text for content images.
- `loading="lazy"` on product/detail images where appropriate.

Note: meta keywords are included because they appear in the assessment rubric, although major search engines generally do not use the keywords meta tag as a ranking signal. Update the canonical URL and social preview image metadata after the final GitHub Pages address is known.

## 8. Enquiry form functionality and validation
The contact form requests:
- Full name.
- Email address.
- Optional phone number.
- Enquiry type.
- Message.

JavaScript validates the required fields, email format, optional phone format and message length. Invalid fields receive an inline error message, an `aria-invalid` state and focus when submission fails. A valid submission builds a pre-filled email addressed to `brandscope.za@gmail.com` using the visitor's default email application.

**Important technical limitation:** this static HTML/CSS/JavaScript project has no server-side email service or database. The form does not silently claim that an email was sent; it opens the visitor's email application and the visitor must press Send. A backend or form service would be needed for automatic server-side submission.

## 9. Contact controls and process
The website provides:
- Email link using `mailto:brandscope.za@gmail.com`.
- WhatsApp links for the existing BrandScope contact numbers.
- Instagram link to `@brandscope.za`.
- Johannesburg location and embedded map.
- Product-specific WhatsApp purchase/enquiry links.
- Enquiry bag WhatsApp message containing selected product names and displayed prices.

External links open in a new tab where appropriate. The visitor can choose the contact channel that suits their enquiry.

## 10. Testing checklist
Run the project from the `brandscope.html` homepage using a local development server (recommended) or open it in a browser. Test the following:

### Desktop, tablet and mobile
- [ ] Desktop layout at approximately 1440 × 900.
- [ ] Tablet layout at approximately 768 × 1024.
- [ ] Mobile layout at approximately 390 × 844.
- [ ] Navigation, category cards and product cards remain usable.
- [ ] No horizontal overflow or clipped text.
- [ ] Map resizes within the contact section.

### Interactive functionality
- [ ] Header search icon focuses the search field.
- [ ] Search for `Nike`, `Stussy`, `hoodie` and a term with no results.
- [ ] Clear search restores all products.
- [ ] Add multiple products to the enquiry bag.
- [ ] Remove an item and check the count updates.
- [ ] Enquiry bag WhatsApp link includes selected products.
- [ ] Open a category/product image in the lightbox.
- [ ] Test previous/next, Escape, backdrop and close controls.
- [ ] Test the product image viewer on each product detail page.

### Forms and contact
- [ ] Submit the form empty and confirm inline errors appear.
- [ ] Test an invalid email address.
- [ ] Test a phone number and the optional blank phone field.
- [ ] Test a message shorter than 10 characters.
- [ ] Submit valid information and confirm a pre-filled email is created.
- [ ] Check email, WhatsApp and Instagram contact links.

### SEO and technical checks
- [ ] Each page has a unique title and meta description.
- [ ] All content images have useful alt text.
- [ ] Confirm renamed image files load without 404 errors.
- [ ] Check browser console for JavaScript errors.
- [ ] Check all internal product and navigation links.
- [ ] Confirm the map loads with an internet connection.

Capture real screenshots of the completed desktop, tablet and mobile tests and add them to a `screenshots/` folder before submission. Do not include screenshots of features that have not been tested.

## 11. Project structure
```text
BrandScope_Part2_Merged/
├── brandscope.html
├── product-Aape.html
├── product-C.P company.html
├── product-Nike.html
├── product-stussy.html
├── product-tnf supreme.html
├── css/
│   └── style.css
├── javascript/
│   └── script.js
├── images/
│   ├── Beanies/
│   ├── Caps/
│   ├── Hoodies/
│   ├── Jackets/
│   ├── Pants/
│   ├── Sweaters/
│   └── T-Shirts/
├── README.md
├── CHANGELOG.md
└── .nojekyll
```

## 12. GitHub commits
Use meaningful commits as each feature is completed. Suggested commands:

Create multiple descriptive commits, stage the related files, and push the history:

```bash
git status
git add brandscope.html javascript/script.js css/style.css
git commit -m "feat: add interactive search enquiry bag map and form"

git add product-*.html
git commit -m "feat: add product page SEO and image lightbox support"

git add images README.md CHANGELOG.md .nojekyll
git commit -m "docs: optimise image assets and complete Part 3 documentation"

git log --oneline
git push origin main
```

If a command reports that there is nothing to commit, check `git status` and continue. The commits must be pushed to the existing GitHub repository for the online marking evidence.

## 13. Deployment — GitHub Pages
The website is a static website and can be hosted with GitHub Pages.

1. Push the complete project to the existing GitHub repository.
2. Open the repository on GitHub.
3. Select **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish the site.
7. Open the published URL and test the homepage, all product pages, images, search, enquiry bag, lightbox, map and form.
8. Add the final published URL to this README and set the canonical URL in the homepage to that real URL.

The project files are prepared for static hosting, but deployment is not complete until the repository owner enables Pages and verifies the published URL.

## 14. References
- MDN Web Docs. (n.d.). *HTML: HyperText Markup Language*. https://developer.mozilla.org/en-US/docs/Web/HTML
- MDN Web Docs. (n.d.). *The meta element*. https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
- MDN Web Docs. (n.d.). *HTML forms*. https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms
- MDN Web Docs. (n.d.). *Constraint validation*. https://developer.mozilla.org/en-US/docs/Web/HTML/Constraint_validation
- MDN Web Docs. (n.d.). *JavaScript*. https://developer.mozilla.org/en-US/docs/Web/JavaScript
- MDN Web Docs. (n.d.). *EventTarget.addEventListener()*. https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener
- MDN Web Docs. (n.d.). *Responsive images*. https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images
- Google Maps Platform. (n.d.). *Maps Embed API*. https://developers.google.com/maps/documentation/embed
- GitHub Docs. (n.d.). *What is GitHub Pages?*. https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages

Product names and trademarks remain the property of their respective owners. BrandScope is an independent resale/showcase project and does not claim affiliation with the brands displayed.

## 15. Submission readiness
- [x] Part 2 website retained and extended.
- [x] Interactive product search.
- [x] Enquiry bag and WhatsApp enquiry link.
- [x] Interactive map embed.
- [x] Image lightbox.
- [x] SEO metadata on homepage and product pages.
- [x] Descriptive image filenames and alt text.
- [x] Enquiry form validation and email hand-off.
- [x] README and changelog updated.
- [ ] Browser testing and screenshots captured by the student.
- [ ] Git commits pushed to the existing GitHub repository.
- [ ] GitHub Pages enabled and published URL verified.
