# Reno Decks — code handoff and outstanding production blockers

This is the original React 18 / Vite 7 / TypeScript / Tailwind application supplied as `maxdemov002-main.zip`, with a first-pass set of focused corrections.

## Changes in this ZIP
- Corrected shop category filtering when navigation changes or removes `?category=`.
- Corrected repetitive homepage headings.
- Improved product-card price typography and made Quick View accessible on touch screens.
- Clarified that contact-form submission is a **demo validation only** and does **not send enquiries**.
- Removed the broken default Vite favicon and irrelevant Bolt social preview image.
- Added a proper not-found page instead of silently showing the homepage for missing routes.

## Critical client launch blockers (must resolve first)
1. **Catalogue**: 23 hard-coded sample products, prices and Unsplash stock photos in `src/data/products.ts`. These are NOT verified prices, specifications or supplier photos. Replace with a client-approved product spreadsheet and properly licensed matching images before going live.
2. **Enquiries**: `src/pages/ContactPage.tsx` validates fields but DOES NOT send them. Contact details are placeholders. Supply a verified receiving email and integrate an email/form backend; implement error/success handling and test real delivery.
3. **Checkout**: cart state is stored in localStorage, not a payment or fulfilment backend. Never describe the shop as fully transacting until ordering/payment is actually integrated and tested.
4. **Portfolio**: existing project images and descriptions are illustrative concepts, not verified past client projects.
5. **AI assistant**: no bot has been integrated or configured. Need provider account and embed ID plus verified knowledge base; only then add a live assistant.
6. **Domain and deployment**: verify DNS ownership, preserve business email MX/SPF/DKIM records, and deploy to hosting suitable for client commercial use.
7. **Imagery rights**: obtain permission for Timmdek product photos or use client-provided/licensed supplier assets. Unsplash images currently hotlink to external sources; treat as inspiration until approved.

## Commands
```bash
npm ci
npm run typecheck
npm run lint
npm run build
npm run dev
```

Cloudflare Pages for a static Vite deployment: build command `npm run build`, output `dist`; validate routes and all functions after deployment.

## Verification limits
Dependency installation was blocked in the assistant environment because the offline npm cache lacked packages; therefore this package was not compiled or browser-tested here. It needs `npm ci` and build/test on a machine with npm registry access.
