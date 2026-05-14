# Quack® like a duck — Safety Platform Website

**Source file:** Originally `quikrete_safety_platform_2.html` (rebranded — Quikrete name dropped due to trademark)
**Current brand:** Quack® like a duck
**Status:** Active development — single-page HTML, self-contained (no build step required)

---

## Folder Structure

```
quack-like-a-duck-safety-platform/
├── index.html       ← Main website (edit this file)
├── assets/          ← Drop images, logos, icons here as needed
├── deploy/          ← Deployment scripts and hosting config
└── README.md
```

## Editing

Open `index.html` directly in a browser to preview. All CSS and JS is embedded in the single file — no dependencies to install. To edit:

- **Brand/copy changes:** search `Quack® like a duck` to find all brand references
- **Colors:** CSS variables are at the top of the `<style>` block (`:root { ... }`)
- **Navigation sections:** each page is a `.route` div — find by searching `class="route"`
- **Logo mark text:** look for `class="logo-mark"` inside the `<nav>` block

## Deploy

### Option 1 — Static host (Netlify / Vercel / S3)
Drag `index.html` into Netlify Drop or upload to S3 + CloudFront. No build needed.

### Option 2 — AWS S3 + CloudFront (recommended for enterprise clients)
See `deploy/aws-deploy.md` (create when ready). Basic steps:
1. `aws s3 cp index.html s3://YOUR-BUCKET/index.html --content-type text/html`
2. Invalidate CloudFront: `aws cloudfront create-invalidation --distribution-id YOUR-ID --paths "/*"`

### Option 3 — GitHub Pages
Push `index.html` to a repo root and enable Pages in repo settings. Free and instant.

## Trademark Note

The original client name **QUIKRETE** was removed due to trademark conflict (Quikrete is a registered concrete brand).
Current placeholder brand: **Quack® like a duck** — replace with the actual client/product name before going live.
