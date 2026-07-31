# getvocablo.com

Marketing site for [Vocablo](https://apps.apple.com/app/vocablo-learn-mexican-spanish/id6790215871),
a fully native, fully on-device app that puts Mexican Spanish vocabulary
widgets on the iPhone Home Screen and Lock Screen, the iPad Home Screen, and
the Mac desktop.

Live at **[getvocablo.com](https://getvocablo.com)**, served by GitHub Pages.

## Layout

```
index.html         The site — a single static page, no build step, no dependencies
assets/            Optimized images (WebP), the app icon (SVG), and the hero video
legal/privacy.txt  Vocablo's privacy policy
llms.txt           Canonical app facts for AI answer engines
robots.txt         Crawler policy + sitemap pointer
sitemap.xml        Single-URL sitemap
CNAME              Custom domain for GitHub Pages
.nojekyll          Serve files as-is (skip Jekyll processing)
```

## Editing

Everything is hand-written HTML/CSS in `index.html` (styles inlined for a
single fast request; the only JavaScript is the promo-expiry gate at the
bottom of the file). Edit, commit, push — GitHub Pages redeploys automatically.

Things to keep in sync when the app changes:

- Pricing and feature claims appear in three places: the visible page, the
  `SoftwareApplication` JSON-LD block, and `llms.txt`.
- The FAQ section and the `FAQPage` JSON-LD block mirror each other.
- The promo button (`#promo`) reads its offer code and expiry from data
  attributes and hides itself after the expiry date.
