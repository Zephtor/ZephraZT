# Zephra OS website

Standalone static website for Zephra OS, separate from the Archiso profile and ISO build. The canonical domain is `https://zephtor.org/`.

## Preview locally

From this directory, start a static file server:

```sh
python -m http.server 8000
```

Open `http://localhost:8000/`. No build step or package manager is needed. Google Fonts are optional; system font fallbacks are included. Stop the server with `Ctrl+C`.

## Deploy to your domain

1. Choose a static hosting provider (for example Codeberg Pages, GitHub Pages, Cloudflare Pages, Netlify, or your own web host).
2. Upload/publish the **contents** of this directory as the site root.
3. Add `zephtor.org` as a custom domain in the hosting provider.
4. At your DNS provider, configure only the DNS records supplied by the host. Record types and target values depend on the service; do not guess or reuse generic IP addresses.
5. Enable HTTPS at the host. If you want `www.zephtor.org`, configure it as an additional name and redirect it to the canonical domain.
6. Check the homepage, `/docs/`, `robots.txt`, `sitemap.xml`, the custom 404 page, and HTTPS after DNS has propagated.

The site uses relative asset and page links and is intended for the domain root. Canonical URLs currently use `https://zephtor.org/`.

## Before publishing

- Replace the placeholder repository URL only after confirming the public repository address.
- Confirm the current project status and test warnings. The site intentionally does not advertise an official ISO download because one has not been verified/published.
- Confirm project and asset licensing, contributor contact details, and privacy/legal requirements for the intended audience and hosting region.
- Google Fonts are loaded from Google when online; remove those font links if you prefer a fully third-party-free page. The page has local system-font fallbacks.

## Contents

- `index.html` — landing page, project overview, status, FAQ preview, and contribution entry point
- `docs/` — overview, status/roadmap, VM safety, and FAQ
- `styles.css` — responsive shared styles
- `script.js` — accessible mobile menu and current-year label
- `assets/favicon.svg` — site icon
- `robots.txt`, `sitemap.xml`, `404.html` — basic static-hosting support
