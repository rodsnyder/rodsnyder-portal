# rodsnyder.ai — Personal Portal Site

## What This Project Is

A static personal portal website for Rod Snyder at `rodsnyder.ai`. The site presents Rod as a technologist, AI researcher/developer, and writer. It serves as the hub in a hub-and-spoke domain architecture where subdomains host individual apps.

## About Rod Snyder

- **Born:** January 27, 1961
- **Background:** Technology professional, writer/journalist (257+ journalism pieces), AI researcher and developer
- **Current focus:** Artificial Intelligence research and development, building full-stack Python web apps with Claude Code
- **Writing:** Journalism archive, novels, articles — plans to publish on Medium and Substack
- **Athletics:** Competitive Masters Olympic weightlifter — 60-64 age group, 75kg weight class, East Coast Gold team, USMW
- **Recovery:** Active in AA, peer support, and recovery community organizations
- **Tools:** DEVONthink (knowledge base), NotePlan + Obsidian (notes), Claude Code (AI-assisted development)

## Domain Architecture

The domain `rodsnyder.ai` uses a hub-and-spoke model managed via Cloudflare:

| Subdomain | URL | Hosting | Status |
|-----------|-----|---------|--------|
| `@` (root) | `rodsnyder.ai` | Cloudflare Pages | **This project** |
| `guide` | `guide.rodsnyder.ai` | Railway | Live — Flask learning app |
| *(future)* | `lifting.rodsnyder.ai` | TBD | Planned — Olympic Weightlifting |
| *(future)* | `homegroup.rodsnyder.ai` | TBD | Planned — AA Home Group |

**Infrastructure details:**
- **DNS/CDN:** Cloudflare (free plan) — manages DNS, SSL, CDN
- **SSL mode:** Full (not Full Strict) — set in Cloudflare SSL/TLS settings
- **Deployment:** Cloudflare Pages — auto-deploys from GitHub on push to `main`
- **No build step needed** — plain HTML/CSS/JS, served directly
- Full domain architecture doc: `/Users/rodsnyder/Claude Code/docs/domain-architecture.md`

## Design Spec

See `docs/design-spec.md` for the complete design specification. Key points:

### Colors
| Role | Color | Hex |
|------|-------|-----|
| Primary | Deep navy blue | `#1a365d` |
| Accent | Warm gold | `#d4a843` |
| Complement | Slate gray | `#64748b` |
| Body text | Dark charcoal | `#1e293b` |
| Background | Off-white | `#f8fafc` |
| Card background | White | `#ffffff` |

### Typography
- **Headings:** Inter (Google Fonts) — clean, highly readable sans-serif
- **Body:** Inter at 1.1rem with 1.7 line-height — optimized for readability
- **No large blocks of text** — scannable sections, short paragraphs

### Layout
- **Mobile-first responsive** — works on desktop, laptop, tablet, phone
- **Browser agnostic** — no vendor-specific CSS, standard HTML5/CSS3
- **Extensible** — easy to add new sections, pages, and subdomain links

### Sections (top to bottom)
1. **Header/Nav** — Name + nav links (Home, Projects, Writing, Contact). Only active links — add future subdomains when ready
2. **Hero** — Name, tagline, brief positioning statement
3. **About** — 2-3 short paragraphs: tech background, AI focus, writing history
4. **Focus Areas** — Card grid: AI R&D, Writing & Journalism, Projects
5. **Writing** — Featured articles section (placeholder for Medium/Substack links)
6. **Footer** — Social links, email, copyright

### Social Links
Rod has accounts on: GitHub, Medium, Substack, LinkedIn, Facebook, Instagram, Reddit
*(Exact URLs to be provided — use placeholder hrefs until then)*

### Assets Needed (not yet provided)
- [ ] Professional headshot/photo
- [ ] Social profile URLs (GitHub, Medium, Substack, LinkedIn, Facebook, Instagram, Reddit)
- [ ] Bio text (or draft from context above for Rod's review)
- [ ] Favicon (generate an "RS" monogram in blue/gold)

## Tech Stack

| Component | Technology |
|-----------|-----------|
| HTML | HTML5 semantic markup |
| CSS | Vanilla CSS (no framework) — CSS Grid + Flexbox |
| Fonts | Google Fonts (Inter) |
| Icons | SVG icons for social links (inline, no external deps) |
| Hosting | Cloudflare Pages |
| Repo | GitHub (`rodsnyder/rodsnyder-portal`) |
| DNS | Cloudflare |

**No JavaScript required for v1.** No build tools, no npm, no frameworks.

## Project Structure

```
rodsnyder-portal/
├── CLAUDE.md          # This file — project instructions for Claude Code
├── TASKS.md           # Task tracker
├── .gitignore         # Git exclusions
├── index.html         # Homepage
├── style.css          # All styles
├── assets/            # Images, favicon
│   ├── favicon.svg    # Browser tab icon
│   └── headshot.jpg   # Rod's photo (when provided)
└── docs/
    ├── design-spec.md # Full design specification
    └── content-brief.md # Bio, copy, and content direction
```

## Development Workflow

1. Edit `index.html` and `style.css`
2. Use Claude Code Preview tools to view locally, take screenshots, test responsive layouts
3. Commit and push to GitHub
4. Cloudflare Pages auto-deploys (once connected in Phase 11.3)

## Session Instructions

1. At the start of each session, read `TASKS.md` to understand current progress
2. Reference `docs/design-spec.md` for colors, typography, and layout decisions
3. Reference `docs/content-brief.md` for bio text and content direction
4. Use Claude Code Preview tools to iterate visually on the design
5. After completing a task, update `TASKS.md` by checking it off

## Relationship to Other Projects

This portal project was spun out of the Claude Code Guide project:
- **Claude Code Guide repo:** `/Users/rodsnyder/Claude Code/Dev/projects/claude-code-guide/`
- **Guide site:** `guide.rodsnyder.ai` (Flask app on Railway)
- **Master task tracker:** `/Users/rodsnyder/Claude Code/TASKS.md` (Phase 11 tracks this project)
- **Domain architecture:** `/Users/rodsnyder/Claude Code/docs/domain-architecture.md`
