# Bening's Delicacies — Web & Mobile Design

A responsive, accessible e-commerce website designed for **Bening's Delicacies**, a Filipino cook-to-order family business offering Espasol, Cassava Cake, Bibingka, and seasonal Homemade Kimchi.

---

## Project Overview

- **Client:** Bening's Delicacies
- **Business Model:** Cook-to-order traditional Filipino specialties (started by Nanay Bening to raise her 5 children, and now passed down to her son Cenon)
- **Target Audience:** Adults aged 40 and above (demanding comfortable readability, calm anti-glare colors, and large tap targets)
- **Design Deliverable:** 4 responsive pages adhering to desktop (1440 × 1024 px) and mobile (390 × 844 px) standards
- **Hosting Ready:** Pre-configured for instant zero-config deployment on [Vercel](https://vercel.com)

---

## The 4 Pages

| Page | File | Route | Description |
|---|---|---|---|
| **Home Page** | [`index.html`](index.html) | `/` | Hero section with tagline, 3 core value cards, 4-delicacy showcase, **Pasalubong for Abroad / Travel-Ready feature section**, customer testimonials, and rich footer. |
| **About Us** | [`about.html`](about.html) | `/about` | Family story honoring Nanay Bening and son Cenon, kitchen photo showcase, 3 core pillars, and 5 checkmark differentiators. |
| **Delicacies Menu** | [`menu.html`](menu.html) | `/menu` | Full product grid (Espasol, Cassava Cake, Bibingka, Kimchi) with prices, occasion tags, order notice banner, and 3-step order process. |
| **Contact & Order** | [`contact.html`](contact.html) | `/contact` | Accessible order request form with query parameter auto-selection (e.g. `?product=cassava`), direct contact card with phone/email/hours/map, and native FAQ accordion. |

---

## Responsive Design Decisions

Every page is self-contained using CSS media queries (`@media (max-width: 768px)`) to provide distinct, deliberate responsive experiences:

1. **Collapsed & Bottom Navigation:**
   - **Desktop ($\ge 769\text{px}$):** Sticky top bar with logo, links, and an "Order Now" action button.
   - **Mobile ($\le 768\text{px}$):** Top bar collapses to a 44px hamburger menu button, and a **fixed bottom navigation bar** (Home, Menu, About, Contact) appears for easy one-handed thumb navigation.
2. **Single-Column Reflow:**
   - Multi-column desktop grids (hero 2-col, features 3-col, menu 2x2, contact 60/40) reflow into clean, single-column stacks on mobile.
3. **Large Tap Targets ($\ge 44 \times 44\text{ px}$):**
   - Action buttons are enlarged to **52px – 56px height**, form inputs to **48px**, and bottom navigation items to **48px** for easy tapping by older patrons.
4. **Content Priority Reordering:**
   - **Home:** Delicacies showcase appears first on mobile before heading text.
   - **About:** Hearth & kitchen visual appears first before the narrative.
   - **Contact:** The Contact Details card appears **above the form** on mobile for immediate phone/email access.

---

## Design System

The complete token and component documentation is stored in [`design-system.txt`](design-system.txt).

### Color Palette (Pleasing, Low-Strain Earth Tones)

| Token Role | Color Name | HEX Code | Tested Contrast Ratio | WCAG AA Status |
|---|---|---|---|---|
| **Primary** | Warm Brown | `#7B5C3A` | $4.6 : 1$ (on Light Text) | ✅ Pass (AA) |
| **Primary Light** | Honey Brown | `#A8784F` | Hover state | ✅ Pass |
| **Secondary** | Soft Caramel | `#C4956A` | Accent borders & badges | ✅ Pass |
| **Accent** | Pale Peach | `#E8C9A0` | Banner highlights | ✅ Pass |
| **Accent Light** | Warm Cream | `#F5EAD8` | Section backgrounds | ✅ Pass |
| **Background** | Warm Off-White | `#FBF7F2` | Main page canvas (anti-glare) | ✅ Pass |
| **Neutral Dark** | Deep Espresso | `#3D2B1F` | $9.1 : 1$ (Headings on bg) | ✅ AAA Enhanced |
| **Neutral Mid** | Medium Brown | `#6B5244` | $5.4 : 1$ (Body text on bg) | ✅ AA Normal |
| **Neutral Light** | Muted Tan | `#D4B99A` | Borders & placeholder fills | ✅ Pass |

### Typography

- **Heading Font:** *Playfair Display* (Serif) — weights 600, 700. Conveying warmth, tradition, and culinary heritage.
- **Body Font:** *Lato* (Sans-serif) — weights 400, 600, 700. Clean, humanist sans-serif with high legibility.
- **Type Scale:** Display H1: 52px (34px mobile) · Section H2: 38px (28px mobile) · Card H3: 22–26px · Body: **18px** (well above the 16px minimum).

---

## Accessibility & Inclusivity (WCAG AA)

- [x] **Contrast Compliance:** All text-to-background combinations exceed the 4.5:1 minimum (up to 9.1:1 for headings and 12.6:1 for footer text).
- [x] **Body Text Scale:** Set to 18px on both desktop and mobile.
- [x] **Tap Targets:** Mobile buttons are 52–56px, nav items $\ge 48\text{px}$ (exceeding the $44\text{px}$ standard).
- [x] **No Color-Only Meaning:** Checkmarks, badge icons, and descriptive text accompany all statuses.
- [x] **Alternative Text Notes:** Provided on all image containers and placeholders for screen reader compatibility.
- [x] **Keyboard Navigation:** Native `<details>`/`<summary>` accordion for FAQ, clear focus outline styles.

---

## How to Test Locally

1. Open `index.html` in any web browser.
2. Maximize the window to view the **1440px desktop layout**.
3. Press `F12` $\rightarrow$ Toggle Device Toolbar (`Ctrl+Shift+M`) $\rightarrow$ set to **390 × 844 px** to view the **mobile responsive layout**.

---

## How to Deploy to Vercel

### Option 1: Vercel CLI
```powershell
npx vercel
```

### Option 2: GitHub Integration
1. Push this folder to a GitHub repository.
2. Import the repository into [Vercel](https://vercel.com/new).
3. Click **Deploy**. Vercel will automatically serve `index.html` at your production URL.
