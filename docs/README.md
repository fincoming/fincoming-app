# FIncoming website (static)

Host this folder at **https://fincoming.app** for App Store Connect and in-app legal links.

Published via **GitHub Pages** from the `/docs` folder on `main`.

## Pages

| URL | Purpose |
|-----|---------|
| `/` | Home (marketing-lite) |
| `/support/` | **Support URL** (required by App Store) |
| `/privacy/` | Privacy policy |
| `/terms/` | Terms of service |

## Deploy with GitHub Pages

1. Push this repo to GitHub.
2. **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: `main` (or your default)
   - Folder: **`/docs`**
3. **Custom domain:** `fincoming.app` (matches `CNAME` in this folder).
4. At your domain registrar, add DNS (GitHub documents current IPs — verify in Pages settings):
   - **Apex** `fincoming.app`: A records → GitHub Pages IPs, **or**
   - **CNAME** `www` → `YOUR_USERNAME.github.io` if you only use www
5. Enable **Enforce HTTPS** after DNS propagates.

## Deploy with Cloudflare Pages

1. Connect the GitHub repo.
2. Build command: *(none)* — static site.
3. Output directory: `docs`
4. Custom domain: `fincoming.app`

## App Store Connect

Use these URLs when submitting:

- **Privacy Policy URL:** `https://fincoming.app/privacy/`
- **Support URL:** `https://fincoming.app/support/`
- **Marketing URL (optional):** `https://fincoming.app/`

## Other domains

You can redirect `getfincoming.com` and `fincoming.net` to `https://fincoming.app` at your registrar or Cloudflare.

## Local preview

```bash
cd docs && python3 -m http.server 8080
```

Open http://localhost:8080/
