# Fraction Portfolio

A single-page portfolio for Fraction, a Mumbai dance collective. It is plain HTML, CSS and JavaScript, with no build step and no framework. Everything is relative to this folder, so it runs from any GitHub account or any static host.

## Put it live on GitHub Pages

1. Create a new **public** repository on the Fraction GitHub account, for example `fraction-portfolio`.
2. Upload the **contents** of this folder to the root of that repository: `index.html`, `README.md`, `.nojekyll` and the `media` folder. Every file is under 25 MB, so dragging them into github.com → Add file → Upload files works. GitHub accepts about 100 files per upload, so upload `media` in two batches if needed.
3. Go to Settings → Pages → Build and deployment → Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)** → Save.
4. After about a minute the site is live at `https://<account>.github.io/fraction-portfolio/`.

To use a custom domain (for example `portfolio.fraction.in`), add it in Settings → Pages → Custom domain, then create a CNAME record at the domain registrar pointing to `<account>.github.io`.

## Before going public

- In `index.html`, delete the line `<meta name="robots" content="noindex,nofollow">` so search engines can list the site. It is there only while this is a trial.

## Adding content later

- **Creator cutouts:** add transparent PNGs to `media/creators/`, named `yashraj-mukhate.png`, `just-neel-things.png`, `prosenjit-kundu.png` and `ruhee-dosani.png`. They replace the placeholders automatically.
- **Client logos:** add PNGs to `media/logos/`, named `fastandup.png`, `kameezing.png`, `the-souled-store.png`, `sharjah-warriors.png`, `airtel.png`, `imap.png`, `jaadu.png` and `anant-khamkar.png`. Each logo replaces its name card.
- **Client video links:** in `index.html`, find `const CLIENTS` and paste the video URL as the fourth value on that client's line. An empty `""` shows "Video link needed".
- **Dance films:** in `index.html`, find `const FILMS`. Each line is one playlist row: title, label, thumbnail, preview clip and the full-film link.

## Moving it to another account

On GitHub, go to repository Settings → General → Danger Zone → **Transfer ownership**. Pages settings move with the repository. If the site was served from a different account's `github.io` address, that address changes to the new owner's.
