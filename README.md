# My Prayer Clock — Landing Page

Production-ready static landing page for [My Prayer Clock](https://apps.apple.com/app/my-prayer-clock/id6757612033) iOS app.

## Stack

Plain HTML + CSS + vanilla JS. Zero build tools, zero dependencies. Deploys instantly to Vercel or Netlify.

## File Structure

```
my-prayer-clock/
├── index.html              # Main page
├── styles.css              # All styles
├── robots.txt              # Search engine instructions
├── sitemap.xml             # Sitemap (update URL before deploy)
├── README.md               # This file
│
├── My_Prayer_Clock_SC11.jpg   # Hero screenshot (home, light mode)
├── My_Prayer_Clock_SC21.jpg   # Alternate home screenshot
├── MPC_SC3.jpg                # Light & dark theme comparison
├── MPC_SC4.jpg                # Ramadan screen
├── Updated_Tracking.jpg       # Prayer tracker screen
├── LC_Widgets.jpg             # Lock screen widgets
└── Widgets_HS.jpg             # Home screen widgets
```

> **Important:** All `.jpg` screenshot files must be in the same directory as `index.html`.

## Deploy to Vercel

1. Install Vercel CLI: `npm i -g vercel`
2. From this directory: `vercel`
3. Follow prompts — framework: **Other**, root: `.`
4. Your site is live. Set your custom domain in the Vercel dashboard.

Or drag and drop the folder at [vercel.com/new](https://vercel.com/new).

## Deploy to Netlify

1. Drag and drop the entire folder onto [app.netlify.com](https://app.netlify.com)
2. Set your custom domain in Netlify site settings.

Or via CLI:
```bash
npm i -g netlify-cli
netlify deploy --prod --dir .
```

## Before Going Live

Update these placeholder values:

| File | What to update |
|------|----------------|
| `index.html` | `og:url` and `og:image` base URL (`https://myprayerclock.app`) |
| `index.html` | `og:image` path once images are hosted |
| `sitemap.xml` | Base URL and `lastmod` date |

## SEO Features

- Full `<head>` meta tags (title, description, keywords)
- Open Graph (Facebook, LinkedIn)
- Twitter Card
- JSON-LD structured data (`MobileApplication` schema)
- Semantic HTML5 (`header`, `main`, `section`, `footer`, proper h1→h3 hierarchy)
- `alt` text on all images
- Lazy-loaded images (except hero)
- `robots.txt` + `sitemap.xml`
- Canonical URL tag
- `prefers-reduced-motion` support

## Performance

- No JavaScript frameworks or libraries
- Fonts loaded via Google Fonts with `display=swap`
- Images lazy-loaded below the fold
- CSS animations use `will-change: transform` only where needed
- Parallax effect disabled on touch devices
