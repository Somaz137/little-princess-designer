# Little Princess Designer

Storefront site for **Little Princess Designer**, a Lahore-based made-to-order atelier for girls', boys', and baby party wear. Browse the catalog and reach out via WhatsApp, email, or phone to order — no cart or checkout, just a showcase that drives inquiries.

## Structure

- `index.html` — the whole site (plain HTML/CSS/JS, no build step, no dependencies)
- `products.json` — the product catalog, edited via the `/admin` CMS below
- `admin/` — [Decap CMS](https://decapcms.org/) setup for editing products without touching code
- `uploads/` — logo assets (product photos uploaded via the CMS also land here, under `uploads/products/`)

## Editing products

`index.html` fetches `products.json` on load. Edit that file (directly, or through `/admin` once deployed) to add products, change prices, or update descriptions — no code changes needed.

## Deploying (Netlify + Decap CMS)

1. Push this repo to GitHub (already done if you're reading this from GitHub).
2. In [Netlify](https://app.netlify.com), **Add new site → Import from GitHub**, pick this repo. No build command needed — publish directory is `/` (repo root).
3. In Netlify, enable **Identity** (Site configuration → Identity → Enable) and under Identity settings enable **Git Gateway**.
4. Invite yourself as a user under Site configuration → Identity → Invite users.
5. Visit `yoursite.netlify.app/admin`, log in, and edit products through the form. Each save commits to `products.json` and Netlify auto-redeploys.

## Local preview

Just open `index.html` in a browser, or serve the folder with any static file server, e.g.:

```
npx serve .
```
