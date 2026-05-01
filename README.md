# ReadSlip Launch Website

Static App Store support site for ReadSlip.

## Files

- `index.html` - marketing URL
- `privacy.html` - App Store Privacy Policy URL
- `support.html` - App Store Support URL
- `assets/app-icon.png` - app icon copied from the Xcode asset catalog
- `assets/hero-dashboard.png` - real app screenshot copied from the latest App Store screenshot capture

## Before Deploy

1. Replace `support@readslip.app` in `support.html` with the real support email.
2. Deploy this folder to a static host such as GitHub Pages, Netlify, Vercel, Firebase Hosting, or Cloudflare Pages.
3. Use the deployed URLs in App Store Connect:
   - Marketing URL: `/index.html`
   - Privacy Policy URL: `/privacy.html`
   - Support URL: `/support.html`
