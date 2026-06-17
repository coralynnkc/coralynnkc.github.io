# Personal website

Static personal site (plain HTML/CSS, no build step). Three pages:

- `index.html` — About
- `reflections.html` — Reflections (coming soon)
- `snippets.html` — Snippets (masonry card layout)

## Local preview

```sh
python3 -m http.server
# then open http://localhost:8000
```

## Deploy (GitHub Pages)

Hosted at https://coralynnkc.github.io from a repo named `coralynnkc.github.io`.

1. Push this directory to the `main` branch of `coralynnkc.github.io`.
2. Repo Settings → Pages → Source: `main` / root.
3. Live within a minute or two.

### Custom domain (optional, later)

Add a `CNAME` file containing the domain (e.g. `coralynnyang.com`) and set it
under Settings → Pages → Custom domain.

## Photo

`assets/photo.jpg` was converted from HEIC and downscaled to 1000px wide.
