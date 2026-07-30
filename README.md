# Ruby Pizza N' Wings — Restaurant Website

A responsive, static marketing website for **Ruby Pizza N' Wings**, a family-run
pizza and wings restaurant at 162 Main St, Toronto, ON M4E 2V8. Built at the
restaurant's request to give the business its own web presence beyond its
Uber Eats listing.

## Pages & Features

| Page | What's on it |
|---|---|
| `index.html` | Hero over the storefront photo, info strip (address, hours, phone), Fan Favourites cards, Deals & Combos cards, order links |
| `Menu.html` | Full menu — 13 categories, every item with description and price, "#1/#2 most liked" badges, category jump navigation |
| `AboutUs.html` | Restaurant story, storefront photo, hours table, contact details |

Shared across all pages: sticky branded navbar with mobile hamburger menu,
footer with address/hours/phone, and "Order on Uber Eats" call-to-action links.

## Tech Stack

- **HTML5 / CSS3** — no framework, hand-written responsive layout (flexbox + grid)
- **Vanilla JavaScript** — mobile menu toggle (`assets/script.js`)
- **Font Awesome** — icons via CDN kit

## Running Locally

No build step. Serve the folder with any static server:

```bash
npx serve . -l 3005
```

Then open <http://localhost:3005>. (Opening `index.html` directly in a browser
also works.)

## Project Structure

```
rubyPizzaNWings/
├── index.html          # Home page
├── Menu.html           # Full menu
├── AboutUs.html        # About / contact page
├── assets/
│   ├── styles.css      # All styling (navbar + page sections)
│   ├── script.js       # Mobile menu toggle
│   └── images/         # Logo, storefront photo, branded promo cards
└── docs/               # Business analysis & product documentation
```

## Menu Data Source

Menu categories, item names, descriptions, and prices were populated from the
restaurant's live [Uber Eats store page](https://www.ubereats.com/ca/store/ruby-pizza-n-wings/yXwueHCQV8ON_TCOdP3NLA)
(retrieved July 30, 2026). Wing sauce options and the phone number come from
the restaurant's own branded promo cards in `assets/images/`.

## Documentation

Business analysis and product ownership artifacts for this project live in
[`docs/`](docs/):

- [Business Requirements Document (BRD)](docs/01-business-requirements.md) — why the site exists, stakeholders, scope, success metrics
- [Functional Requirements Specification (FRS)](docs/02-functional-requirements.md) — numbered functional and non-functional requirements
- [User Stories & Product Backlog](docs/03-user-stories-backlog.md) — personas, epics, stories with acceptance criteria, MoSCoW priorities
- [Release Plan & Roadmap](docs/04-release-plan.md) — v1.0 scope, future releases, Definition of Done

## License

Refer to license in repo.
