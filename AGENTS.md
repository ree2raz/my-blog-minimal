# AGENTS.md - Agent Interactions and Decisions

## Project: Personal Blog with 11ty

### Context
Building a minimal, technical blog for a technical person who posts every few days with images, gifs, and links. No comments, but RSS support required. Deployment on GitHub Pages.

### Key Decisions Made

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-01-29 | Choose 11ty over other SSG options | Simpler than Jekyll (no Ruby), lighter than Hugo for JS ecosystem, full control over output |
| 2026-01-29 | Use Liquid templating | Simpler choice as requested, default in 11ty |
| 2026-01-29 | Use Nunjucks (.njk extension) | Liquid is deprecated in 11ty, Nunjucks is the recommended simpler option |
| 2026-01-29 | GitHub Actions for deployment | Automatic builds on push, no manual steps required |

### Design Decisions

| Element | Choice | Notes |
|---------|--------|-------|
| Link colors | #2a7ae2 (unvisited), #1756a9 (visited) | From reference blog, adjusted for visibility |
| Text color | #111111 | High contrast, easy reading |
| Background | #ffffff | Clean, minimal |
| Typography | System fonts stack | No external dependencies, fast loading |
| CSS approach | Custom, minimal framework | Full creative control, lightweight |

### Stack Choices
- **SSG**: Eleventy (11ty) v3.x
- **Templating**: Nunjucks
- **Styling**: Custom CSS (no frameworks)
- **Deployment**: GitHub Pages via GitHub Actions
- **Content Format**: Markdown with front matter

### Files and Their Purposes
- `.eleventy.js` - 11ty configuration and filters
- `src/_includes/layouts/` - Page templates (base, home, post)
- `src/_includes/components/` - Reusable UI pieces (header, footer)
- `src/_data/site.json` - Global site metadata
- `src/assets/css/style.css` - All styling
- `src/posts/*.md` - Blog content
- `.github/workflows/deploy.yml` - CI/CD pipeline

### Technical Considerations
- Passthrough copy for CSS and images
- Date formatting filter for post listings
- RSS feed generation using 11ty's feed plugin
- SEO-friendly meta tags in base layout
- Mobile-responsive design
- Clean, readable typography with proper max-width

### Reference Used
- reference.html - Jekyll-based blog (geohot.github.io)
- Adapted minimal, clean aesthetic with blue links on white background
- Improved: No copying exact design, added creative touches
