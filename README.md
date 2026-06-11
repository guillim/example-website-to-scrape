# The Inkwell & Quill — scraping-practice demo site

A fictional independent bookshop website, built as a target for web-scraping practice. Plain HTML + CSS, zero build step, ready for GitHub Pages.

Everything on the site is made up — the shop, the staff, the books, the emails. There's a disclaimer banner on every page.

## What's here

- `index.html` — home page
- 10 subpages: `about`, `new-arrivals`, `bestsellers`, `fiction`, `non-fiction`, `childrens`, `events`, `staff`, `blog`, `contact`
- `styles.css` — shared stylesheet
- `.nojekyll` — tells GitHub Pages to serve files as-is (skip Jekyll processing)

## The 5 fake emails (scraping targets)

Spread across the Staff, Events, and Contact pages, all on the fictional `inkwellquill.shop` domain:

1. `hello@inkwellquill.shop` — Contact page
2. `rsvp@inkwellquill.shop` — Events page (and referenced on Contact)
3. `m.solberg@inkwellquill.shop` — Staff page (Marit Sølberg)
4. `j.kapoor@inkwellquill.shop` — Staff page (Jaya Kapoor)
5. `t.chen@inkwellquill.shop` — Staff page (Theo Chen)

## Run locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `exampletoscrape`) and push this folder:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/exampletoscrape.git
   git push -u origin main
   ```

2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick **main** / `/ (root)`, and save.
4. Wait ~1 minute. Your site will be live at `https://<your-username>.github.io/exampletoscrape/`.

That's it — no build pipeline, no Jekyll config, no dependencies.
