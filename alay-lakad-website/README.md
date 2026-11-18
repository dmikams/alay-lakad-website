# CODEGEEKS / Alay Lakad Foundation frontend

A responsive React + JavaScript + Tailwind CSS + Vite implementation based on the seven screenshots supplied in this chat. No backend or payment integration is included.

## Run locally

Install Node.js 20.19+ or 22.12+ (Node 24 is supported), then open a terminal in this folder:

```sh
npm ci
npm run dev
```

Open the Local URL printed by Vite. To produce and preview the production build:

```sh
npm run build
npm run preview
```

The production files are written to `dist/`. Serve that directory with a static HTTP server; do not open index.html directly from the filesystem. Hash-based navigation supports static hosting without route rewrite configuration. Relative build URLs support deployment under a subdirectory.

## Page checklist

The user's labeled screenshots are the selected version references, superseding ambiguous duplicate Figma frames. The Figma connector could not inspect this file because the connected account lacked editor access.

- [x] ALFI Homepage — supplied screenshot 1
- [x] About Us — Refined — supplied screenshot 2
- [x] Initiatives — Enhanced — supplied screenshot 3
- [x] Services — Kitt Changes — supplied screenshot 4
- [x] Support Us — Enhanced — supplied screenshot 5
- [x] Developers — Enhanced — supplied screenshot 6
- [x] Contact Us — supplied screenshot 7
- [ ] Application — no screenshot supplied. Application links open an explicit pending-design dialog over Services; this is not an implemented Application page.

Routes: `#/`, `#/about`, `#/initiatives`, `#/services`, `#/support`, `#/developers`, `#/contact`. The original eight-page task is not complete until the Application reference is supplied and implemented.

## Functionality

- Shared navigation with active page indication, mobile menu and Escape dismissal.
- Text-size controls and high-contrast toggle (session-local preferences).
- Donation frequency, peso amount, custom amount and payment method selectors; confirmation dialog explicitly collects no payment.
- Contact topic links populate the inquiry form; standard HTML validation checks required fields and email format. Submission gives local demo feedback. No personal data is transmitted or stored.
- Technical support dialog with validation and local demo feedback. Email links open the user's email client and do not send automatically.
- Native modal dialogs provide focus trapping, Escape close and focus restoration. Skip link, visible focus styles, semantic headings and labeled inputs are included.
- FAQ answers remain expanded as shown in the references.

## Project structure

- `src/pages/` — seven separate page components.
- `src/components/` — header/footer, shared UI, shared sections and donation form.
- `src/data/content.js` — navigation, FAQs, application steps and reusable copy.
- `src/styles.css` — Tailwind import, shared design rules and responsive breakpoints.
- `public/assets/` — approved screenshot crops, ready to replace with original assets.
- `ASSETS.md` — crop provenance and replacement notes.

## Design assumptions and limitations

- Desktop screenshot layouts were adapted at 960px and 640px for tablet/mobile; no smaller Figma layouts were provided.
- Body type uses locally bundled Raleway; headings use Georgia. Exact font families and weights could not be inspected in Figma, so these are visual approximations.
- Layouts, colors and spacing are inferred from screenshots, not extracted Figma tokens. Pixel-accurate equivalence is not claimed.
- Photos and logo are cropped from the screenshots with the user's permission. Some contain the original photographic tint, rounded corners or baked-in labels. Replace with original assets for final image quality.
- The Homepage's original full hero photograph is not recoverable behind overlaid text; its gradient remains without that photograph. The Services hero uses the supplied foundation photo as an explicitly temporary substitute. Support uses the matching community photo crop with an overlay. Original hero photographs are still needed.
- Lucide icons approximate the visible line icons because original icon assets were unavailable.
- The GCash QR is an unverified screenshot reference. Recipient details remain awaiting verification, as in the supplied design. The donation controls are a demo and never initiate a payment.
- The unusual trailing word in the Support page's “You can also give your time or resources” heading was preserved exactly from the supplied screenshot. Confirm editorial correction before publishing.
- Services impact statistics and Developers project statistics are reproduced from the supplied designs, not independently verified.
- The About screenshot highlights Services in its header. The implementation corrects active navigation to About so location is represented accurately.
- Contact details and unconfirmed event dates remain pending, matching the supplied copy.
- The support-request form is a minimal frontend interaction because an opened support form state was not supplied.

## Validation

- Production build verified with `npm run build` on Node 24.
- All referenced local image files checked for nonempty content; photo crops visually inspected.
- Desktop, tablet and mobile responsive rules are implemented. Browser visual and interaction testing could not be completed: both local server URLs timed out in the available browser, despite Vite reporting ready. Run locally and compare each page with its reference before treating the implementation as final.

No secrets, credentials, backend calls or remote temporary Figma asset links are included.
