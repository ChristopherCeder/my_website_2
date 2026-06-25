# CederBI — Christopher Ceder Consulting Website

The live site for [cederbi.com](https://cederbi.com) — Christopher Ceder's fractional CEO and operations consulting practice. A fully static site (no build step, no framework) hosted on GitHub Pages.

## File Structure

```
├── index.html           # Home page
├── services.html        # Services detail page (3 tiers + FAQ)
├── about.html           # About page
├── contact.html         # Contact page (Formspree-powered form)
├── logo.png             # Site logo
├── headshot-home.jpg    # Headshot used on home page
├── headshot-about.jpg   # Headshot used on about page
├── favicon.png          # Favicon
├── CNAME                # Custom domain config (cederbi.com)
├── .nojekyll             # Disables Jekyll processing on GitHub Pages
└── README.md
```

CSS and JavaScript are inline within each HTML file — there is no separate `/css` or `/js` directory. This is intentional; each page is self-contained.

## Hosting & Domain

- Hosted on **GitHub Pages**, serving from the `main` branch root.
- Custom domain `cederbi.com` is configured via the `CNAME` file plus DNS records managed through **Squarespace Domains**.
- `.nojekyll` is present to prevent GitHub Pages' default Jekyll build step from interfering with file/folder names (this previously caused a build conflict — see Known Issues history below).

## Contact Form

The contact form on `contact.html` submits via **[Formspree](https://formspree.io)**. Submissions are emailed to `christopher@cederbi.com`.

> Considering a switch to a plain `mailto:` link instead, to avoid the third-party dependency — tradeoff is that `mailto:` requires the visitor's own email client to send, which has a higher drop-off rate than a silent form POST. Not yet decided.

## Editing

No build process, no dependencies, no npm. Edit the HTML files directly and push to `main` — GitHub Pages redeploys automatically within a minute or two.

## Status / Known Issues

No known outstanding issues at this time. This section will be updated as new items come up.

## Brand Voice Notes

Copy across the site favors direct, confident, no-fluff language — avoids generic consulting jargon. Keep this tone consistent in any future copy edits or new pages (e.g. blog/article content).
