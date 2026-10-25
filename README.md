# Apps

A small, static overview of Patrick's personal hobby apps at `apps.helmsdeep.at`.

## Structure

- `Website/` contains the deployable site.
- `Website/assets/` contains app icons.
- `Website/privacy/` contains the local privacy pages.
- Raccoon's website and privacy page remain at `raccoon.helmsdeep.at`.

## Local preview

```sh
cd Website
python3 -m http.server 4173
```

Open `http://127.0.0.1:4173`.

## Deployment

Every push to `main` deploys `Website/` to GitHub Pages via `.github/workflows/deploy-pages.yml`.

No build step, JavaScript, package manager, or external font is needed.

## Adding an app

1. Add the app icon to `Website/assets/`.
2. Add an app card in `Website/index.html` in alphabetical order.
3. Add a matching privacy page under `Website/privacy/<slug>/` or link to the app's existing privacy URL.
4. Keep the privacy links in the footer in the same alphabetical order.

## Privacy policy review

Review the local privacy documents for Carlo, Hydro, and Streak before publishing changes, especially where they mention logging, third-party providers, or data collection.
