# semantic-portfolio

A multi-page personal portfolio website built with HTML5, advanced CSS3, and vanilla JavaScript — no frameworks, no build step. Combines **semantic markup**, **WCAG accessibility**, **SEO best practices**, and a modern **responsive, theme-able UI**.

## Features

- **Fully semantic HTML5** — `header`, `nav`, `main`, `section`, `article`, `aside`, `footer` used purposefully
- **CSS Grid** for page-level layout (header/main/footer skeleton, hero section, card grids, content + sidebar)
- **Flexbox** for navigation, header controls, and component-level layout
- **Mobile-first responsive design** with breakpoints at 600px (tablet) and 1000px (desktop)
- **CSS custom properties** — a full design-token system for color, spacing, radius, shadow, and transitions
- **Light / dark mode toggle** — persisted via `localStorage`, respects `prefers-color-scheme` on first visit, no flash of incorrect theme on load
- **Smooth animations & transitions** — section fade-ins, card hover-lift, animated hamburger icon, collapsible mobile nav — all GPU-cheap and disabled under `prefers-reduced-motion`
- **Modern card design** with hover states and consistent spacing
- **Responsive navigation menu** — hamburger menu on mobile (keyboard accessible, closes on Escape/outside click/resize), full horizontal nav on larger screens
- **Accessible by design** — proper heading hierarchy, labeled form fields, ARIA attributes, visible focus states, skip-to-content link
- **Performance-conscious** — deferred JS, lazy-loaded images, no web fonts or external frameworks

## Pages

| Page | Description |
|---|---|
| `index.html` | Home — hero section, skills overview |
| `about.html` | About — background, approach, skills, quick facts sidebar |
| `projects.html` | Projects — responsive card grid of featured work |
| `contact.html` | Contact — accessible form with labeled fields, fieldset/legend grouping, contact info sidebar |

## Project Structure

\`\`\`
semantic/
├── index.html
├── about.html
├── projects.html
├── contact.html
├── style.css
└── script.js
\`\`\`

## Theming

Dark/light mode is controlled by a `data-theme` attribute on `<html>`, toggled via the button in the header. The chosen theme is saved to `localStorage` so it persists across visits; if no preference is stored yet, the site falls back to the visitor's OS-level `prefers-color-scheme`. All colors are defined as CSS custom properties in `style.css`, so adding a new theme is a matter of adding another `[data-theme="..."]` block.

## SEO

Every page includes:

- A unique, descriptive `<title>`
- A unique `meta description` under 160 characters
- `meta name="robots" content="index, follow"`
- A `rel="canonical"` link
- Properly nested headings for crawlability

## Performance

- `script.js` loaded with `defer` so it never blocks rendering
- Project images use `loading="lazy"` and `decoding="async"`
- No web fonts, no CSS/JS frameworks, single stylesheet
- Target: Lighthouse score 90+ across Performance, Accessibility, Best Practices, and SEO

## Tech

- HTML5
- CSS3 (Grid, Flexbox, custom properties, media queries, animations)
- Vanilla JavaScript (theme toggle, mobile nav — no dependencies)

## License

MIT 

---

Built by srividya mallavarapu
