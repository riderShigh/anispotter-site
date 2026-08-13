# Deploying this site

This is a static site (no build step) — deploy it as-is to any static host: GitHub Pages, Cloudflare Pages, Netlify, Vercel, or S3+CloudFront.
For GitHub Pages: enable Pages on this repo pointing at this directory (or push its contents to a `gh-pages` branch / the `docs/` root), then set the custom domain to `anispotter.com` via the repo Settings → Pages and a `CNAME` file.
For Cloudflare Pages: create a project with this directory as the output/root, no build command needed, and attach the `anispotter.com` custom domain.
The host must serve `privacy/index.html` at `/privacy` and `terms/index.html` at `/terms` (most static hosts do this automatically for `<dir>/index.html` — no extra rewrite rules needed).
HTTPS is required (App Store Connect will reject an http:// URL) — all of the hosts above provision TLS automatically for custom domains.
