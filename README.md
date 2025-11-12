# Atlas Rapid Supply – Static Site

This repo hosts the public-facing site for Atlas Rapid Supply. Content is generated from the `/site` directory in the private ops repo and synced here for GitHub Pages.

## Deployment
- GitHub Actions workflow `.github/workflows/deploy-site.yml` publishes to Pages automatically on push to `main`.
- Custom domain is `www.atlasrapidsupply.com` (CNAME file present).
