# User Stories & Product Backlog

**Project:** Ruby Pizza N' Wings — Restaurant Website
**Author:** Vithusan Uthayakumaran (Product Owner)
**Version:** 1.0
**Date:** July 30, 2026
**Related documents:** [BRD](01-business-requirements.md) · [FRS](02-functional-requirements.md) · [Release Plan](04-release-plan.md)

---

## 1. Personas

**Priya, 38 — the family planner.** Lives in the Upper Beaches with two kids.
Orders delivery on busy weeknights and looks for family-sized deals on her
phone. Wants to see combo contents and total price before deciding.

**Marcus, 27 — the commuter.** Passes the Main St storefront on his walk from
Main Street station. Wants to check hours and call ahead so a pickup order is
ready when he arrives.

**Sandra, 55 — the explorer.** Bored of standard pizza. Curious about the
butter chicken pizza she heard about from a neighbour. Wants photos, a menu
she can browse, and a reason to trust the place before trying it.

## 2. Epics

| Epic | Goal | Objective link |
|---|---|---|
| E1 — Discover the restaurant | Visitors instantly understand what/where/when | BO-1 |
| E2 — Browse the menu | Full menu with prices, easy to scan on mobile | BO-3 |
| E3 — Place an order | Clear paths to phone and Uber Eats ordering | BO-2, BO-5 |
| E4 — Trust the brand | Story, photos, and brand assets build confidence | BO-4 |
| E5 — Operate & grow (future) | Hosting, SEO, analytics, ordering integrations | BO-1, BO-2 |

## 3. User Stories — v1.0 (Delivered)

### Epic E1 — Discover the restaurant

**US-01** (Must) — *As a visitor, I want the home page to show what the
restaurant is and where it is, so I can decide if it's for me.*
- **Given** I land on the home page, **when** it loads, **then** I see the
  restaurant name, slogan, cuisine tags, and storefront photo without scrolling.
- **Given** any page, **when** I scroll to the info strip or footer, **then**
  I see the address and daily hours. ✅ Done (FR-05, FR-07)

**US-02** (Must) — *As a mobile visitor, I want navigation that works on my
phone, so I can move between pages with one thumb.*
- **Given** a viewport ≤ 960px, **when** I tap the hamburger icon, **then** the
  menu opens; tapping again (or a link) closes it. ✅ Done (FR-03)

### Epic E2 — Browse the menu

**US-03** (Must) — *As Priya, I want to see every menu item with its price, so
I can budget the order before calling.*
- **Given** the Menu page, **when** it loads, **then** all categories and every
  item show a price. ✅ Done (FR-10, FR-11)

**US-04** (Should) — *As Priya, I want deals and combos grouped and detailed,
so I can compare family options quickly.*
- **Given** the Menu page, **when** I open "Family Combos & Specials", **then**
  each combo lists its full contents and total price. ✅ Done (FR-09, FR-10)

**US-05** (Should) — *As a menu browser, I want to jump straight to a
category, so I don't scroll through 40+ items.*
- **Given** the Menu page, **when** I tap a category chip, **then** the page
  scrolls to that section with the heading visible below the sticky navbar.
  ✅ Done (FR-13)

**US-06** (Could) — *As Sandra, I want to see which items other customers
like most, so I can pick a safe first order.*
- **Given** the Menu page, **then** items flagged most-liked on Uber Eats show
  a badge. ✅ Done (FR-12)

### Epic E3 — Place an order

**US-07** (Must) — *As Marcus, I want to call the restaurant in one tap, so my
pickup order is ready when I arrive.*
- **Given** any page on a phone, **when** I tap the phone number, **then** my
  dialer opens with 416-800-0823 prefilled. ✅ Done (FR-20)

**US-08** (Must) — *As a delivery customer, I want a direct link to the Uber
Eats store, so I can order delivery immediately.*
- **Given** any page, **when** I tap "Order on Uber Eats", **then** the store
  page opens in a new tab. ✅ Done (FR-06, FR-21)

### Epic E4 — Trust the brand

**US-09** (Should) — *As Sandra, I want to read the restaurant's story and see
the storefront, so I feel confident trying it.*
- **Given** the About Us page, **then** I see the story, the storefront photo,
  hours, and contact details. ✅ Done (FR-16–FR-18)

**US-10** (Should) — *As the owner, I want the site to use my existing brand
artwork, so the site matches my print and social presence.*
- **Given** the home page, **then** the logo, promo cards, and brand colours
  (chalkboard dark, ruby red, mustard yellow) appear throughout. ✅ Done (FR-08, FR-09)

## 4. Product Backlog — Future (v1.1+)

Ordered by priority. See the [Release Plan](04-release-plan.md) for grouping.

| ID | Story | Priority | Notes |
|---|---|---|---|
| US-11 | As the owner, I want the site hosted on a public URL (and the `rubypizzanwings.ca` domain connected), so customers can actually find it | Must | GitHub Pages is free; domain status needs confirming (OI-3) |
| US-12 | As a searcher, I want the site to rank for "pizza near Main Street Toronto", so I discover it on Google | Must | Meta descriptions, Open Graph tags, `sitemap.xml`, Google Business Profile link |
| US-13 | As the owner, I want to know how many people visit and tap "call", so I can measure the site's value | Should | Privacy-friendly analytics (e.g., Plausible/GoatCounter); measures BO-2 |
| US-14 | As Priya, I want a Google Maps embed with directions, so I can find parking and the storefront | Should | |
| US-15 | As Sandra, I want real photos of the food (not promo cards), so I know what arrives | Should | Owner to supply/approve photos; several exist in the newer OneDrive asset set |
| US-16 | As a visitor, I want confirmation that in-store prices match the listed prices, so I'm not surprised at pickup | Should | Depends on OI-1 owner confirmation |
| US-17 | As the owner, I want menu content in one data file (e.g., JSON) rendering the page, so price updates touch one place | Could | Keeps no-build constraint if done client-side |
| US-18 | As a customer, I want to order and pay on the site itself, so the restaurant avoids commissions | Could | Larger effort: needs payments, order handling; revisit after traffic data |
| US-19 | As a returning customer, I want to see weekly specials, so I check back regularly | Could | Reuses promo-card pipeline |
| US-20 | As a francophone customer, I want key info in French, so I can read hours and address comfortably | Won't (this year) | Revisit with owner |

## 5. Definition of Ready (for future stories)

A story enters a build cycle when it has: a persona and goal, testable
acceptance criteria, content/assets confirmed by the owner, and a priority
agreed against the rest of the backlog.
