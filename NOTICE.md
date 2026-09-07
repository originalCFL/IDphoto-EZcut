# Third-Party Notices

This project bundles no third-party source code directly, but it loads the
following third-party components **at runtime, from external CDNs**, inside
the visitor's browser. Their own licenses and copyright notices apply and
must stay intact.

---

## 1. @imgly/background-removal

- **What it's used for:** the "AI 去背" (AI background removal) feature.
- **How it's loaded:** dynamically imported at runtime from a CDN
  (`https://cdn.jsdelivr.net/npm/@imgly/background-removal@.../+esm`) — it is
  **not** copied, bundled, minified, or modified by this project in any way.
- **Copyright:** © IMG.LY GmbH.
- **License:** GNU Affero General Public License v3.0 (AGPL-3.0).
- **Upstream source / license text:**
  https://github.com/imgly/background-removal-js
- **Why this matters for you:** the AGPL-3.0 requires that anyone who
  interacts with this application over a network be offered the complete
  corresponding source code of the running application (see AGPL-3.0 §13).
  Because this project's own code directly drives this AGPL-licensed
  library in the same running page, the whole project is distributed under
  AGPL-3.0 as well (see `LICENSE`) — this is the simplest way to keep the
  obligations consistent rather than arguing the two are "separate works."
- **Note:** IMG.LY is known to also offer commercial licensing terms as an
  alternative to AGPL-3.0 for parties who cannot accept AGPL obligations.
  If that applies to you, confirm current terms directly with IMG.LY —
  don't rely on this note, which may be out of date.

## 2. Noto Sans TC (Google Fonts)

- **What it's used for:** the page's Traditional Chinese typeface, loaded
  via `<link>` tags to `fonts.googleapis.com` / `fonts.gstatic.com`.
- **License:** SIL Open Font License 1.1 (permissive; no copyleft
  obligation on your own code).
- **Source:** https://fonts.google.com/noto/specimen/Noto+Sans+TC
- **Privacy note (not a license issue, but worth disclosing):** loading
  fonts directly from Google's CDN sends each visitor's IP address to
  Google as an ordinary side effect of the HTTP request. If you expect EU
  visitors, consider mentioning this in a privacy note, or self-hosting the
  font file instead of loading it from Google's servers.

---

## What is NOT a third-party dependency

- The application UI (HTML/CSS/JS), the linear-gradient "blue background"
  renderer, the layout/tiling logic, and all Canvas drawing code were
  written for this project and are covered by this project's own
  `LICENSE`, not by any third-party terms.
- No icon packs, image assets, stock photos, or other embedded media are
  included.
