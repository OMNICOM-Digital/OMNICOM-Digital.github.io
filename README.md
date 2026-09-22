# Omnicom Digital GitHub Pages site

Source for a GitHub Pages landing page showcasing Omnicom's open-source / dev-facing
work, currently the GLPI MCP Server plugin, plus a few internal tools built along the way.

## Files

- `index.html`: the page content
- `style.css`: styling (dark theme, Omnicom brand red `#c2304e` / `#c61f40`, IBM Plex Sans)

No build step. It's plain HTML/CSS, so GitHub Pages can serve it as-is.

## Publishing this on GitHub

1. **Create the org/repo.** If `github.com/OMNICOM-Digital` doesn't exist yet, create it
   (Settings → New organization), or use whatever handle you actually register, swapping the
   `OMNICOM-Digital` links in `index.html` if you pick a different name.
   For a single showcase page, the repo is usually named `OMNICOM-Digital.github.io`
   (this makes the site live at `https://OMNICOM-Digital.github.io` with no extra config).
   A repo with any other name also works. Pages just serves it at
   `https://OMNICOM-Digital.github.io/<repo-name>/` instead.

2. **Push these files** to the repo's default branch (`main`):
   ```bash
   git init
   git add index.html style.css README.md
   git commit -m "Initial GitHub Pages site"
   git branch -M main
   git remote add origin https://github.com/OMNICOM-Digital/<repo-name>.git
   git push -u origin main
   ```

3. **Enable Pages.** In the repo, go to Settings → Pages → Build and deployment → Source →
   "Deploy from a branch" → pick `main` / `/ (root)` → Save. The site goes live in a minute
   or two at the URL GitHub shows there.

4. **Optional: custom domain.** If you'd rather serve this at something like
   `dev.omnicom.digital`, add a `CNAME` file with that hostname and point a DNS `CNAME`
   record at `OMNICOM-Digital.github.io`. GitHub's Pages docs walk through the exact
   DNS records.

## Before it goes public, double-check

- Swap every `github.com/OMNICOM-Digital` link in `index.html` for your real org handle.
- The GLPI MCP Server plugin project card is marked "In development" with no repo link yet.
  Add the actual repo link (and flip the status badge) once it's public.
- The "internal tooling" cards (notification templates, icon sets, backup scripts) are
  described but not linked, since they're not on GitHub yet. Link them if/when they are,
  or drop the cards if they should stay internal.
