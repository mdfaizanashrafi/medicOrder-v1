# MedicOrder Landing Page

> **The Operating System for Medicine Distribution**  
> A modern, premium B2B SaaS landing page built for the pharmaceutical supply chain industry.

---

## Overview

This repository contains a complete, production-ready landing page for **MedicOrder** — a B2B pharmaceutical wholesale logistics and procurement platform. The page is designed to communicate trust, security, and enterprise-grade infrastructure to pharmacies, stockists, distributors, and medical vendors.

**Design Philosophy:** *"Stripe meets healthcare supply-chain infrastructure."*

---

## ✨ Features

- **Single-file architecture** — Zero dependencies, zero build steps. Just open the HTML file.
- **Responsive design** — Fully adaptive from mobile to desktop with a dedicated mobile navigation menu.
- **Scroll-triggered animations** — IntersectionObserver-based fade-in effects for a polished, modern feel.
- **Interactive hero section** — Animated logistics network visualization with floating dashboard cards, live order routing preview, and glowing network nodes.
- **Complete section coverage:**
  - Fixed glassmorphism navigation
  - Animated hero with gradient background
  - Problem statement (dark themed)
  - Core platform features (6 cards)
  - Dual value proposition (Pharmacies vs. Stockists)
  - 4-step "How It Works" workflow
  - Security & compliance highlight
  - Waitlist signup with gradient CTA
  - Full footer with site map
- **Form handling** — Waitlist form with visual success feedback.
- **Smooth scrolling** — Anchor links scroll smoothly to target sections.
- **Custom scrollbar** — Brand-styled scrollbar for cohesion.

---

## 🚀 Quick Start

No installation required. No build tools. No dependencies.

### Option 1: Direct Open
Simply open `index.html` in any modern web browser.

```bash
open index.html
```

### Option 2: Local Server (recommended for testing)
```bash
# Python 3
python -m http.server 8000

# Node.js (if you have npx)
npx serve .

# PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000`.

---

## 📁 File Structure

```
medicorder-landing/
├── index.html          # Complete landing page (HTML + CSS + JS)
└── README.md           # This file
```

> **Note:** The entire application is self-contained in a single HTML file. All styles are embedded in `<style>` and all scripts are embedded in `<script>`. No external CSS or JS files are required. Google Fonts are loaded via CDN.

---

## 🎨 Brand Palette

| Color       | Hex Code  | Purpose                                     |
| ----------- | --------- | ------------------------------------------- |
| Deep Forest | `#182825` | Authority, trust, headings, dark sections   |
| Royal Blue  | `#016FB9` | Primary actions, CTAs, links                |
| Bright Cyan | `#22AED1` | Innovation, highlights, icons               |
| Muted Steel | `#6D8EA0` | Secondary text, borders, supporting content |
| Warm Stone  | `#AFA98D` | Decorative accents and subtle backgrounds   |

### CSS Variables

```css
:root {
  --primary:   #182825;
  --secondary: #016FB9;
  --accent:    #22AED1;
  --muted:     #6D8EA0;
  --neutral:   #AFA98D;
  --bg:        #F8FAFC;
  --surface:   #FFFFFF;
  --text:      #182825;
  --text-light:#6D8EA0;
  --border:    rgba(109,142,160,0.18);
  --shadow:    0 12px 30px rgba(24,40,37,0.08);
}
```

---

## 🔤 Typography

| Role     | Font  | Weights              |
| -------- | ----- | -------------------- |
| Headings | Sora  | 400, 500, 600, 700   |
| Body     | Inter | 400, 500, 600, 700   |

Fonts are loaded via Google Fonts CDN:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Sora:wght@400;500;600;700&display=swap" rel="stylesheet">
```

---

## 📱 Responsive Breakpoints

| Breakpoint | Behavior                                              |
| ---------- | ----------------------------------------------------- |
| > 1024px   | Full desktop layout — 2-column grids, hero visual     |
| ≤ 1024px   | Tablet — hero stacks vertically, value props stack    |
| ≤ 768px    | Mobile — hamburger menu, single-column, hidden visuals|

---

## 🧩 Sections

| Section            | Description                                           |
| ------------------ | ----------------------------------------------------- |
| **Navigation**     | Fixed glassmorphism navbar with logo, links, CTA      |
| **Hero**           | Gradient background, animated network, dashboard card|
| **Problem**        | Dark section highlighting 4 core industry pain points  |
| **Features**       | 6 core platform capabilities in hover-animated cards   |
| **Value Prop**     | Side-by-side benefits for Pharmacies & Stockists     |
| **How It Works**   | 4-step workflow with numbered badges                   |
| **Security**       | Enterprise compliance & trust signals                 |
| **Waitlist**       | Email capture with gradient CTA section               |
| **Footer**         | 4-column layout: brand, platform, company, legal     |

---

## ⚙️ Customization Guide

### Changing Colors
All colors are defined as CSS variables in the `:root` selector at the top of the `<style>` block. Update the hex codes there to retheme the entire page.

### Adding a New Feature Card
Copy an existing `.feature-card` block inside the `.features-grid` container:
```html
<div class="feature-card fade-in">
  <div class="feature-icon">🎯</div>
  <h3>Your Feature Name</h3>
  <p>Your feature description here.</p>
</div>
```

### Updating Navigation Links
Edit the `.nav-links` `<ul>` and the `.mobile-menu` `<div>` simultaneously to keep desktop and mobile menus in sync.

### Changing Hero Content
Edit the `.hero-content` div. The `.hero-visual` contains the animated dashboard preview — adjust the `.dashboard-card` rows to simulate different order data.

### Waitlist Endpoint
The waitlist form currently shows a visual success state via JavaScript. To connect to a real backend:

1. Locate the `handleWaitlist` function in the `<script>` block.
2. Replace the `setTimeout` logic with a `fetch()` call to your API endpoint.

```javascript
// Example integration
fetch('/api/waitlist', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ email: emailValue })
})
```

---

## 🌐 Browser Compatibility

| Browser | Version | Status |
|---------|---------|--------|
| Chrome  | 90+     | ✅ Full support |
| Firefox | 88+     | ✅ Full support |
| Safari  | 14+     | ✅ Full support |
| Edge    | 90+     | ✅ Full support |
| Mobile Safari | iOS 14+ | ✅ Full support |
| Chrome Android | 90+ | ✅ Full support |

> **Note:** Internet Explorer is not supported.

---

## 📦 Dependencies

| Dependency | Source | Purpose |
| ---------- | ------ | ------- |
| Google Fonts (Sora) | CDN | Heading typography |
| Google Fonts (Inter) | CDN | Body typography |

**Total external dependencies: 1** (Google Fonts stylesheet)  
**Build tools required: 0**

---

## 🏗️ Future Enhancements

- [ ] Connect waitlist form to backend API / email service (e.g., Mailchimp, ConvertKit)
- [ ] Add dark mode toggle
- [ ] Implement multi-language support (i18n)
- [ ] Add testimonial carousel from beta users
- [ ] Integrate Calendly or similar for demo booking
- [ ] Add FAQ accordion section
- [ ] Implement cookie consent banner
- [ ] Add Open Graph / Twitter Card meta tags for social sharing
- [ ] Create separate pages for Terms, Privacy, and Security documentation
- [ ] Add structured data (JSON-LD) for SEO

---

## 📄 License

Proprietary — MedicOrder Platform. All rights reserved.

---

## 🙋 Support

For questions about this landing page or the MedicOrder platform, contact the development team or open an issue in the project repository.

---

<p align="center">
  <strong>MedicOrder</strong> — The digital backbone of pharmaceutical wholesale procurement.
</p>
