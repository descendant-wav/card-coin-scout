# Card & Coin Scout V2 — Android-ready PWA

This is the V2 build designed around an Android phone camera.

## V2 features

- Front + back / obverse + reverse capture
- Card centering/corner/edge/surface observations
- Coin variety/error screening
- Raw low / typical / high estimate
- "Worth grading?" recommendation
- HOT / CHECK / LOW triage
- Verification checklist for suspicious items
- One-tap eBay SOLD/COMPLETED search
- Local collection and running typical-value total
- Installable as a home-screen PWA

## Get it onto the phone

This folder must be served from HTTPS for the cleanest camera/PWA behavior.

### Easiest route: GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html`, `manifest.json`, and `service-worker.js`.
3. Enable GitHub Pages for the repository.
4. Open the resulting HTTPS URL in Chrome on Android.
5. Use Chrome's install/add-to-home-screen option.

Chrome's current web platform supports installable web apps/PWAs, and the app manifest supplies the app name and launch behavior. See Chrome's developer documentation for manifest requirements. 

### API key

The prototype stores your OpenAI API key in browser local storage. This is acceptable for a private personal prototype but is NOT how a public app should be deployed. V3 should put the API key behind a small backend.

## Pricing

The AI provides a conservative estimate, then the app links directly to eBay SOLD/COMPLETED results. The latter is the market sanity check. Active asking prices are not treated as completed-sale prices.

## V3 roadmap

- Secure backend so the API key is never on the phone
- Better sold-comps aggregation
- Dedicated card database matching
- Dedicated coin variety references
- Barcode scanning
- Automatic perspective correction
- Batch mode: scan -> save -> immediately scan next
- CSV export
- Collection search/filter
- Optional cloud sync
- Native Android APK after the workflow is proven
