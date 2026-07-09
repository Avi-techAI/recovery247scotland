# Recovery 24x7 Scotland — Business Landing Page

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**Live site:** [recovery247scotland.com](https://recovery247scotland.com)

---

## Project Overview

A high-conversion landing page designed for **Recovery 24x7 Scotland**, a 24/7 car and van recovery business operating across Glasgow and a 20-mile radius. The primary business goal is to maximise inbound phone calls from drivers who have broken down or been involved in an accident.

This project was built from scratch as a real commercial product, covering the full process from competitor research and UX strategy through to design, development, and live deployment via a GitHub → Netlify CI/CD pipeline.

---

## Business Problem

The client needed a web presence that could:

- Convert stressed, mobile-first visitors into phone calls as fast as possible
- Stand out from generic competitor websites in the Glasgow recovery market
- Work as a complete website without a CMS or backend, keeping ongoing costs at zero
- Be editable by a non-technical business owner without developer support

---

## Solution & Technical Decisions

### Single-file architecture
The entire site — HTML, CSS, and JavaScript — is contained in one `.html` file with no external dependencies beyond Google Fonts. This means zero hosting costs, instant load times, and no build pipeline required for the client to maintain it.

### Mobile-first, conversion-focused layout
Research into Glasgow recovery competitors revealed that most existing sites buried the phone number and were not optimised for stressed mobile users. The layout was designed around a single goal: get the visitor to tap "Call" within three seconds of landing on the page.

Key conversion decisions:
- A sticky header with a tap-to-call button always visible as the user scrolls
- A fixed call/WhatsApp bar pinned to the bottom of the screen on mobile at all times
- The primary call button is the largest, highest-contrast element on every screen
- A WhatsApp button as a secondary contact option, common among UK mobile users

### Design system
A custom design system was built using CSS custom properties (variables), making the entire colour palette editable from a single location. The brand identity was derived from Chapter 8 hazard markings — the red and yellow chevron stripes on the back of every UK recovery vehicle — giving the site an immediately recognisable visual language native to the trade.

Two complete theme variants were produced:
- **Dark theme** (recommended for live use) — asphalt background, hi-vis yellow call buttons
- **Light theme** — warm off-white background, dark call buttons with yellow highlights

### Centralised contact configuration
All phone numbers, WhatsApp links, and email addresses are managed from a single JavaScript `CONFIG` object at the bottom of the file. Updating contact details site-wide requires editing one value in one place, with no risk of missing an instance.

### Accessibility and performance
- Semantic HTML throughout (`<header>`, `<section>`, `<nav>`, `<footer>`, `aria-label` attributes)
- Keyboard focus styles for all interactive elements
- `prefers-reduced-motion` media query to disable animations for users who need it
- No images (the recovery truck is an inline SVG), so the page loads instantly even on poor mobile data connections
- All interactive elements sized for large tap targets suitable for stressed users in difficult conditions

### Competitor research
Before design began, the Glasgow vehicle recovery market was researched across competitors including SRL Recovery, LM Recovery, YBR Glasgow Recovery, and Car Recovery Glasgow. Key findings:
- Most sites use generic templates with poor mobile optimisation
- Trust signals (insurance, accreditation, reviews) are inconsistently presented
- Non-fault accident recovery (a high-margin service paid by insurers) is under-promoted
- Almost no competitors publish transparent pricing, creating an opportunity to build trust

These findings directly informed the page structure and copy.

---

## Features

- Tap-to-call and WhatsApp buttons throughout
- Sticky header call button (desktop and mobile)
- Fixed mobile call bar pinned to bottom of screen
- Pulsing "Open Now" beacon indicator
- Six service cards with icons
- Non-fault accident recovery highlight panel
- 20 mile coverage area with town list and radius graphic
- Three-step "how it works" section
- Customer reviews section (placeholder, ready for real reviews)
- Transparent pricing reassurance block
- Expandable FAQ section which looks elegant
- Full footer with contact details and service area
- Fully commented source code for non-technical editing

---

## Deployment

The site is deployed via a GitHub → Netlify continuous deployment pipeline.

- Every commit to the `main` branch triggers an automatic redeploy on Netlify
- Deployment typically completes in under 30 seconds
- HTTPS is provided automatically by Netlify

**To deploy your own copy:**
1. Fork this repository
2. Connect the fork to a Netlify account via "Import from Git"
3. Leave all build settings blank (no build command needed)
4. Click Deploy

---

## Editing the Live Site

To update any content (phone number, services, coverage area, reviews):

1. Edit `index.html` directly on GitHub using the pencil icon
2. Commit the change to `main`
3. Netlify automatically redeploys within 30 seconds

Contact details (phone, WhatsApp, email) are managed from the `CONFIG` block at the bottom of `index.html`.

---

## Project Context

This landing page was built as part of a real business launch for a vehicle recovery startup in Glasgow, Scotland. It demonstrates end-to-end product thinking — from market research and UX decisions through to production deployment — within the constraint of zero ongoing hosting or maintenance cost for the client.

**Built by:** Avi (MSc Computer Science, Glasgow Caledonian University)
**Business:** Recovery 24x7 Scotland
**Year:** 2026

---

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and semantic markup |
| CSS3 | Styling, layout (Grid, Flexbox), animations, CSS variables |
| Vanilla JavaScript | CONFIG system, dynamic contact detail injection |
| Google Fonts | Anton (display) and Archivo (body) typefaces |
| SVG | Inline recovery truck illustration and all icons |
| Netlify | Hosting and continuous deployment |
| GitHub | Version control and portfolio evidence |
