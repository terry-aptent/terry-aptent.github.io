# Aptent LLC website

Static one-page site: `index.html`, `style.css`, `script.js`. No build step — open `index.html` directly to preview, or push it to GitHub Pages for a public URL.

## Push to GitHub

This folder is already a git repo with everything committed on branch `master`. From this folder:

```bash
git branch -m main
git remote add origin https://github.com/aptent/REPO_NAME.git
git push -u origin main
```

Replace `REPO_NAME` with whatever you name the repo on GitHub.com under the `aptent` account/org (create it first at github.com/new — don't initialize it with a README, since this folder already has one and it'll cause a conflict).

**Repo name matters for the URL:**
- Name it `aptent.github.io` → site is live at `https://aptent.github.io/` (clean root URL, but you only get one repo like this per account).
- Any other name (e.g. `aptent-site`) → site is live at `https://aptent.github.io/aptent-site/`.

## Turn on GitHub Pages

1. On GitHub, go to the repo → **Settings** → **Pages**.
2. Under "Build and deployment," set **Source** to `Deploy from a branch`.
3. Branch: `main`, folder: `/ (root)`. Save.
4. Wait ~1 minute, then visit the URL GitHub shows on that page.

## Contact form

The form on the Contact section posts to Formspree (`https://formspree.io/f/YOUR_FORM_ID` in `index.html`), since GitHub Pages can't run server code to send emails itself.

1. Sign up free at [formspree.io](https://formspree.io), create a form pointed at `terry@aptent.co`.
2. Copy the form endpoint it gives you.
3. In `index.html`, replace `YOUR_FORM_ID` in the `<form action="...">` line with your real ID.

Until that's done, the form will show an error on submit — email and LinkedIn links work regardless.

## Editing content later

Everything is plain HTML/CSS in `index.html` and `style.css` — no framework. Open a terminal in this folder, run `claude`, and just describe the change (e.g. "add a sixth portfolio company called X").
