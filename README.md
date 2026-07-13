# cybersec-blog

Hugo + [PaperMod](https://github.com/adityatelange/hugo-PaperMod), auto-deployed to
GitHub Pages via Actions, DNS/CDN on Cloudflare.

## Local setup

```bash
git clone --recurse-submodules https://github.com/yourhandle/cybersec-blog.git
cd cybersec-blog
hugo server -D    # http://localhost:1313
```

New post:

```bash
hugo new posts/my-writeup.md
```

## Repo setup (one-time)

1. Push this repo to GitHub as `cybersec-blog` (public).
2. Settings → Pages → Source → **GitHub Actions** (not "Deploy from branch").
3. Edit `hugo.toml`: set `baseURL` to your real domain, swap `yourhandle`/`yourdomain.tld`
   placeholders in `hugo.toml`, `static/CNAME`, and `static/.well-known/security.txt`.
4. Settings → Pages → Custom domain → enter your domain. This commits the `CNAME` file
   (already present under `static/` here so Hugo copies it into `public/` on build).

## Cloudflare DNS setup

1. Add your domain to Cloudflare (free plan), update nameservers at your registrar.
2. DNS tab, add:
   - `CNAME  @  yourhandle.github.io`  (or `A` records to GitHub Pages IPs if you need apex without CNAME flattening — Cloudflare supports CNAME flattening at root, so the CNAME above is fine)
   - `CNAME  www  yourhandle.github.io` (optional, for www redirect)
3. Proxy status: **Proxied (orange cloud)** — gets you Cloudflare's CDN/WAF in front of GitHub Pages for free.
4. SSL/TLS mode: set to **Full** (not Flexible) since GitHub Pages serves HTTPS natively.
5. In GitHub repo Settings → Pages, check "Enforce HTTPS" once the cert provisions (can take
   a few minutes to a few hours after DNS propagates).

## Notes

- GitHub Pages doesn't support custom response headers (no `_headers` file support like
  Cloudflare Pages), so set security headers (CSP, HSTS, etc.) via **Cloudflare
  Transform Rules / Response Header Modification** on the free plan instead.
- `content/labs/` is there if you want to publish docker-compose setups alongside writeups
  for reproducible vuln labs — not wired into the nav by default beyond the menu entry in
  `hugo.toml`.
- CI installs Hugo Extended via the `.deb` release in `deploy.yml`; bump `HUGO_VERSION`
  there when you want a newer Hugo.
