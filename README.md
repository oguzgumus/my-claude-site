# Classical Photography Portfolio

An editorial, book-inspired photography portfolio site with per-genre galleries and bilingual (English / Turkish) support. Built as self-contained HTML — no build step, no dependencies to install.

## Pages

| File | Description |
|------|-------------|
| `index.html` | Homepage — nav, hero, six-genre collections, Services & Pricing, About, testimonials, Instagram feed, and contact form. |
| `gallery.html` | Reusable per-genre gallery template. Which genre it shows is driven by the `?g=` URL parameter (e.g. `gallery.html?g=weddings`). Includes a masonry grid, genre switcher, click-to-open lightbox, and booking CTA. |

## Supporting files

| File | Description |
|------|-------------|
| `image-slot.js` | Drag-and-drop image placeholder component used for every photo area (hero, galleries, Instagram feed). |
| `support.js` | Shared runtime utilities required by both pages. |
| `styles.css` | Classical design-system stylesheet (typography, colors, spacing). |

Both `.js` files must sit alongside the HTML files — the pages reference them by relative path.

## Features

- **Editorial "Classical" styling** — matted photo plates, hairline rules, Cormorant + Lora typography, and gold accents throughout.
- **Bilingual EN / TR** — a language toggle swaps all chrome, headings, and blurbs via a translation dictionary. The choice persists across page loads.
- **Per-genre galleries** — one gallery template serves all six genres via the `?g=` parameter.
- **Lightbox** — click any photo to view it full-screen; reads the actual dropped image.
- **Drag-and-drop photos** — drop images directly into any slot; drops persist across reloads.

## Running locally

Because the pages load `image-slot.js` and `support.js` over HTTP, serve the folder rather than opening the file directly:

```bash
# from inside this folder
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

## Customizing

- **Pricing** — edit the four service tiers in `index.html` (currently placeholder rates).
- **Photos** — drop your images into the slots on the homepage and gallery pages.
- **Genres** — the gallery genres and their labels are defined in `gallery.html`.
- **Translations** — EN/TR strings live in the translation dictionaries inside each page.
