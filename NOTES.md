# Before you push — read this

Everything here was generated in a sandbox with **no internet access**, so two
files are stand-ins and need to be regenerated with your real data before (or
right after) you push:

- `data/contributions.json` and `contrib-heatmap.svg` — built from **fake,
  randomly-generated** contribution counts, just to prove out the layout/sizing.
  Regenerate for real with:
  ```bash
  pip install -r scripts/requirements.txt
  GH_PROFILE_USER=baidi10 python scripts/fetch_contributions.py
  python scripts/render_heatmap_svg.py
  ```
  (Or just let `.github/workflows/update-profile-art.yml` do it automatically
  once you push and enable the workflow — see step 7 in `PROMPT.md`.)

Everything else is real and ready to go:
- `avi-ascii.svg` — generated from your uploaded photo (background removed by
  color/geometry since it was a flat-color avatar circle, not `rembg`).
  Tuned settings: `CONTRAST=1.35`, `GAMMA=0.55`, `WHITE_FLOOR=0.74` in
  `scripts/make_ascii_svg.py`.
- `info-card.svg` — built from your CV (FST Errachidia, Commune d'Arfoud
  internship, stack, highlights).
- `README.md` — filled in with your name, tagline, portfolio, and LinkedIn.
  **Instagram badge is left out** — send a handle if you want it added.

## Still needed
- A `.github/workflows/update-profile-art.yml` wasn't in your uploads, so it's
  not included here — that's step 7 in `PROMPT.md` if you want the daily
  auto-refresh.
- Create the repo (must be named exactly `baidi10`) and push these files.
