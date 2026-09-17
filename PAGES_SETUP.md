# GitHub Pages Setup Instructions

The corporate site is ready to deploy. To enable GitHub Pages:

## Steps to Enable

1. Go to the repository settings: https://github.com/Dream-Invent-Inspire/dreaminventinspire.com/settings/pages
2. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
3. Save the settings

## What Happens Next

Once enabled, the workflow will automatically:
- Deploy the site from the `main` branch
- Make it available at: https://dream-invent-inspire.github.io/dreaminventinspire.com/

## After Deployment

The site will be live at the GitHub Pages URL. When ready, point the `dreaminventinspire.com` DNS to the Pages site by:

1. Adding a `CNAME` file with `dreaminventinspire.com` (if desired)
2. Configuring DNS records:
   - `A` records pointing to GitHub Pages IPs
   - Or `CNAME` record for subdomain

## Manual Deployment Trigger

After Pages is enabled, you can manually trigger a deployment:
```bash
gh workflow run pages.yml
```

Or push any change to the `main` branch to trigger automatic deployment.
