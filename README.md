# ReadSlip support website

Static Thai-first website with English summaries for the free ReadSlip iPhone redesign. No build step, external fonts, JavaScript, analytics or third-party page assets are required by the website.

## Current content

- `index.html`: Photos-first workflow, free scanning/summaries/XLSX/PDF exports, current native screenshots and payment-verification limits.
- `support.html`: setup, Photos permissions, review and bulk classification, summaries, export, earlier records and Apple subscription help.
- `privacy.html`: local OCR/QR and storage, iCloud retrieval, Firebase Analytics, earlier team sync and legacy Apple purchases.
- `style.css`: responsive layout matching the app's warm background and green palette, visible keyboard focus and skip links.
- `assets/app-icon.png`: current Pip app icon copied unchanged from the app source.
- `assets/screenshots/`: actual native synthetic captures with [source provenance and viewport limits](assets/screenshots/README.md).

The source of truth for this update is [ReadSlip commit 83e836f35161ba01ee94cc795d4b7553fb727718](https://github.com/pond1982/ReadSlip/commit/83e836f35161ba01ee94cc795d4b7553fb727718), tested development build **1.2 (9)**. The screenshots do not establish public App Store availability. The old shop dashboard image has been removed. No customer transaction images or personal records are used.

Keep the development-preview notices until the App Store release is verified. A separate App Store submission does not itself establish publication. Free local features do not cancel existing Apple subscriptions; preserve the separate management guidance unless billing changes are verified.

## Preview and verification

From this directory, run:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Open `http://127.0.0.1:8765/`. The HTML uses relative paths so it also works under the GitHub Pages project path.

For updates, check all pages at desktop and narrow mobile widths, keyboard focus and skip links, every local link/fragment, image loading, and contrast. Compare screenshots against the actual app source rather than assuming older captures are current. Check `git diff --check` before committing.

## Existing hosting

GitHub Pages is already configured to publish **`main` / repository root** at:

https://pond1982.github.io/ReadSlipWebsite/

Pushing to `main` triggers the existing `pages-build-deployment` workflow automatically. Do not create another branch, change hosting settings, or manually deploy as part of a normal content update. The existing App Store support paths remain `index.html`, `support.html`, and `privacy.html`. Support/privacy contact: `pondd.dev@gmail.com`.

## Validation for the November 4 update

- Browser checks on all three pages at 1440 × 1000 and 320 × 844, plus home/gallery and privacy at 390 × 844: no horizontal overflow or failed images. Screenshot links open the full, uncropped captures.
- Keyboard skip link becomes visible and transfers focus to the main content. HTML landmarks, unique IDs, image descriptions and all 37 local references/fragments checked.
- Main text, muted text, buttons and link colors meet a 4.5:1 contrast ratio on their backgrounds (checked pairs range 5.48:1–11.34:1).
- Every page, stylesheet, icon and screenshot served successfully over local HTTP and matched its working file. All four screenshot files match the app's native capture bytes exactly.
- `git diff --check` passed. No application, hosting, account or billing settings changed. The separately requested App Store graphics are outside this repository update; no website search feature is included.
