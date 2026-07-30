# Functional Requirements Specification (FRS)

**Project:** Ruby Pizza N' Wings — Restaurant Website
**Author:** Vithusan Uthayakumaran (Business Analyst)
**Version:** 1.0
**Date:** July 30, 2026
**Related documents:** [BRD](01-business-requirements.md) · [User Stories & Backlog](03-user-stories-backlog.md)

---

## 1. Purpose

Defines what the website must do (functional requirements) and the qualities
it must have (non-functional requirements). Each requirement is numbered for
traceability to user stories and test checks. Status reflects the v1.0 build.

## 2. Functional Requirements

### 2.1 Global Navigation & Layout

| ID | Requirement | Priority | Status |
|---|---|---|---|
| FR-01 | Every page displays a sticky navbar with the restaurant logo, name, and slogan | Must | Done |
| FR-02 | Navbar links to Home, Menu, and About Us from every page | Must | Done |
| FR-03 | At viewport widths ≤ 960px, navigation collapses into a hamburger menu that toggles open/closed on tap | Must | Done |
| FR-04 | Every page displays a footer with address, hours, click-to-call phone link, and Uber Eats order link | Must | Done |

### 2.2 Home Page (`index.html`)

| ID | Requirement | Priority | Status |
|---|---|---|---|
| FR-05 | Hero section shows the storefront photo with restaurant name, slogan, and cuisine tags | Must | Done |
| FR-06 | Hero provides two calls-to-action: "See Our Menu" (internal) and "Order on Uber Eats" (external, new tab) | Must | Done |
| FR-07 | Info strip shows address, daily hours, and phone number; phone is a `tel:` link | Must | Done |
| FR-08 | "Fan Favourites" section shows at least three featured items with image, name, description, and price | Should | Done |
| FR-09 | "Deals & Combos" section shows family combo offers with branded promo-card imagery and price | Should | Done |

### 2.3 Menu Page (`Menu.html`)

| ID | Requirement | Priority | Status |
|---|---|---|---|
| FR-10 | Menu displays all categories from the restaurant's live menu (13 categories at time of build) | Must | Done |
| FR-11 | Each menu item shows name and price; description where available | Must | Done |
| FR-12 | Popularity badges ("#1 most liked", "#2 most liked") shown on items flagged on Uber Eats | Could | Done |
| FR-13 | A category jump-navigation bar links to each menu section via anchors | Should | Done |
| FR-14 | Wing sauce options and salad add-on pricing are listed as section notes | Should | Done |
| FR-15 | Page header repeats hours, phone, and Uber Eats ordering link | Should | Done |

### 2.4 About Us Page (`AboutUs.html`)

| ID | Requirement | Priority | Status |
|---|---|---|---|
| FR-16 | Page tells the restaurant's story, including its international menu positioning | Must | Done |
| FR-17 | Page shows the storefront photo | Should | Done |
| FR-18 | "Visit Us" section lists hours in a table and full contact details | Must | Done |
| FR-19 | Page includes an "Order on Uber Eats" call-to-action button | Should | Done |

### 2.5 Ordering Paths

| ID | Requirement | Priority | Status |
|---|---|---|---|
| FR-20 | All phone numbers are tappable `tel:+14168000823` links | Must | Done |
| FR-21 | All Uber Eats links open the store page in a new tab with `rel="noopener"` | Must | Done |

## 3. Non-Functional Requirements

| ID | Requirement | Priority | Status |
|---|---|---|---|
| NFR-01 | **Responsive:** usable from 375px (mobile) to 1300px+ (desktop); no horizontal scroll | Must | Done |
| NFR-02 | **No build step:** plain HTML/CSS/JS servable from any static host | Must | Done |
| NFR-03 | **Performance:** pages load over a static server with no JS framework payload; images are the only heavy assets | Should | Done (image optimization deferred to v1.1) |
| NFR-04 | **Accessibility:** all images carry descriptive `alt` text; semantic landmarks (`nav`, `main`, `footer`) used | Should | Done |
| NFR-05 | **Browser support:** current Chrome, Edge, Firefox, Safari (desktop & mobile) | Must | Done |
| NFR-06 | **Content accuracy:** menu parity with the Uber Eats listing, date-stamped in the README | Must | Done (as of July 30, 2026) |
| NFR-07 | **SEO basics:** unique, descriptive `<title>` per page | Should | Done (meta descriptions deferred to v1.1) |

## 4. Data Sources

| Data | Source | Notes |
|---|---|---|
| Menu categories, items, descriptions, prices | Uber Eats store page (retrieved July 30, 2026) | Authoritative, owner-published |
| Phone number, website name | Restaurant business card (`assets/images/01.jpg`) | |
| Wing sauces, add-on pricing | Branded promo cards (`assets/images/03.jpg`, `013.jpg`) | Detail not present on Uber Eats |
| Hours | Uber Eats store info | 11:00 a.m. – 9:00 p.m. daily |

## 5. Open Items

- OI-1: Owner to confirm whether in-store prices differ from Uber Eats prices
  (delivery platforms often carry a markup). If so, site should show in-store
  pricing.
- OI-2: Promo cards show some items/prices not on Uber Eats (e.g., sandwich
  specials, small/large fries split, poutine sizes). Owner to confirm which
  list is current before v1.1 content update.
- OI-3: Decide hosting target and custom domain (`rubypizzanwings.ca` appears
  on the business card — confirm ownership/renewal status).
