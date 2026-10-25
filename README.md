# Apps Website

Static overview for Patrick Steiner's personal hobby apps, intended for `app.helmsdeep.at`.

## Structure

- `Website/` is the complete deployable document root.
- `Website/assets/` contains the app icons.
- `Website/privacy/carlo/`, `hydro/`, and `streak/` provide their app-specific privacy URLs.
- Raccoon's website and privacy policy intentionally remain at `raccoon.helmsdeep.at`.

## Local preview

```sh
cd Website
python3 -m http.server 4173
```

Open `http://127.0.0.1:4173`.

## Caddy deployment

Copy the contents of `Website/` to the configured document root, then adapt the path in `Caddyfile` if necessary:

```caddy
app.helmsdeep.at {
  root * /var/www/apps-website
  file_server
  encode zstd gzip
}
```

No build step, JavaScript, package manager, or external font is required.

## Adding an app

1. Add the app icon to `Website/assets/`.
2. Add an app card in `Website/index.html` in alphabetical order.
3. Add a matching privacy page under `Website/privacy/<slug>/` or link to the app's existing privacy URL.
4. Keep the privacy links in the footer in the same alphabetical order.

## Privacy policy review

The Carlo, Hydro, and Streak privacy documents were imported from their existing websites without content changes. Review their accuracy before deploying, especially where the texts mention logging, third-party providers, or data collection.
