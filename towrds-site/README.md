# Towrds 10: Work With Me

Static landing page for GitHub Pages. No build step.

## Files
- `index.html` : the full page (HTML + CSS inline, fonts from Google Fonts)
- `favicon.svg` : browser tab icon
- `.nojekyll` : tells GitHub Pages to serve files as-is

## Deploy
1. Create a repo (e.g. `towrds-site`) and upload these files to the root of the `main` branch.
2. Repo **Settings > Pages**: Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)`. Save.
3. Custom domain: in the same Pages screen, enter your domain (e.g. `www.towrds.com`) and save. GitHub adds a `CNAME` file to the repo.
4. At your DNS provider:
   - `www` subdomain: CNAME record pointing to `<your-github-username>.github.io`
   - Apex domain (`towrds.com`): A records to 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
5. Once DNS resolves, check **Enforce HTTPS** in Settings > Pages.

## Before launch
- Swap the Capability Brief video placeholder (search `[Capability Brief video embed]`) for your YouTube/Vimeo/Loom embed.
- Swap the photo placeholder (search `[Photo: David`) for an `<img>` tag, and add the image file to the repo.
- Note: `www.towrds.com` currently points at Substack. Moving the domain to GitHub Pages moves the whole domain, including your Substack posts, unless you keep Substack on a subdomain.
