# Images folder

Drop image assets here. The site currently references one image; everything else uses inline SVGs (icons, logos, social marks) baked into the HTML.

## What goes here

### Required

**`victorpic.001.jpeg`** — Professional headshot
- Used on: `index.html` (hero, top right) and `about.html` (left column)
- Best aspect ratio: square (1:1). The CSS crops to a square anyway, so anything wider/taller gets centre-cropped.
- Recommended size: at least 1000×1000 px so it stays crisp on retina screens.
- Format: JPEG (smaller file) or PNG. Filename must match exactly.

> You already have this file in your existing repo at
> `https://victormoron.github.io/images/victorpic.001.jpeg`
> — just download it from there and drop it in this folder, or replace it with a fresher photo using the same filename.

### Optional but recommended

**`favicon.png`** — Browser tab icon
- 32×32 px or 48×48 px PNG.
- Could just be your initials on the brand gradient, or a simplified mark.
- If you add this file, also add `<link rel="icon" href="images/favicon.png" />` inside each page's `<head>`.

**`og-image.jpg`** — Social share preview
- 1200×630 px JPEG. Shows when the site is shared on LinkedIn, Twitter, etc.
- Best content: your name + tagline ("AI leadership at the intersection of science, scale, and responsibility") + a clean visual.
- If you add this file, also add the following inside each page's `<head>`:
  ```html
  <meta property="og:title" content="Víctor Morón — Responsible AI Leadership" />
  <meta property="og:description" content="PhD-trained AI and data leader. Building AI that ships and stays trusted." />
  <meta property="og:image" content="https://victormoron.github.io/images/og-image.jpg" />
  <meta property="og:url" content="https://victormoron.github.io" />
  <meta name="twitter:card" content="summary_large_image" />
  ```

## Why this folder was empty when delivered

The site was built as plain HTML + CSS. There's no image generation step, and your existing photos live on your live GitHub Pages repo — not somewhere I can pull from directly. The cleanest path is for you to copy your existing `victorpic.001.jpeg` (or a refreshed version) into this folder before pushing.
