# Dylan's Creek Walk adventures

Static site, migrated from Universe (creekwalk.univer.se) in September 2025.
Plain HTML + one CSS file. No build step. Host anywhere that serves files
(GitHub Pages: Settings -> Pages -> deploy from branch -> main, root).

## Layout

- `index.html` - homepage
- `2022.html` ... `2025.html` - one page per year; URLs stay `/2022` etc. on Pages
- `style.css` - all styling; fonts: Permanent Marker (self-hosted, open license)
  for titles, Optima/Candara system stack for body
- `assets/<year>/` - images as `<name>-750.avif` + `<name>-1500.avif` (srcset pair),
  videos as `<name>-video.mp4` + `<name>-poster.*`
- `assets/manifest.csv` - maps every renamed file back to its original
  Universe/Imgix UUID URL

Each `<img>` carries an inline `aspect-ratio` matching the crop Universe
displayed it at; `object-fit: cover` in the CSS applies the crop.

## TODO: finish 2025

The 2025 page stops at "ready to go" - the walk happened, but the write-up
was never finished. The photos are still on the phone. To finish it: add
`<h2>Title</h2> <p>text</p> <img ...>` blocks to `2025.html`, drop resized
photos into `assets/2025/`, and follow the srcset pattern the other pages use.
