# TMA Security website

The production site is published from the `main` branch of [tmasecurity/tmasecurity.github.io](https://github.com/tmasecurity/tmasecurity.github.io) via GitHub Pages at [tmasecurity.com](https://tmasecurity.com/).

## Edit and publish

Edit `index.html` for content and `styles.css` for layout. Commit and push to `main`; GitHub Pages publishes the repository root. The `concepts/` directory contains unpublished design explorations and is excluded from Git.

## Domain and email

`CNAME` sets the Pages custom domain to `tmasecurity.com`. Cloudflare DNS points the apex to GitHub Pages' four IPv4 addresses (`185.199.108.153` through `185.199.111.153`), and `www` is a CNAME to `tmasecurity.github.io`. These web records are DNS-only so GitHub can issue and manage the HTTPS certificate.

Mail routing is separate: keep the existing Cloudflare Email Routing MX, SPF and DKIM records and the verified forwarding destination when updating web DNS. Website inquiries use `info@tmasecurity.com`; vulnerability reports can use `security@tmasecurity.com`.

## Local preview

From the repository root, run `python -m http.server 8124` and open `http://127.0.0.1:8124/`. The site needs no build step or external assets.
