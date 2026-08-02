# St Ambrose — Blessed Edmund Rice & the Eight Essentials

A single-page interactive site built for St Ambrose. The college crest sits at the centre with the Eight Essentials arranged around it. Tap the crest to meet Blessed Edmund Rice; tap any of the eight emblems to see how that essential connects to his life. A small "?" button in the bottom-right corner explains how the site itself was made.

Made by Sebastian.

## What's inside

```
index.html          the page structure and content
styles.css           the navy-and-gold theme, layout, and pop-up styling
script.js             all pop-up text, plus the eight icons themselves, embedded
assets/                the original icon and crest artwork, kept for reference only
```

Every icon is embedded directly inside `script.js` as image data, so the page never depends on loading a separate image file — it displays correctly no matter where or how it's opened.

## Try it locally

No build step or installs needed — it's plain HTML, CSS and JavaScript. Either:

- double-click `index.html` to open it in a browser, or
- serve the folder so the pop-ups and images behave exactly as they will online:
  ```
  python3 -m http.server
  ```
  then visit `http://localhost:8000`.

## Publish it with GitHub Pages

1. Create a new GitHub repository and add these files to it (keep `index.html`, `styles.css`, `script.js` and the `assets` folder all at the same level).
2. Push to the `main` branch.
3. On GitHub, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set the branch to `main` and the folder to `/ (root)`, then **Save**.
6. GitHub publishes the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two — refresh that Pages settings screen to get the exact link.

## Editing the content

- **Text in the pop-ups** — open `script.js` and edit the `content` object near the top. Each entry has a `title` and a `body`.
- **Icons** — each entry in the `content` object in `script.js` has an `icon` field holding the image itself (as embedded data), not a file path. To swap one, base64-encode your replacement image and paste the new string in as that entry's `icon`.
- **Footer credit** — edit the `<footer>` near the bottom of `index.html`.
