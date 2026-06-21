# Aura & Thread — Modern Fashion Brand Website

A premium, fully responsive fashion e‑commerce website showcasing a modern clothing brand with refined editorial aesthetics. This single‑page application includes a complete shopping experience with product browsing, filtering, sorting, cart management, wishlist, and a dark/light theme — all built with vanilla HTML, CSS, and JavaScript.

---

<img width="1900" height="902" alt="image" src="https://github.com/user-attachments/assets/eb01b9dc-a30a-4ad2-a4c1-3acdc8a10f73" />


## Overview

**Aura & Thread** is a conceptual fashion brand website that combines **editorial aesthetics** with **practical e‑commerce functionality**. The site presents a curated collection of clothing and accessories with a focus on:

- **Visual storytelling** — hero sliders, editorial lookbook, and polished typography.
- **Seamless shopping** — product browsing, filtering, sorting, and a persistent cart.
- **User engagement** — wishlist, quick view, and theme personalisation.
- **Modern craftsmanship** — ethical, slow‑fashion positioning with a sustainable ethos.

All content is static (data-driven via JavaScript), making it perfect for **brand showcases**, **portfolio projects**, or as a foundation for a full e‑commerce platform.

---

## Features

| Feature                     | Description                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| **Hero Slider**             | Auto‑rotating full‑width slides with dot navigation and smooth transitions.                      |
| **Typing & Motion Effects** | Subtle animations, floating shapes, and parallax scrolling for a polished feel.                  |
| **Product Carousel**        | Scrollable product cards with hover image‑swap, size selection, and "Add to Bag".                |
| **Category Grid**           | Visual category tiles linking to filtered product views.                                         |
| **Product Listing**         | Grid layout with **filtering** (by category) and **sorting** (price, newest, featured).          |
| **Quick View Modal**        | Detailed product view with image gallery, size selector, and add‑to‑cart from modal.             |
| **Shopping Cart**           | Slide‑out panel with item quantities, removal, total calculation, and persistent storage.        |
| **Wishlist**                | Heart‑icon toggle with persistent storage and counter badge.                                    |
| **Dark / Light Theme**      | Toggleable theme with smooth transitions; preference saved in `localStorage`.                   |
| **Lookbook / Editorial**    | Masonry grid with images and video content; images open in a lightbox.                          |
| **Newsletter Signup**       | Email subscription form with validation and toast feedback.                                     |
| **Store Locator**           | Embedded Google Maps iframe for store locations.                                                |
| **Toast Notifications**     | Non‑intrusive feedback for all user actions (cart, wishlist, newsletter).                       |
| **Responsive Design**       | Fully responsive across desktop, tablet, and mobile devices.                                    |
| **Accessibility**           | ARIA labels, semantic HTML, keyboard navigation, and focus management.                          |
| **PWA Ready**               | Inline manifest and service worker registration for basic offline support.                      |
| **Keyboard Shortcuts**      | `Ctrl+K` (or `Cmd+K`) to open search overlay.                                                   |
| **Persistent Data**         | Cart and wishlist saved in `localStorage`.                                                      |

---

## Technology Stack

- **HTML5** — Semantic markup with ARIA attributes for accessibility.
- **CSS3** — Custom properties (variables), Grid, Flexbox, animations, transitions, and dark/light theming.
- **Vanilla JavaScript (ES6+)** — DOM manipulation, event handling, state management, and localStorage persistence.
- **Google Fonts** — [Bodoni Moda](https://fonts.google.com/specimen/Bodoni+Moda) (serif headings) and [Inter](https://fonts.google.com/specimen/Inter) (sans‑serif body).
- **Unsplash** — High‑quality stock images used for products, categories, and editorial content.
- **Service Worker** — Basic offline caching via inline registration.
- **Manifest** — Inline JSON manifest for PWA support.

**No frameworks, no build tools, no dependencies** — everything is self‑contained in one HTML file.

---

## Installation & Usage

### 1. Download the file

Save `index.html` to your local machine.

### 2. Open in a browser

Double‑click the file or open it in your favourite browser (Chrome, Firefox, Edge, Safari).

### 3. Offline support

The page includes a minimal service worker that enables basic offline caching — once loaded, you can revisit without an internet connection.

### 4. Hosting

For live deployment, upload the file to any static hosting service (Netlify, Vercel, GitHub Pages, etc.).

---

## Project Structure

The entire application is contained in a **single HTML file** with well‑organised sections:

```
Clothes2.html
├── <head>
│   ├── Meta tags (viewport, charset, description)
│   ├── Google Fonts link
│   ├── Inline manifest (data URI)
│   └── <style> (all CSS — ~900 lines)
├── <body>
│   ├── Loading screen (animated thread logo)
│   ├── Header (fixed, with logo, nav, theme toggle, search, wishlist, cart, hamburger)
│   ├── Mega menu (Shop dropdown with categories)
│   ├── Search overlay (keyboard‑accessible)
│   ├── Hero section (auto‑sliding full‑width banner)
│   ├── New Arrivals carousel
│   ├── Category grid
│   ├── Product listing (with filters and sort)
│   ├── Lookbook (masonry with images and video)
│   ├── About / Sustainability section
│   ├── Newsletter & social grid
│   ├── Store locator (Google Maps iframe)
│   ├── Footer
│   ├── Back to top button
│   ├── Cart panel (slide‑out)
│   ├── Quick view modal
│   ├── Toast container
│   └── <script> (all JavaScript — ~600 lines)
└── (end)
```

---

## Key Components

### Loading Screen

- Animated SVG of a needle and thread, representing the brand's crafting ethos.
- Auto‑hides after the page loads (`window.load` event).
- Smooth opacity/visibility transition.

### Hero Slider

- Three full‑screen background images, auto‑rotating every 5 seconds.
- Dot navigation for manual control.
- Pause on hover? (not implemented, but easy to add).
- Call‑to‑action button with ripple effect.

### Product Carousel

- Horizontal scrollable track of product cards.
- Each card shows:
  - Front and back images (swap on hover).
  - Product name, price, and size circles.
  - "Add to Bag" button (slides up on hover).
- Navigation arrows for quick scrolling.
- Keyboard‑accessible (`ArrowLeft` / `ArrowRight`).

### Category Grid

- Five visual tiles: Dresses, Tops, Bottoms, Outerwear, Accessories.
- Clicking a tile filters the product grid and scrolls to it.
- Hover zoom and overlay effects.

### Product Listing with Filter & Sort

- **Filters** — category tabs (`All`, `Dresses`, `Tops`, `Bottoms`, `Outerwear`, `Accessories`).
- **Sort** — dropdown: `Featured`, `Price: Low → High`, `Price: High → Low`,
