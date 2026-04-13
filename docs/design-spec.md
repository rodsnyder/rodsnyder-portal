# Design Specification — rodsnyder.ai

## Design Principles

1. **Scannable** — No large areas of text. Short paragraphs, card layouts, clear visual hierarchy.
2. **Responsive** — Mobile-first. Must look great on phone, tablet, laptop, and desktop.
3. **Browser agnostic** — Standard HTML5/CSS3 only. No vendor prefixes or browser-specific features.
4. **Extensible** — Easy to add new sections, pages, and subdomain links without redesigning.
5. **Accessible** — WCAG AA contrast ratios, semantic HTML, readable fonts, proper alt text.

## Color Palette

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Primary | Deep navy | `#1a365d` | Headers, nav background, buttons |
| Primary light | Medium blue | `#2d4a7c` | Hover states, secondary elements |
| Accent | Warm gold | `#d4a843` | Borders, highlights, icons, decorative accents |
| Accent dark | Deep gold | `#b8922e` | Hover state for gold elements |
| Text primary | Dark charcoal | `#1e293b` | Body text |
| Text secondary | Slate gray | `#64748b` | Captions, metadata, subtle text |
| Background | Off-white | `#f8fafc` | Page background |
| Surface | White | `#ffffff` | Cards, content areas |
| Border | Light gray | `#e2e8f0` | Card borders, dividers |

### Color Usage Rules
- **Gold on white is unreadable** — never use gold (`#d4a843`) for text on white/light backgrounds
- Gold is for: borders, decorative lines, icon fills, button accents, hover underlines
- Blue is for: headings, nav, buttons, links
- Body text is always dark charcoal (`#1e293b`) on light backgrounds or white on dark backgrounds

## Typography

| Element | Font | Size | Weight | Line Height |
|---------|------|------|--------|-------------|
| H1 (hero) | Inter | 3rem (mobile: 2rem) | 700 | 1.2 |
| H2 (section) | Inter | 2rem (mobile: 1.5rem) | 600 | 1.3 |
| H3 (card title) | Inter | 1.25rem | 600 | 1.4 |
| Body | Inter | 1.1rem | 400 | 1.7 |
| Nav links | Inter | 1rem | 500 | 1 |
| Caption | Inter | 0.9rem | 400 | 1.5 |

**Font loading:** Google Fonts CDN — `Inter` with weights 400, 500, 600, 700.

## Layout & Spacing

### Max widths
- **Content area:** 1200px max, centered
- **Text blocks:** 720px max (readable line length)
- **Cards grid:** 3 columns desktop, 2 tablet, 1 mobile

### Spacing scale
- Section padding: `5rem 0` (desktop), `3rem 0` (mobile)
- Card padding: `2rem`
- Card gap: `2rem`
- Section gap between elements: `1.5rem`

### Breakpoints
| Name | Width | Columns |
|------|-------|---------|
| Mobile | < 640px | 1 |
| Tablet | 640px–1024px | 2 |
| Desktop | > 1024px | 3 |

## Page Sections

### 1. Header/Navigation
- Fixed or sticky nav at top
- Left: "Rod Snyder" (text logo, navy blue)
- Right: Nav links — Home, Projects, Writing, Contact
- Mobile: hamburger menu or collapsed nav
- Bottom border: thin gold accent line

### 2. Hero Section
- Full-width, navy blue background
- Rod's name (large, white)
- Tagline: something like "AI Research & Development | Writer | Technologist"
- Optional: headshot photo (circular, gold border)
- Subtle gold accent — line, dot, or geometric element

### 3. About Section
- Off-white background
- 2-3 short paragraphs (max 3-4 sentences each)
- Focus: technology background, AI current work, writing history
- Optional: photo alongside text on desktop

### 4. Focus Areas (Card Grid)
- 3 cards on desktop, stacked on mobile
- Each card: icon/emoji, title, 2-3 sentence description, link
- Cards:
  - **AI Research & Development** — current focus, Claude Code, building with AI
  - **Writing & Journalism** — 257+ journalism pieces, novels, future Medium/Substack
  - **Projects** — link to guide.rodsnyder.ai and future apps

### 5. Writing Section
- Featured articles area (placeholder for Medium/Substack links)
- Card layout: title, publication, brief excerpt, read link
- Start with 2-3 placeholder cards or "Coming soon" state
- Design should accommodate 6-9 article cards at full capacity

### 6. Footer
- Navy blue background
- Social links row (SVG icons): GitHub, Medium, Substack, LinkedIn, Facebook, Instagram, Reddit
- Contact email: rod@rodsnyder.ai (when email routing is set up)
- Copyright: "© 2026 Rod Snyder"
- Gold accent line at top of footer

## SEO & Metadata

```html
<title>Rod Snyder — AI Research & Development | Writer</title>
<meta name="description" content="Rod Snyder — technologist, AI researcher and developer, and writer. Building at the intersection of artificial intelligence and human experience.">

<!-- Open Graph (social sharing) -->
<meta property="og:title" content="Rod Snyder — AI Research & Development | Writer">
<meta property="og:description" content="Technologist, AI researcher and developer, and writer.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://rodsnyder.ai">
<meta property="og:image" content="https://rodsnyder.ai/assets/og-image.png">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
```

## Favicon

- SVG format (scalable, small file)
- "RS" monogram in navy blue on transparent background, or navy circle with gold "RS"
- Also include as `<link rel="icon" type="image/svg+xml" href="/assets/favicon.svg">`

## Accessibility Checklist

- [ ] All images have alt text
- [ ] Color contrast ratios meet WCAG AA (4.5:1 for body text, 3:1 for large text)
- [ ] Semantic HTML (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- [ ] Focusable nav links with visible focus styles
- [ ] `lang="en"` on `<html>` tag
- [ ] Responsive text (no text smaller than 16px on mobile)
