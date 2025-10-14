# Prairie Management & Development, Inc. Website

This repository contains a modern, responsive static site for **Prairie Management & Development, Inc.** (PMD).  The goal of the redesign is to create a professional refresh of the existing GoDaddy‑hosted site while remaining simple, accessible and easy to deploy.

## Project structure

The site is organised into a handful of HTML pages with a small collection of static assets.  TailwindCSS is pulled from a CDN for rapid styling.

```
├── index.html        # Home page with hero banner and mission overview
├── about.html        # About page describing the company’s history and mission
├── careers.html      # Careers page highlighting typical roles and how to apply
├── contact.html      # Contact page with a simple contact form and Google Map
├── assets/
│   ├── css/
│   │   └── style.css     # Custom stylesheet replacing Tailwind
│   └── img/
│       ├── hero-real.jpg # Real Chicago skyline used on the home page
│       ├── about.png     # Illustration for the About page
│       └── careers.png   # Illustration for the Careers page
└── README.md         # This document
```

## Viewing locally

No build process is required.  Simply open `index.html` in a modern web browser to view the site.  All styling is provided by a local CSS file located in `assets/css/style.css`, so the site will render correctly even without an Internet connection.  The homepage features a real photograph of the Chicago skyline (`hero-real.jpg`), and the interior pages reuse a consistent navigation and layout.

## Deploying to Vercel

1. **Create a repository:** Create a new GitHub repository named `pmdchicago-site` under your account (for example, *btec*) and commit all files from this project into the repository.

2. **Connect to Vercel:** Sign in to [Vercel](https://vercel.com/) with your GitHub account.  Import the `pmdchicago-site` repository.  When asked for a framework preset, select **Other** since this is a pure static site.  Vercel will detect the `index.html` file in the root and automatically configure the build.

3. **Deploy:** Click **Deploy**.  Vercel will upload the files and provide a unique preview URL as well as a production URL.  HTTPS is automatically configured by Vercel for custom domains.

4. **Add the custom domain:** Once the site is working on Vercel, add your custom domain (`pmdchicago.com`) in the Vercel dashboard under **Domains**.  Vercel will generate DNS records (usually a `CNAME` for the `www` subdomain and an `A` record for the root) that need to be added to your GoDaddy DNS settings.

## DNS setup notes

To point your domain to Vercel, update your GoDaddy DNS settings:

1. Log in to your GoDaddy account and navigate to the DNS management page for `pmdchicago.com`.
2. Remove any existing DNS records that point to the old hosting provider (e.g., legacy `A` or `CNAME` records).
3. Add the DNS records provided by Vercel.  Typically this involves:
   - A `CNAME` record for the `www` subdomain pointing to a Vercel-provided domain (e.g., `cname.vercel-dns.com`).
   - An `A` record for the root (`@`) pointing to the IP address that Vercel specifies.
4. Save your changes.  DNS propagation can take up to 24 hours, though updates often appear within minutes.  Once propagated, visiting `pmdchicago.com` will load the new site served from Vercel over HTTPS.

## Licence and content

The custom CSS and HTML in this project are released for your use without restriction.  Images in the `assets/img` directory include a photograph of the Chicago skyline downloaded from the original GoDaddy site as well as abstract illustrations created for this project.  They are intended as placeholders; feel free to replace them with high‑quality photos of your properties or other approved imagery when it becomes available.  The text used on the pages summarises PMD’s mission and history and can be updated when official language is provided.
