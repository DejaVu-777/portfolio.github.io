# A Jagannath — Portfolio

A single-page, static portfolio. No build step, no dependencies, no framework.
Everything is plain HTML + CSS, with one small vanilla JS file inline (scroll reveal + active nav).

## What's in here

```
index.html          the whole site
assets/photo.jpg    hero portrait
assets/resume.pdf   linked from the "Résumé" buttons
```

## Deploy to Vercel (2 minutes, free)

**Option A — drag and drop**
1. Unzip this folder.
2. Go to https://vercel.com/new and choose the **Deploy** tab (or "Deploy from template" → drag).
3. Drag the whole `portfolio` folder onto the page.
4. Vercel gives you a URL like `portfolio-xyz.vercel.app`. Done.

**Option B — with Git (recommended if you'll keep editing)**
```bash
git init
git add .
git commit -m "portfolio"
# create an empty repo on GitHub, then:
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```
Then on Vercel: **Add New → Project → Import** the repo.
Framework preset: **Other**. Build command: *(leave empty)*. Output directory: *(leave empty)*.

**Custom domain:** Vercel → Project → Settings → Domains → add yours.

## Things to edit before you publish

Search `index.html` for these and replace:

| Find | Replace with |
| --- | --- |
| `href="#" aria-label="GitHub"` | your GitHub URL |
| `href="#" aria-label="LinkedIn"` | your LinkedIn URL |
| `jagannath.datascience@zohomail.in` (2 places) | your preferred email |
| `assets/photo.jpg` | any new portrait, keep it portrait-shaped (4:5 works best) |

Text lives in plain paragraphs — open `index.html` in any editor, edit, save, refresh.

## Notes

- **Responsive:** two-column hero on desktop, stacked on mobile. Nav links scroll horizontally on
  small screens instead of hiding behind a menu button.
- **Accessibility:** keyboard-skippable, visible focus, alt text on the portrait, honours
  `prefers-reduced-motion` (animation off), decent contrast.
- **Fonts** load from Google Fonts. To go fully offline, download Space Grotesk, IBM Plex Mono and
  Instrument Serif and swap the `<link>` for local `@font-face` rules.
- **Colours** are CSS variables at the top of the `<style>` block — change `--rust` or `--teal` to
  re-tint the whole site.
- Works without JavaScript too: content is all in the HTML, the reveal animation just doesn't run.
