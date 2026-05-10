# CLRLC-LLMs Workshop Proposal · NeurIPS 2026

Source code for the workshop proposal website, organised by the **Center for Low-Resource Languages and Cultures (CLRLC)**.

---

## 📁 Folder Structure

```
.
├── index.html              ← The page itself. Edit text content here.
├── style.css               ← Colours, fonts, layout. Edit here for styling.
├── README.md               ← This file.
└── images/
    ├── neurips-logo.png    ← NeurIPS logo for the hero (optional)
    ├── clrlc-logo.png      ← CLRLC logo for the hero (optional)
    ├── hero-bg.jpg         ← Optional background photo for the hero
    ├── speakers/
    │   ├── speaker-1.jpg   ← Speaker photos (square, ~600x600px works well)
    │   ├── speaker-2.jpg
    │   ├── speaker-3.jpg
    │   └── speaker-4.jpg
    ├── organizers/
    │   ├── joy.jpg         ← Organizer photos (square)
    │   ├── mary.jpg
    │   ├── cynthia.jpg
    │   ├── yann.jpg
    │   ├── sharon.jpg
    │   ├── flora.jpg
    │   └── oluchi.jpg
    └── sponsors/
        ├── platinum-1.png  ← Sponsor logos (transparent PNG works best)
        ├── platinum-2.png
        ├── gold-1.png
        ├── gold-2.png
        └── ...
```

---

## 🖼️ Where Each Picture Goes

Every image slot in `index.html` is labelled with a comment like:

```html
<!-- IMAGE SLOT: NeurIPS logo · path: images/neurips-logo.png -->
```

Just save your picture at the path shown, with the exact filename. The page will pick it up automatically. **If an image is missing, a clean placeholder is shown instead** — so the site never looks broken while you're still gathering pictures.

### Photo tips
| Image | Format | Recommended size |
|---|---|---|
| Speaker / organizer photos | JPG or PNG | Square, 600×600 px |
| NeurIPS / CLRLC logos | PNG with transparency | ~120 px tall |
| Sponsor logos | PNG with transparency | ~200 px tall |
| Hero background (optional) | JPG | 1920×1080 px or larger |

### To use a hero background photo
1. Save your photo as `images/hero-bg.jpg`.
2. In `index.html`, change `<header class="hero" id="home">` to `<header class="hero with-bg" id="home">`.

---

## ✏️ How to Edit Content

| What you want to change | Where to do it |
|---|---|
| Workshop title, dates, venue | `index.html` — the **Hero** section near the top |
| Overview text | `index.html` — the `<section id="overview">` block |
| Speaker names & affiliations | `index.html` — `<section id="speakers">` |
| Agenda times and sessions | `index.html` — `<table class="agenda-table">` |
| Lightning Talk topics, deadlines | `index.html` — `<section id="cfp">` |
| Organizer names & affiliations | `index.html` — `<section id="organizers">` |
| Sponsor logos | `images/sponsors/` + `<section id="sponsors">` |
| Contact emails | `index.html` — `<section id="contact">` |
| Colour palette | `style.css` — the `:root { ... }` block at the top |
| Fonts | `style.css` — change `--font-serif` and `--font-sans` in `:root` |

To **add a new speaker or organizer**, copy a `<article class="person">` block in `index.html` and update the image path and name.

To **remove someone**, just delete that block.

---

## 🚀 Deploy on GitHub Pages

1. **Create a new repository** on GitHub (e.g. `clrlc-llms-neurips-2026`).
2. Upload all the files in this folder (you can drag-and-drop in the GitHub web UI).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set:
   - Source: **Deploy from a branch**
   - Branch: **main** · **/ (root)**
5. Click **Save**. Within a minute, your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

To add or update pictures later, just upload the file to the right folder in the repo — GitHub Pages will redeploy automatically.

---

## 🎨 Quick Customisation

All colours are in CSS variables at the top of `style.css`:

```css
:root {
  --accent:      #8a3324;   /* primary accent — currently deep terracotta */
  --accent-soft: #c5704f;   /* lighter accent */
  --gold:        #b8893d;   /* warm gold */
  --paper:       #faf8f3;   /* page background */
  --ink:         #1a1f2e;   /* main text colour */
  /* ... */
}
```

Change those values and the whole site re-themes.

---

## 📬 Contact

Workshop email: **centerlowresourcellms@gmail.com**
Website: [www.clrlc.org](https://www.clrlc.org/)

© 2026 CLRLC-LLMs Workshop · Organised by the Center for Low-Resource Languages and Cultures (CLRLC)
