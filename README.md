# En Circle — Legal site

Static Privacy Policy + Terms of Service pages for the En Circle app, hosted on GitHub Pages.

## Publish (one time)

From inside this `legal-site/` folder:

```bash
# 1. Create a NEW public repo on GitHub named "encircle-legal" (via the website
#    or the gh CLI below), then push just these files into it:
gh repo create encircle-legal --public --source=. --remote=origin --push

# If you'd rather do it by hand:
#   git init && git add . && git commit -m "En Circle legal pages"
#   git branch -M main
#   git remote add origin https://github.com/<YOUR_GH_USERNAME>/encircle-legal.git
#   git push -u origin main
```

Then on github.com: **Settings → Pages → Build and deployment → Source: Deploy from a branch → main / (root) → Save.**

After ~1 minute the pages are live at:

- `https://<YOUR_GH_USERNAME>.github.io/encircle-legal/privacy.html`
- `https://<YOUR_GH_USERNAME>.github.io/encircle-legal/terms.html`

## Update the app + store listings

Put those two URLs into:
- `constants/app.ts` (`PRIVACY_URL`, `TERMS_URL`) in the main app repo
- App Store Connect (App Privacy → Privacy Policy URL)
- Google Play Console (Store presence → Privacy policy)

## Before shipping
- Replace `[STATE]` in `terms.html` (governing-law state, e.g. the state where the LLC is registered).
