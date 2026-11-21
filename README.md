# BenchBook website

A one-page showcase for BenchBook. Plain HTML and CSS: no framework, no build step and no external requests.

```
index.html      the page
styles.css      layout, colours (from the app icon), light and dark mode
assets/         app icon, favicon, screens/ (app screenshots) and videos/ (tutorial thumbnails)
```

## Preview

Open `index.html` in a browser. Or serve the folder, so links behave as they will online:

```sh
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Before publishing

- **Screenshots** in `assets/screens/` are captures of BenchBook's own windows (`screencapture -l <window id> -o`), so the corners stay transparent and the page adds the shadow. Some photos in them carry third-party watermarks (JetPhotos); replace those shots if anyone objects. Retake a shot by capturing the same window at a similar size and overwriting the file.
- **Placeholders.** The Kits and Custom mixes sections show `kits-placeholder.svg` and `mixes-placeholder.svg`. Capture the Kits window and an Edit Mix sheet as above, save them as PNGs in `assets/screens/`, and change each `<img>`'s `src`, `width`, `height` and `alt` to match.
- **Tutorials** link to YouTube instead of embedding players, so the page loads nothing from YouTube. Each card's thumbnail is a 640×360 copy of the video's YouTube thumbnail, saved in `assets/videos/`. To add a video, copy a card in the Tutorials section and add its thumbnail.
- **Download link.** Buttons point to `github.com/jvanlint/BenchBook/releases/latest`, which always serves the newest release.
- **Wording.** Check the footer credit and the "Free" and "Signed and notarised by Apple" claims still hold.

## Publishing

This folder is its own git repository, kept out of the app's repository by `/website/` in the app's `.gitignore`. GitHub Pages can serve it straight from the repository's `main` branch: Settings › Pages › Deploy from a branch › `main` / root.
