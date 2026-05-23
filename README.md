# Portfolio Demos

Anonymized case-study demos linked from the Notion portfolio.

## Files

- `index.html` — master navigation page (open this first)
- `case_a*.html` — anonymized notebook exports, SQL/Python source views, interactive dashboards
- `case_a*.pdf` — anonymized PDF exports (decks, written sections)

## Host on GitHub Pages (one-time setup)

```bash
# 1. Create a new public repo for the demos (recommended: portfolio-demos)
gh repo create portfolio-demos --public --confirm
cd portfolio-demos
git init

# 2. Copy the demos into the repo
cp -R /Users/ahmetcolak/GitHub/PORTFOLIO/portfolio_demos/* .
git add .
git commit -m "initial demos"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/portfolio-demos.git
git push -u origin main

# 3. Enable Pages: GitHub → repo → Settings → Pages → Branch: main / root → Save
```

Live URL pattern: `https://<YOUR_USERNAME>.github.io/portfolio-demos/`

## Local preview

```bash
cd portfolio_demos
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Re-generate after source changes

The HTMLs are produced via Jupyter `nbconvert` with a sanitization pass. If you update the source notebooks, regenerate from this folder — the masking rules are documented in the generation script.
