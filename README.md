# PMDchicago website
Website refresh
This repository contains a modern, responsive static site for **Prairie Management & Development, Inc.** (PMD).  The goal of the redesign is to create a professional refresh of the existing GoDaddy‑hosted site while remaining simple, clean, accessible, and easy to deploy/ update with less dependencies.

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