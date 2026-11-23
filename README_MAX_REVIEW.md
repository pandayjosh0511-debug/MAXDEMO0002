# Reno Decks — Max review version (23 Nov 2026)

## What changed
- Removed fabricated product prices from the demonstration catalogue; all items are now enquiry/quote only.
- Replaced the original invented Premium R Range and generic board labels with real documented **Timmdek product families**: Rockies (Aspen, Cedar, Charcoal, Teak, Walnut), Alps, Andes, Rockies 2D and 3D cladding, Rockies trim, Elitebeam, composite balusters.
- Retained seven original Reno Decks additional items separately as **unverified client extras** (balustrade system, posts, rail, starter clips, fixing clips, finishing kit, accessory pack).
- Created 19 local lightweight image assets, individually labelled **ILLUSTRATIVE / NOT PRODUCT PHOTOGRAPHY**. No Timmdek product photographs have been copied, because rights to reuse could not be verified. These are attractive draft product visuals, not accurate technical drawings.
- Replaced add-to-cart with price-enquiry links for items with unverified pricing.
- Added `IMAGE_MAPPING_REVIEW.csv` so Max can approve each product and supply exact authorised photos, prices and units.

## Before client goes live
1. Ask Timmdek for resale-marketing image permission or request their approved image pack. Replace the local SVG previews with supplied photographs in `public/images/catalogue/`, update `src/data/products.ts` references if filenames change.
2. Get Max to approve exact product combinations, pricing, VAT treatment, units and any special extras. This is a range-level **draft**, not a final inventory.
3. Existing photos on other pages may still be from Unsplash and are illustrative; do not claim they show completed Reno Decks installations.
4. The quotation/contact form still needs a real delivery mechanism before live commercial launch.

## Source catalogue verification
- https://www.timmdek.co.za/products/
- https://www.timmdek.co.za/rockies-decking-range/
- https://www.timmdek.co.za/alps-decking-range/
- https://www.timmdek.co.za/andes-decking-range/
- https://www.timmdek.co.za/rockies-2d-cladding/
- https://www.timmdek.co.za/wood-composite-cladding/
- https://www.timmdek.co.za/elitebeam/
- https://www.timmdek.co.za/downloads/

## Local build
``npm install`` then ``npm run build``. This environment did not have package dependencies installed, so a complete application build has not been verified.

## GitHub upload
Extract ZIP first. Upload the *contents of the project directory* (including `src`, `public`, `package.json`, `index.html`, `package-lock.json`, etc.), not the ZIP as a single file. Use GitHub > Add file > Upload files. Do not upload `node_modules`, `.env`, or credentials. Commit to a new branch or keep a backup before replacing existing work.
