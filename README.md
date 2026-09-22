# Tato's Media — site files

Everything needed for the site is in this folder:

- `index.html` — the whole page (nav, hero, work galleries, videos, about, pricing, contact)
- `assets/img/` — logo, concert photos, combat & sport photos, video poster thumbnails
- `assets/video/` — the four reels (`like-a-woman.mp4`, `local-bjj-promotional.mp4`, `omar-episode-1.mp4`, `kudo-1.mp4`)

No build step — it's plain HTML/CSS/JS. Open `index.html` in a browser and it works as-is.

## Putting it on GitHub Pages

1. Create a new repo on GitHub (e.g. `tatos-media`) and push everything in this folder to it, keeping the same file layout (`index.html` at the repo root, `assets/` beside it).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," pick the `main` branch and the `/ (root)` folder, then save.
4. GitHub gives you a URL like `https://<your-username>.github.io/tatos-media/` a minute or two later.

If you want a custom domain (e.g. `tatosmedia.com`), add it under the same Pages settings and point your domain's DNS at GitHub per their instructions — GitHub will prompt you for the exact records once you enter the domain.

## Notes

- The four video files total about 67 MB, each under GitHub's 100 MB per-file limit, so a normal `git push` works — no Git LFS needed.
- The videos are H.264/AAC MP4s re-encoded to fit a good quality-to-size balance for the web; swap in your own files at the same paths if you'd rather use different cuts.
- The photo galleries and video carousel are all plain HTML/CSS/JS — no dependencies beyond the two Google Fonts loaded in the `<head>`.
