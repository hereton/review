# Commercial Platform — Permission Center Architecture Reviews

GitHub Pages site hosting architecture reviews for the Permission Center system.

## Tech Stack

- **HTML5** — static pages, no framework
- **Tailwind CSS** — loaded via CDN
- **Mermaid.js v11** — diagram rendering via CDN ES module
- No build tools or package managers required

## Directory Structure

```
github-pages/
├── docs/
│   ├── index.html                                          # Landing page with navigation
│   ├── api-03-architecture-review-2026-05-25.html
│   ├── api-03-architecture-review-backend-2026-05-25.html
│   ├── api-03-db-review-2026-05-25.html
│   ├── api-04-architecture-review-2026-05-25.html
│   ├── api-04-architecture-review-backend-2026-05-25.html
│   ├── api-04-db-review-2026-05-25.html
│   ├── web-03-architecture-review-2026-05-25.html
│   ├── web-03-architecture-review-frontend-2026-05-25.html
│   ├── web-04-architecture-review-2026-05-25.html
│   └── web-04-architecture-review-frontend-2026-05-25.html
└── README.md
```

## File Naming Convention

```
{scope}-{iteration}-{type}-{date}.html
```

| Segment     | Values                          |
|-------------|---------------------------------|
| `scope`     | `api`, `web`                    |
| `iteration` | `03`, `04`                      |
| `type`      | `architecture-review`, `architecture-review-backend`, `architecture-review-frontend`, `db-review` |
| `date`      | `YYYY-MM-DD`                    |

## File Breakdown

| Category | Count | Description |
|----------|-------|-------------|
| Landing page | 1 | `index.html` — navigation to all reviews |
| Architecture reviews | 4 | Full-stack architecture analysis (api + web, iterations 03–04) |
| Backend reviews | 2 | Go/Gin backend deep-dives (api iterations 03–04) |
| Frontend reviews | 2 | React/TypeScript frontend deep-dives (web iterations 03–04) |
| DB reviews | 2 | PostgreSQL schema reviews (api iterations 03–04) |

## Review Content

Each review file follows a consistent structure:

- **Header** — project info, tech stack, scale metrics, review date
- **Candidates** — refactoring candidates with before/after Mermaid diagrams
- **Badges** — recommendation strength indicators:
  - **Strong** (green) — high impact, low risk
  - **Worth Exploring** (amber) — moderate value
  - **Speculative** (gray) — future consideration
- **Layer color-coding** — Presentation (indigo), Application (violet), Domain (sky), Infrastructure (amber)
- **Recommendations** — prioritized implementation order

## Deployment

Served via GitHub Pages from the `docs/` directory. No build step needed — push HTML files and the site updates.
