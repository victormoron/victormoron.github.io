# victormoron.github.io

Personal website for Víctor Morón — AI leadership at the intersection of science, scale, and responsibility.

## Project structure

```
victormoron-site/
├── index.html          # Home (hero, stats, pillars, work preview, insights preview, CTA)
├── about.html          # Story, credentials, what I'm open to
├── work.html           # Case studies (Responsible AI, digital twin, fusion platform, etc.)
├── insights.html       # Medium articles + Advisory & Board
├── contact.html        # Contact form + engagement types
├── styles.css          # Shared stylesheet
├── images/             # Drop image assets here (see below)
├── .nojekyll           # Tells GitHub Pages to skip Jekyll processing
└── README.md           # You are here
```

All pages share a single `styles.css` and load Inter + JetBrains Mono from Google Fonts. No build step, no dependencies — just static files.

## Deploying to GitHub Pages (your existing setup)

You already host at `victormoron.github.io`, so the repo is the username repo. To replace the current site with this one:

### Option A — via GitHub web UI (easiest)

1. Go to https://github.com/victormoron/victormoron.github.io
2. Delete the old files (or move them to an `archive/` folder if you want a backup)
3. Click **Add file → Upload files** and drag everything from `victormoron-site/` (including the `images/` folder)
4. Commit directly to `main`
5. Wait ~30 seconds; the site updates at https://victormoron.github.io

### Option B — via git CLI (if you prefer)

```bash
# Clone the existing repo
git clone https://github.com/victormoron/victormoron.github.io.git
cd victormoron.github.io

# Optional: keep a backup of the old site
git checkout -b archive/old-site
git push origin archive/old-site
git checkout main

# Replace contents with the new site
# (delete old files, copy new ones from victormoron-site/)
git add .
git commit -m "Redesign: modern multi-page site with case studies"
git push origin main
```

GitHub Pages will pick up the change and republish within a minute.

### Optional: custom domain

If you decide to reactivate `victormoron.info`:

1. Add a file named `CNAME` at the root of the repo, containing just:
   ```
   victormoron.info
   ```
2. In your DNS, add an `A` record (or `ALIAS`/`ANAME`) pointing the apex domain to GitHub Pages IPs (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153).
3. In the repo's **Settings → Pages**, set the custom domain to `victormoron.info` and enable "Enforce HTTPS".

## Images

The site references the following images. Drop them in the `images/` folder with these exact filenames:

| Filename                  | Used on                | Notes                                                                  |
|---------------------------|------------------------|------------------------------------------------------------------------|
| `victorpic.001.jpeg`      | Home hero, About page  | Professional headshot. Square aspect works best (1000×1000 or larger). |
| `favicon.png` *(optional)*| Browser tab            | 32×32 or 48×48 PNG. If added, the HTML can reference it.               |
| `og-image.jpg` *(optional)*| Social share previews | 1200×630, used when the site is shared on LinkedIn/Twitter.            |

You can reuse `victorpic.001.jpeg` from your existing repo at `victormoron.github.io/images/` — it already lives there.

## Contact form

The contact form on `contact.html` posts to **FormSubmit** (https://formsubmit.co) — a free, no-backend email forwarding service. It's pointed at `vmorontejero@gmail.com`.

The **first time** anyone submits the form, FormSubmit will email you a confirmation link to activate the endpoint. Click it once, and from then on every submission will arrive in your inbox.

If you'd rather use a different service (Formspree, Netlify Forms, your own backend), just change the `action="..."` attribute on the `<form>` element in `contact.html`.

## Local preview

Open any of the HTML files directly in a browser (`file://...`) — they'll work as-is. For a closer match to production:

```bash
# From inside the victormoron-site/ folder:
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## Future tweaks

Likely next steps:
- Refresh / replace the headshot
- Adjust copy on the Work case studies (especially anonymisation level)
- Add new Insights posts as they're published
- Add a Speaking section if engagements start coming in
- Add a favicon and Open Graph image for nicer social shares
