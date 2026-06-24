# Christopher Ceder — Consulting Website

A clean, modern static site for Christopher Ceder's fractional CEO and operations consulting business.

## File Structure

```
├── index.html          # Home page
├── services.html       # Services detail page
├── about.html          # About page
├── contact.html        # Contact page
├── css/
│   └── style.css       # All styles
├── js/
│   └── main.js         # Nav, FAQ accordion, smooth scroll
└── README.md
```

## Deploying to GitHub Pages

### Option A — Root of repo (simplest)
1. Copy all these files into the **root** of your GitHub repo (`my_website` or whatever it's named).
2. Go to **Settings → Pages**.
3. Under "Source", choose **Deploy from a branch** → `main` (or `master`) → `/` (root).
4. Save. Your site will be live at `https://christopherceder.github.io/<repo-name>/` within a minute or two.

### Option B — Custom domain
1. Deploy as above first and confirm it works.
2. Add a file called `CNAME` to the root of the repo containing just your domain:
   ```
   christopherceder.com
   ```
3. In your domain registrar's DNS settings, add:
   - An **A record** pointing to `185.199.108.153` (and optionally the other GitHub IPs: `.109`, `.110`, `.111`)
   - Or a **CNAME record** pointing `www` → `christopherceder.github.io`
4. In **Settings → Pages**, enter your custom domain and check "Enforce HTTPS."

## Things to customize before going live

- **Contact form**: The form uses [Formspree](https://formspree.io) (free tier available). Sign up, create a form, and replace `YOUR_FORM_ID` in `contact.html` with your actual ID.
  ```html
  action="https://formspree.io/f/YOUR_FORM_ID"
  ```
- **Email & phone**: Update `hello@christopherceder.com` and the SMS link in `contact.html` with your real contact info.
- **Photo**: Replace the placeholder `.img-frame` divs in `about.html` and `index.html` with real `<img>` tags pointing to your headshot.
- **Testimonials**: Swap the placeholder quote in `index.html` with a real one from a client.
- **Meta tags / SEO**: Update the `<title>` and `<meta name="description">` tags if you want to adjust how your pages appear in Google.

## Fonts

The site uses Google Fonts (Fraunces + Inter), loaded via CDN. No build step needed — it works as plain HTML/CSS/JS.

## No build process required

This is a fully static site. No npm, no bundler, no framework. Just drag the files into your repo and it works.
