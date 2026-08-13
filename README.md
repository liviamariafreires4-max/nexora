# Nexora — Premium SaaS & Agency Bootstrap 5 Theme

A fully responsive, multi-page business/marketing theme built with **Bootstrap 5.3**, semantic HTML5 and vanilla JavaScript. Designed for SaaS startups, digital agencies, IT companies and consulting firms.

## 📁 Folder Structure

```
nexora-theme/
├── index.html              Home (landing page)
├── about.html              About Us
├── services.html           Services overview
├── service-details.html    Single service detail
├── portfolio.html           Portfolio / case studies grid (with filter)
├── portfolio-single.html    Single case study
├── blog.html                Blog listing
├── blog-details.html        Single blog post
├── pricing.html             Pricing plans + comparison table
├── contact.html             Contact form + map
├── css/
│   └── custom.css           Design system (variables, components, overrides)
├── js/
│   └── main.js              UI interactions (navbar, scroll reveal, validation, etc.)
└── README.md
```

## 🎨 Design System

All design tokens live as CSS variables at the top of `css/custom.css` under `:root`. Edit these to retheme the entire site in minutes.

| Token | Value | Use |
|---|---|---|
| `--n-primary` | `#155EEF` | Primary buttons, links, accents |
| `--n-secondary` | `#6941C6` | Secondary accents, gradients |
| `--n-navy` | `#0B1437` | Headings, dark sections |
| `--n-success` | `#12B76A` | Checkmarks, success states |
| `--n-bg` | `#F7F9FC` | Section backgrounds |
| `--n-border` | `#E4E7EC` | Borders, dividers |

### Typography
- **Display / Headings:** [Sora](https://fonts.google.com/specimen/Sora) (700/800 weight)
- **Body:** [Inter](https://fonts.google.com/specimen/Inter)

Both loaded via Google Fonts CDN in the `<head>` of every page.

### Spacing rhythm
8px-based scale via `--n-space-*` variables (`xs` 8px → `2xl` 96px). Section padding uses `.section` (96px) and `.section-sm` (64px), both collapsing on mobile.

## 🧱 Reusable Components

All components are documented with comments in `custom.css`:

- **Navbar** (`.navbar-nexora`) — sticky, blurs on scroll, animated hamburger
- **Buttons** (`.btn-primary`, `.btn-outline-primary`, `.btn-light-custom`, `.btn-outline-white`) — sizes via `.btn-lg-custom` / `.btn-sm-custom`
- **Cards** (`.card-premium`) — soft shadow, hover lift, used for services/blog/team
- **Pricing cards** (`.pricing-card`, `.pricing-card.featured`)
- **Testimonial cards** (`.testimonial-card`)
- **Portfolio cards** (`.portfolio-card` with hover overlay)
- **Process steps** (`.process-step` / `.process-number`) — numbered sequence
- **Page header** (`.page-header`) — dark gradient header for sub-pages
- **CTA section** (`.cta-section`) — dark gradient call-to-action block
- **Widgets** (`.widget`) — sidebar blocks for blog/service pages
- **Footer** (`.footer-nexora`)

## ⚙️ JavaScript Features (`js/main.js`)

- Sticky navbar with scroll-triggered background/blur
- Mobile menu toggle animation (hamburger → X)
- Smooth scroll for in-page anchors
- Lightweight scroll-reveal via IntersectionObserver (`.reveal` class)
- Back-to-top button
- Bootstrap form validation UI (`.needs-validation`)
- Active nav-link highlighting based on current page
- Portfolio category filter (inline script on `portfolio.html`)
- Monthly/Yearly pricing toggle (inline script on `pricing.html`)

## 🚀 Getting Started

1. Open `index.html` in a browser — no build step required.
2. To customize colors/fonts, edit the `:root` variables in `css/custom.css`.
3. Replace placeholder images (Unsplash/Pravatar URLs) with your own assets.
4. Update text content directly in each HTML file — all copy is in plain HTML, no templating engine.
5. To add a new page, copy any existing page and keep the navbar/footer markup identical for consistency.

## 📋 Notes for Buyers

- Built with Bootstrap 5.3 (CDN) + Bootstrap Icons (CDN) — no npm install needed.
- All images are placeholders from Unsplash/Pravatar for demo purposes — replace before going live.
- Contact form and newsletter forms are front-end only (validation UI only); connect to your backend or a service like Formspree/Netlify Forms for submissions.
- Fully responsive: tested down to 320px width, no horizontal scroll.
- Respects `prefers-reduced-motion` for accessibility.

## 🔧 Customization Tips

- **Change accent color:** update `--n-primary` and `--n-gradient-primary` in `custom.css`.
- **Change fonts:** swap the Google Fonts `<link>` and update `--n-font-display` / `--n-font-body`.
- **Add a new service/blog/portfolio item:** duplicate an existing `.card-premium` block and update content/images.
- **Disable animations:** remove the `reveal` class from elements, or it auto-disables under reduced-motion preference.

---
© 2026 Nexora Theme. For support, refer to the documentation comments within `custom.css` and `main.js`.
