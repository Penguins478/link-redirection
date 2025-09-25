linkyapp.dev — hosting instructions

This repository contains a simple static redirect page. Below are recommended steps to host it on your custom domain `linkyapp.dev`.

1) Choose a static hosting provider

- Cloudflare Pages (recommended): free, automatic HTTPS, easy DNS integration with Cloudflare registrar or external registrars.
- GitHub Pages, Netlify, Vercel: all work well for static content.

2) Deploy options

- Connect this repository to Cloudflare Pages and build (no build step needed for static files). Set the build output folder to the repository root.
- For GitHub Pages, enable Pages in repo settings and select branch `main` and folder `/`.
- For Netlify/Vercel, drag-and-drop the site folder or connect the repo and use default settings.

3) Point your domain DNS

- For apex/root domain (linkyapp.dev) Cloudflare Pages recommends adding an A record pointing to Cloudflare's IPs or using the ALIAS/ANAME feature at your registrar. If using Cloudflare, simply set your nameservers to Cloudflare and add the domain in Pages.
- For GitHub Pages, create A records to GitHub Pages IPs and a CNAME for `www`.

4) CNAME

This repo includes a `CNAME` file containing `linkyapp.dev`. Hosting providers that use this (GitHub Pages) will pick up the custom domain automatically. For others, configure the custom domain in the provider dashboard.

5) Enable HTTPS

Most providers enable HTTPS automatically once DNS is correct. On Cloudflare make sure "SSL/TLS" is set to "Full" or "Flexible" depending on your setup.

6) Verify

- Wait for DNS propagation (usually minutes but can be up to 48 hours). Use `dig` or `nslookup` to check.
- Visit https://linkyapp.dev and confirm it redirects.

If you want me to set this up step-by-step with Cloudflare Pages or GitHub Pages, tell me which provider you prefer and whether you control the domain's DNS (which registrar or Cloudflare account). I can then provide exact DNS records and walk through connecting the repo.
