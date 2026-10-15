Project title
Lae Urban Youths Bike Workshop



Purpose
The same three-page site from Assessment 2, restyled with a hand-writtenCSS3 design system and made fully responsive. Visitors can learn about theworkshop, browse services/course prices, check hours, and book via the form.

Target audience
Local adult riders, parents of young riders, students and budget-consciouscommuters in the Riverton area.

Responsive design
Mobile-first: base styles target \~320–480 px; all media queries are min-width.
Breakpoints: 40em (\~640 px, tablet), 56em (\~896 px, desktop),72em (\~1152 px, wide). Em-based so they track user font-size zoom.
Mobile changes are structural, not just shrink-to-fit: the nav stacks thenbecomes a row; card grids reflow from 1 → 2 → 3+ columns; the contact formand info sidebar sit side by side only on wide screens; wide tables scrollhorizontally inside .table-wrap instead of squashing.
Flexbox usage (one-dimensional layout)
body flex column → sticky footer on short pages.
.header-inner → responsive nav bar: stacked/centred on mobile, brand-left/nav-right row from 40em.
.brand a, .option, .footer-nav ul → icon/text alignment, checkbox/radiorows, wrapping footer links.
CSS Grid usage (two-dimensional layout)
.card-grid → "What we do" / "Get involved" / services jump-nav usingrepeat(auto-fit, minmax(min(100%, 16rem), 1fr)).
.media-split → home intro: text column + explicitly placed figure column.
.split.contact-split → booking form (1.4fr) beside info sidebar (1fr) at 72em.
.footer-grid → three aligned footer columns on wide screens.
.grid-2 → two-column "Your details" form fields (legend kept outside thegrid intentionally — fieldset-as-grid breaks legends in some browsers).
Design system
:root custom properties define the colour palette (WCAG AA-checked),fluid clamp() type scale, spacing scale, radii, shadows, container width,easing tokens. Georgia/serif display headings + system sans body — no webfonts.

File list
index.html, services.html, contact.html
css/style.css — single organised stylesheet (tokens → reset → type →layout → components → utilities → media queries → a11y). Kept as one filebecause the project is small enough that a base/layout split would add asecond request without improving clarity.
images/ — workshop-benches(-480/-1400).jpg, course-participant.jpg,donated-bikes.jpg, workshop-entrance.jpg
Technologies used
HTML5, hand-written CSS3 (Flexbox, Grid, custom properties, clamp/minmax,media queries). No JavaScript, no frameworks, no page builders.

How to run
Open index.html locally, or publish via GitHub Pages.

AI Use Declaration
This project was developed with substantial assistance from chat.z.ai, a generative AI conversational assistant. AI was used to draft the HTML, CSS and JavaScript code, the page content, and supporting documentation (README, summary, testing plan). My own contribution consisted of selecting and adding the photographic assets, validating and debugging the code with the W3C validators, performing all browser, responsive and accessibility testing, and studying the generated code until I could explain every design and accessibility decision.

