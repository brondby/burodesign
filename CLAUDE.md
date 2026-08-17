# Buro Design Landing Page — Claude Instructions

## IMPORTANT

Before making Next.js-specific changes, read and follow the Next.js agent instructions in `AGENTS.md`.

Do not modify `AGENTS.md`.

This project uses Next.js 16.3.1.

When Next.js-specific behaviour is unclear, inspect the relevant documentation under:

`node_modules/next/dist/docs/`

Do not rely on assumptions based on older Next.js versions.

---

# Project Purpose

This project is a modern rebuild of the existing single-page Buro Design landing page:

https://burodsin.com

The original page was created approximately 10 years ago.

This is a SINGLE-PAGE STATIC LANDING PAGE.

It is NOT an ecommerce application.

The future main project will be `burotech.com`.

Do not build ecommerce functionality in this project.

The purpose of this project is to provide a modern, fast, responsive gateway page that directs visitors to the existing Buroteck, Buroseat and related product/application websites.

---

# Technology

Use:

- Next.js 16.3.1
- React
- TypeScript
- Tailwind CSS
- Motion only where useful

Use the App Router.

Use static export.

Do NOT introduce:

- Docker
- FastAPI
- Laravel
- Backend
- Database
- API
- CMS
- WordPress
- jQuery
- Bootstrap
- WebSlideMenu
- Font Awesome
- unnecessary UI frameworks
- unnecessary animation libraries

This is intentionally a lightweight project.

---

# Existing Website

The existing website is:

https://burodsin.com

The current source code has been provided to the project owner and should be treated as the reference for the existing functionality.

The new site should modernise the implementation while preserving the important visual and interactive identity of the original.

Do NOT copy the old HTML/CSS architecture.

Rebuild the functionality using modern React, Tailwind CSS and browser APIs.

---

# Existing Eight Interactive Tiles

The original landing page contains eight primary interactive tiles.

Each tile has:

1. Normal visual state.
2. Hover visual state.
3. Destination URL.
4. Unique piano-note sound.

Preserve this concept.

## Tile 1 — Buroteck

Title:

Buroteck

URL:

https://www.buroteck.com/

Image:

`buroteck-dubai.png`

Sound:

`piano_A_sharp.mp3`

---

## Tile 2 — Ergonomic Workstation

Title:

Ergonomic Workstation

URL:

http://buroteck.com/making-technical-furniture/broadcast/

Image:

`buroteck-office-design-01.png`

Sound:

`piano_B.mp3`

---

## Tile 3 — Workplace Interior Design

Title:

Workplace Interior Design

URL:

http://buroteck.com/making-technical-furniture/

Image:

`buroteck-workplace-design.png`

Sound:

`piano_C_sharp.mp3`

---

## Tile 4 — Control Desk

Title:

Control Desk

URL:

http://www.buroteck.com/making-technical-furniture/control-rooms/

Image:

`buroteck-office-design.png`

Sound:

`piano_D.mp3`

---

## Tile 5 — Contact Us

Title:

Contact Us

URL:

http://www.buroteck.com/contact-buroteck/

Image:

`buroteck-contact-us.png`

Sound:

`piano_E.mp3`

---

## Tile 6 — Ergonomic Chairs

Title:

Ergonomic Chairs

URL:

https://buroseat.com/ergo-chairs/

Image:

`ergonomic-chairs-Dubai.png`

Sound:

`piano_F.mp3`

---

## Tile 7 — Sit Stand Desk

Title:

Sit Stand Desk

URL:

https://buroteck.com/sit-stand-desk

Image:

`buroteck-electric-sit-stand-desk-dubai.png`

Sound:

`piano_G_sharp.mp3`

---

## Tile 8 — Large Desk Converters

Title:

Large Desk Converters

URL:

https://buroteck.com/sit-stand-desk/desk-converter-ergoboard-large/

Image:

`desk-converter-buroteck.png`

Sound:

`piano_middle_C.mp3`

---

# IMPORTANT — Preserve Existing URLs

The URLs above are part of the existing Buro website ecosystem.

Do not invent replacement URLs.

Do not change URLs simply because another URL appears more modern.

Do not automatically convert HTTP links to HTTPS.

Preserve the URLs unless the project owner explicitly instructs otherwise.

---

# Existing Tile Images

The original CSS uses images as two-state sprites.

For example:

`background-size: 200%`

with:

`background-position: 0 0`

for the normal state and:

`background-position: 100% 0`

for the hover state.

Therefore an image such as:

`buroteck-dubai.png`

may contain:

NORMAL | HOVER

side-by-side in a single image.

Inspect the actual image assets before modifying or replacing them.

Do not assume every image is a single-state image.

If the existing images have sufficient resolution, reuse them.

If an image is too low-resolution for the new design, identify it and report the issue rather than silently introducing blurry output.

---

# Tile Interaction

Rebuild the old sprite interaction using modern React/CSS.

Do NOT reproduce the old jQuery or inline JavaScript.

Requirements:

- Preload important visual assets.
- No network request should occur when the user first hovers.
- Hover response must feel immediate.
- Preserve the normal/hover visual states.
- Preserve the original visual concept.
- Maintain correct aspect ratio.
- Do not distort images.
- Use CSS transitions where useful.
- Keep JavaScript minimal.

Touch devices do not have true hover.

The experience must therefore work correctly on touch devices without relying on hover.

---

# Audio

The original website uses eight different piano notes.

Preserve the eight-note mapping.

Do NOT replace them with one generic sound.

The sounds are:

- Buroteck → piano A sharp
- Ergonomic Workstation → piano B
- Workplace Interior Design → piano C sharp
- Control Desk → piano D
- Contact Us → piano E
- Ergonomic Chairs → piano F
- Sit Stand Desk → piano G sharp
- Large Desk Converters → middle C

Use modern browser audio handling.

Requirements:

- Preload audio where appropriate.
- Reuse audio instances.
- Do not create a new Audio object on every hover.
- Do not fetch audio only after hover.
- Prevent overlapping playback.
- Handle browser autoplay restrictions.
- Audio must never block page rendering.
- Fail gracefully if playback is unavailable.

Desktop:

Hover may trigger the corresponding note once browser interaction policies permit playback.

Mobile:

Do not depend on hover.

Tap/click may trigger the corresponding note where appropriate.

---

# Hero

The old black background is being replaced.

Use:

`buro-latest-product-desktop.jpg`

for desktop.

Recommended source:

2560 × 1440 px.

Use:

`buro-latest-product-mobile.jpg`

for mobile.

Recommended source:

1080 × 1920 px.

Desktop ratio:

16:9

Mobile ratio:

9:16

The hero should occupy the majority of the viewport.

Do not unnecessarily crop important product details.

If a separate mobile image exists, use it rather than simply cropping the desktop image.

---

# Logo

Reuse the existing Buro logo.

Do not redesign the Buro logo.

The logo should remain prominent.

Ensure sufficient contrast against the hero image.

---

# Navigation

The original site uses WebSlideMenu.

Do NOT use WebSlideMenu in the new project.

Build the navigation using React, Tailwind CSS and modern browser APIs.

Desktop:

- Menu trigger
- Modern animated navigation panel
- Existing links
- Clear hierarchy
- Keyboard support

Mobile:

- Full-screen or large slide-in navigation
- Large touch targets
- Close button
- Escape key support
- Background interaction disabled while menu is open
- No hover dependency

Preserve the existing navigation structure and URLs.

---

# Existing Navigation

The current navigation contains:

Buroteck

Ergonomic Workstation

Workplace Interior Design

Control Desk

Ergo Chairs
- SIT-PRO
- i-Chair
- i-Chair Plus
- Ergo-Stool
- Educational
  - Trainer

Sit Stand Desk
- Single Column
- Two Columns
- Three Columns
- Four Columns
- Ergoboard Plus
- Three Column St
- Ergoboard-18
- Ergoboard-Large
- Ergoboard-Electric

Smart Furniture
- Security Rooms
- Control Desk
- Ergonomic Setup
- Broadcast & TV
- Gaming Console
- Trading Desk

Contact Us

Use the original source code as the authoritative source for the exact submenu URLs.

---

# Social Media

The old website uses raster social icons:

- Facebook GIF
- X/Twitter GIF
- Instagram GIF
- YouTube PNG

Do NOT reuse these raster icons.

Replace them with clean SVG brand icons.

Requirements:

- No pixelation.
- Consistent visual size.
- Consistent alignment.
- Consistent spacing.
- Minimum 44px clickable area on mobile.
- Keyboard accessible.
- Hover and focus states.
- Preserve SVG aspect ratios.
- Do not distort icons.

Existing social links:

Facebook:

https://www.facebook.com/Buro-Teck-352688888105591

X/Twitter:

https://x.com/buroteck_tweets

Instagram:

https://www.instagram.com/buroteck/

YouTube:

https://www.youtube.com/user/burodsin

Do not change these destinations.

---

# Tagline

Existing tagline:

Ergonomic Furniture - Control Command & Monitoring

Preserve the wording unless explicitly instructed to change it.

Modernise the typography, placement and responsiveness.

---

# Legacy Slideshow

The original page contains a small slideshow using:

- `buroteck.jpg`
- `buroteck-ergonomic.jpg`

This appears to be legacy content.

Inspect the current site and determine whether it is still necessary.

Do not automatically reproduce legacy content simply because it exists in the old HTML.

If it does not contribute to the new landing-page experience, remove it.

Document the decision in the final report.

---

# Responsive Design

The original site contains many viewport-specific CSS hacks.

Do NOT reproduce those hacks.

Build a clean responsive layout.

Test at:

- 320px
- 375px
- 390px
- 414px
- 768px
- 1024px
- 1280px
- 1440px
- 1920px

Desktop, tablet and mobile should be deliberately designed rather than simply scaled.

---

# Accessibility

Implement:

- Semantic HTML
- Keyboard navigation
- Visible focus states
- Accessible buttons
- ARIA labels where necessary
- Escape-to-close navigation
- Appropriate image alt text
- Reduced-motion support

Respect:

`prefers-reduced-motion`

When reduced motion is enabled, reduce or disable non-essential animations.

---

# Performance

This is a single-page landing page and should be extremely lightweight.

Avoid unnecessary dependencies.

Do NOT add:

- GSAP
- Three.js
- Lenis
- large UI frameworks
- unnecessary icon libraries

unless a specific requirement proves one is necessary.

Use native browser capabilities wherever practical.

Images and audio must not block initial rendering.

Hover assets and audio should be prepared in advance where appropriate.

---

# SEO

Implement:

- Page title
- Meta description
- Canonical URL
- Open Graph metadata
- Favicon
- Semantic headings
- Descriptive alt text

Canonical:

https://burodsin.com

---

# Static Export

This project must be deployable as a static website.

Configure Next.js for static export according to the current Next.js 16.3.1 documentation.

Do not assume the configuration from older Next.js versions.

Production build:

`npm run build`

Expected deployable output:

`out/`

The contents of `out/` should be directly uploadable to normal shared hosting.

No Node.js runtime should be required on the production hosting account.

---

# Project Structure

Keep the project simple.

Preferred structure:

app/
  layout.tsx
  page.tsx
  globals.css

components/
  Hero.tsx
  ProductGrid.tsx
  ProductTile.tsx
  Navigation.tsx
  SocialLinks.tsx
  Logo.tsx
  HoverAudio.tsx

data/
  navigation.ts

public/
  images/
    hero/
    tiles/
    logo/
  audio/

Do not create dozens of unnecessary components.

---

# Development Process

Before implementing:

1. Read `AGENTS.md`.
2. Read this `CLAUDE.md`.
3. Inspect the existing project files.
4. Inspect supplied image assets.
5. Inspect supplied audio assets.
6. Verify the navigation URLs against the supplied original source.
7. Then implement.

Do not guess when information is already available.

Do not make unrelated changes.

Do not modify `AGENTS.md`.

---

# Testing

After implementation:

1. Run the development server.
2. Test desktop.
3. Test tablet.
4. Test mobile.
5. Test all eight tiles.
6. Test hover visual states.
7. Test audio.
8. Test navigation.
9. Test all external links.
10. Test keyboard navigation.
11. Test Escape-to-close.
12. Test reduced motion.
13. Check browser console.
14. Check for missing assets.
15. Check for horizontal overflow.
16. Run the production build.

Fix errors rather than merely reporting them.

---

# Git

Do not commit automatically after every change.

Before a commit:

- Review changed files.
- Ensure no secrets are present.
- Ensure `node_modules` is ignored.
- Ensure `.next` is ignored.
- Ensure build output is handled correctly.
- Run tests/build where appropriate.

Use clear commit messages.

---

# Definition of Done

The project is complete when:

- Existing Buro landing-page identity is preserved.
- New full-screen product hero works.
- All eight interactive tiles work.
- Hover visual states work immediately.
- Eight individual piano notes work.
- Social icons are sharp and aligned.
- Navigation works on desktop.
- Navigation works on mobile.
- All existing URLs work.
- No jQuery remains.
- No Bootstrap remains.
- No WebSlideMenu remains.
- No Font Awesome dependency remains.
- No console errors exist.
- No broken images exist.
- No broken audio assets exist.
- Keyboard navigation works.
- Reduced-motion behaviour works.
- Production build succeeds.
- `out/` is generated successfully.
- The final output can be uploaded to normal shared hosting.

Keep this project intentionally small.

Do not turn it into the future Burotech ecommerce project.
