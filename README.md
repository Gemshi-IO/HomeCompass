# Home Compass — Marketing Site

Static HTML/CSS site for GitHub Pages. No build step required.

## Local preview

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8080
```

Then visit [http://localhost:8080](http://localhost:8080).

## GitHub Pages

1. Push this repository to GitHub.
2. **Settings → Pages → Build and deployment**
3. Source: **Deploy from a branch**
4. Branch: **`main`** (or your default) / **`/` (root)**
5. Save. The site will be served from `index.html` at the repo root.

`.nojekyll` is included so GitHub Pages serves all assets as-is.

### Project site (`username.github.io/repo-name/`)

If the site is **not** at the domain root, use relative paths (already used) and set your Pages **custom domain** or add a `<base href="/repo-name/">` in each HTML file if assets break. For user/org sites at `username.github.io`, root deploy works as-is.

## Structure

```
index.html          Landing page
privacy.html        Privacy stub
terms.html          Terms stub
css/styles.css      Styles (day mode design system)
js/main.js          App Store links + scroll reveal
images/             App screenshots (include telemetryscreen.jpg for Live Data HUD)
.nojekyll           GitHub Pages helper
```

## Customize

- App Store URL: edit `js/main.js` (`APP_STORE_URL`)
- Support email: edit footer in `index.html`
