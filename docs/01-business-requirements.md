# Business Requirements Document (BRD)

**Project:** Ruby Pizza N' Wings — Restaurant Website
**Author:** Vithusan Uthayakumaran (Business Analyst)
**Version:** 1.0
**Date:** July 30, 2026
**Status:** Draft — pending owner review

---

## 1. Executive Summary

Ruby Pizza N' Wings is a family-run pizza and wings restaurant at 162 Main St,
Toronto (Upper Beaches). Its only digital presence is a third-party Uber Eats
listing. This project delivers a restaurant-owned website that showcases the
brand, publishes the full menu, and gives customers direct ways to order —
by phone or through the existing Uber Eats channel.

## 2. Background & Problem Statement

- The restaurant has **no website of its own**. Customers searching for it find
  only the Uber Eats listing and third-party review sites.
- Uber Eats charges **commission on every order**; the restaurant has no
  channel that promotes free pickup or direct phone orders.
- The Uber Eats listing **cannot express the brand** — no storefront photo, no
  story, no promotion of the restaurant's distinctive Asian & international
  menu (butter chicken pizza, shawarma, souvlaki) that differentiates it from
  other pizza shops on the strip.
- The restaurant already invested in **branded promo-card artwork** (specials,
  combos, business cards) that is only used in print and social posts.

**Problem statement:** Potential customers cannot discover the restaurant's
full offering or contact it directly online, pushing all digital demand
through a commissioned third-party channel.

## 3. Business Objectives

| # | Objective | Measure of success |
|---|---|---|
| BO-1 | Establish an owned digital presence | Site live and indexed by search engines |
| BO-2 | Increase direct (phone/pickup) orders | Phone number prominent on every page; click-to-call enabled |
| BO-3 | Showcase the full menu with prices | 100% of Uber Eats menu items published with prices |
| BO-4 | Reuse existing brand assets | Logo, storefront photo, and promo cards used across the site |
| BO-5 | Preserve the delivery channel | Uber Eats order link present on every page |

## 4. Stakeholders

| Stakeholder | Role | Interest / Influence |
|---|---|---|
| Restaurant owner | Sponsor | Approves scope and content; wants more direct orders |
| Restaurant staff | Operations | Answer phone orders driven by the site |
| Customers (local residents, delivery users) | End users | Find menu, prices, hours, and how to order |
| Developer / BA / PO (Vithusan) | Delivery team | Builds and maintains the site |
| Uber Eats | Third-party platform | Source of menu data; delivery fulfilment channel |

## 5. Scope

### In scope (v1.0)

- Static, responsive website with three pages: Home, Menu, About Us
- Full menu content (categories, items, descriptions, prices) sourced from the
  live Uber Eats listing
- Business information: address, daily hours, phone (click-to-call)
- Brand assets: logo, storefront photo, promo-card imagery
- Outbound ordering links to Uber Eats
- Mobile-first responsive layout with hamburger navigation

### Out of scope (v1.0)

- Online ordering / payment processing on the site itself
- Reservations or table booking
- Content management system (content is edited in HTML)
- Customer accounts, loyalty programs
- Multilingual content
- Custom domain purchase and hosting setup (tracked for a future release)

## 6. Assumptions

- The Uber Eats listing is the authoritative, owner-approved menu and price list.
- Prices and hours change infrequently; manual HTML updates are acceptable at
  this stage.
- The restaurant retains rights to all supplied imagery and branding.
- Hosting will be low/no-cost static hosting (e.g., GitHub Pages) until traffic
  justifies more.

## 7. Constraints

- No budget for paid tooling, stock photography, or custom backend development.
- Single-person delivery team (development, BA, and PO roles combined).
- Site must work without any build system so the owner can host it anywhere.

## 8. Risks

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Menu prices drift out of sync with Uber Eats | High | Medium | Date-stamp the data source; schedule periodic content reviews |
| Restaurant temporarily closed / listing "currently unavailable" | Medium | Medium | Site emphasizes phone contact; hours reviewed with owner |
| No custom domain yet — discoverability limited | Medium | Medium | Roadmap item for domain + SEO in v1.1 |
| Single maintainer availability | Medium | Low | Simple static stack keeps handover cost low |

## 9. Success Metrics (post-launch)

- Site reachable and mobile-friendly (Lighthouse mobile score ≥ 85)
- All 13 menu categories and every priced item published (parity check vs.
  Uber Eats listing)
- Phone number tappable on mobile from every page
- Owner sign-off on brand presentation
- (After hosting + analytics in v1.1) ≥ 100 unique visitors/month and
  measurable click-to-call events

## 10. Approval

| Name | Role | Decision | Date |
|---|---|---|---|
| Restaurant owner | Sponsor | Pending review | — |
| Vithusan Uthayakumaran | BA/PO | Recommended | July 30, 2026 |
