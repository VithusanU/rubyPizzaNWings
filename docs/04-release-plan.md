# Release Plan & Roadmap

**Project:** Ruby Pizza N' Wings — Restaurant Website
**Author:** Vithusan Uthayakumaran (Product Owner)
**Version:** 1.0
**Date:** July 30, 2026
**Related documents:** [BRD](01-business-requirements.md) · [FRS](02-functional-requirements.md) · [User Stories & Backlog](03-user-stories-backlog.md)

---

## 1. Release Strategy

Ship small and early. v1.0 proves the owned web presence with zero hosting
cost and no backend. Each later release is justified by an owner decision or
by data (analytics) from the previous one — no speculative build-out.

## 2. v1.0 — "Open for Business" (Shipped July 30, 2026)

**Goal:** A complete, accurate, branded site a customer can use to decide,
call, or order delivery.

**Scope shipped:**
- Home page: hero, info strip, Fan Favourites, Deals & Combos (US-01, US-02, US-07, US-08, US-10)
- Menu page: 13 categories, all items priced, jump navigation, most-liked badges (US-03–US-06)
- About Us page: story, storefront, hours, contact (US-09)
- Responsive layout with mobile hamburger navigation
- Menu data populated from the live Uber Eats listing (date-stamped)

**Known limitations (accepted for v1.0):**
- Not yet publicly hosted; no custom domain connected
- Promo-card images stand in for real food photography
- Prices mirror Uber Eats and may differ from in-store (OI-1)
- Large source images not yet compressed for web

## 3. v1.1 — "Findable" (Next)

**Goal:** Customers can actually reach the site and the owner can measure it.

| Item | Backlog ref | Exit criteria |
|---|---|---|
| Public hosting (GitHub Pages or similar) | US-11 | Site reachable on public URL over HTTPS |
| Custom domain decision (`rubypizzanwings.ca`) | US-11 / OI-3 | Domain connected or consciously deferred by owner |
| SEO basics: meta descriptions, Open Graph, sitemap | US-12 | Pages indexed; social shares show preview card |
| Analytics with click-to-call tracking | US-13 | Owner receives monthly visits + call-tap numbers |
| Image compression | NFR-03 | Largest page ≤ ~1.5 MB transferred |
| Owner content review (prices, hours, open items OI-1/OI-2) | US-16 | Owner sign-off recorded in BRD approval table |

## 4. v1.2 — "Appetizing"

**Goal:** Increase conversion of visitors into orders.

| Item | Backlog ref |
|---|---|
| Real food photography replacing promo-card stand-ins | US-15 |
| Google Maps embed with directions | US-14 |
| Weekly specials section fed by promo-card pipeline | US-19 |
| Menu content moved to a single JSON data file | US-17 |

## 5. v2.0 — "Direct Orders" (Data-dependent)

**Goal:** Reduce commission dependency — only if v1.1 analytics show real
demand (e.g., sustained ≥ 500 visits/month or strong call-tap rates).

| Item | Backlog ref |
|---|---|
| On-site ordering & payment (evaluate: hosted ordering widgets vs. custom) | US-18 |
| French-language key info | US-20 |

## 6. Definition of Done (applies to every release)

- Renders correctly on mobile (375px) and desktop (1280px) with no horizontal
  scroll
- All internal links, anchors, and external links verified working
- All images have descriptive alt text
- No browser console errors
- Content matches the current owner-approved source (menu, hours, phone)
- Changes committed to `main` and pushed to GitHub with a descriptive message
- README and affected docs updated in the same release

## 7. Cadence & Process

Single-maintainer project: work is batched into the releases above rather than
fixed sprints. Each release ends with an owner review; feedback becomes new
backlog items. The backlog is re-prioritized (MoSCoW) before each release
starts.
