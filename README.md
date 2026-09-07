# 證件照排版工具 (ID Photo Layout Tool)

A single-file, client-side web app for cropping a portrait photo to
standard Taiwan ID-photo sizes, optionally removing the background with
an in-browser AI model, and tiling the result onto 4×6" photo paper or A4
for printing.

Everything runs **entirely in the visitor's browser**. No photo, cropped
image, or generated layout is ever uploaded to a server — this project
has no backend.

## Features

- Upload a photo (JPG / PNG / WEBP), drag to reposition, slider to zoom
- Standard sizes: 2" (3.5×4.5cm), 1" (2.8×3.5cm), or a mixed sheet
  (4× 2" + 4× 1")
- Optional AI background removal, running fully client-side, with a
  choice of white or blue-gradient background
- Auto-tiled layout onto 4×6" photo paper or A4, live preview
- Download as a 300 DPI PNG (filename: `ID-photo-<size>-<paper>.png`)

## Privacy

- No server component. No analytics. No image ever leaves the browser.
- Two things are still fetched from external CDNs, which — as an
  unavoidable side effect of any HTTP request — reveal the visitor's IP
  address to those third parties:
  - `@imgly/background-removal` and its AI model files, from jsDelivr /
    IMG.LY's CDN (only if the visitor turns on "AI 去背")
  - The Noto Sans TC web font, from Google Fonts
- If you deploy this publicly, consider mentioning the above in your own
  privacy notice, especially for EU visitors (see `NOTICE.md`).

## Running it

This is a static, single `index.html` file. Open it directly in a
browser, or host it on any static file host / GitHub Pages — no build
step, no server, no npm install required.

## License

This project is licensed under the **GNU Affero General Public License
v3.0 (AGPL-3.0-only)** — see [`LICENSE`](./LICENSE).

This is not the default choice for a small client-side tool; it's
required here because the app dynamically loads and directly drives
`@imgly/background-removal`, which is itself AGPL-3.0-licensed (see
[`NOTICE.md`](./NOTICE.md) for details). To keep the licensing
obligations of that dependency and of this project consistent, the whole
project carries the same license.

**Practical consequence if you deploy this publicly (AGPL §13):**
anyone interacting with your hosted version over a network must be able
to get the exact corresponding source code of what's running. Keeping
this repository public with the deployed code is the baseline
requirement — for full compliance you should also add a visible link
back to this repository somewhere in the running app's UI (e.g. a footer
"原始碼 / Source code" link). That link is **not yet present** in
`index.html` as of this write-up — add one before you publish, or ask
for it to be added.

## Disclaimer

This tool is provided "as is," without warranty of any kind, as stated
in the AGPL-3.0 license text. You are responsible for having the
necessary rights to any photo you process with it, and for complying
with your local regulations regarding ID/passport photo specifications
(sizes and paper layouts here are provided as a convenience and are not
guaranteed to match every issuing authority's current requirements).

## Third-party components

See [`NOTICE.md`](./NOTICE.md) for the full list of third-party
components loaded at runtime and their licenses.
