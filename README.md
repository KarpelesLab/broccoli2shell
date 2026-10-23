# broccoli2shell.com

A static page about CVE-2026-111497 (Brotli decoder out-of-bounds write).
It's served by Cloudflare Workers static assets.

- `public/` holds the site: `index.html`, `404.html`, and `_headers` for the security headers.
- `wrangler.jsonc` holds the Worker config. It attaches the apex and `www` as custom domains.

## Deploy

Pushes to `master` deploy automatically through Cloudflare Workers Builds.

To deploy by hand:

    npx wrangler login
    npx wrangler deploy
