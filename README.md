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

- **Phone-only video:** the title and Fashion Film sections play a vertical cut on phones (`media/ffv-*.mp4`) and the landscape cut on larger screens. Any `<video>` with `data-msrc` and `data-dsrc` switches the same way.

- **Creator cards:** in `index.html`, find `const CREATORS`. Each line is name, front photo and back photo (Fraction with that creator), all square WebP in `media/creators/`. The card flips in 3D on tap; a creator without a group photo repeats the front image as the back.
- **Worked with (logo carousel):** in `index.html`, find `const LOGOS`. Each line is one logo: name, image file in `media/logos/` (transparent PNG), optional link to a film, and a height that evens out wide and tall marks. Add a line and drop in the file; the row scrolls endlessly and pauses on hover.
- **Brand films collage:** the two stacked tiles (Fast&Up 7th anniversary, The Souled Store) are placeholders. To fill one, replace its empty `<div class="media"></div>` with a `<video class="mono" src="media/…mp4" muted loop playsinline preload="metadata"></video>`, remove the `soon` class from the `<article>`, and swap the "Film coming soon" tag for a Watch link.
- **Dance films:** in `index.html`, find `const FILMS`. Each line is one playlist row: title, label, thumbnail, preview clip and the full-film link.

## Moving it to another account

On GitHub, go to repository Settings → General → Danger Zone → **Transfer ownership**. Pages settings move with the repository. If the site was served from a different account's `github.io` address, that address changes to the new owner's.
