# Landing Site Deployment

The `site/` folder is a static one-pager (HTML + CSS). Deploy it anywhere that serves static files.

## Local Preview
```bash
cd site
npx serve .
# or: python -m http.server 4173
```

## GitHub Pages
1. In the repo root run:
   ```bash
   git subtree push --prefix site origin gh-pages
   ```
2. In GitHub → Settings → Pages, set the source to the `gh-pages` branch / root.
3. Update the intake form link in `site/index.html` once your Tally/Typeform URL is live.

## Vercel / Netlify
1. Create a new project and point it at the repo.
2. Set build command to `npm run build` (not needed) and output directory to `site`.
3. Redeploy whenever `site/` changes or connect to `main` for automatic deploys.

## Environment Variables
None needed—the form currently posts to `https://tally.so/...`. Swap in your actual intake URL + analytics snippets (Plausible, GA4, etc.) before going live.

## Optional Enhancements
- Add `site/package.json` with a build script using Vite if you want components.
- Wire the form submission directly to Make/Zapier via webhook for real-time alerts.
