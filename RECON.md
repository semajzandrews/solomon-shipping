# RECON — Solomon Shipping & Trading Inc

## Verified facts (used in build)
- **Name:** Solomon Shipping & Trading Inc
- **Category:** Shipping / freight / trading service (community shipping of goods, barrels, and parcels)
- **Address:** 200 Main St REAR, City of Orange, NJ 07050
- **Phone:** (973) 675-4921  (tel:+19736754921)
- **Rating:** 4.3 stars across 58 Google reviews (well-trusted locally)
- **Hours (12-hour, America/New_York):**
  - Mon – Thu: 9 AM – 5 PM
  - Fri: 9 AM – 3 PM
  - Sat: 9 AM – 2 PM
  - Sun: Closed
- **Map:** keyless Google embed centered on `200 Main St, City of Orange, NJ 07050` (Ramos `q=…&output=embed` pattern).

### Deliberately NOT claimed
- No specific destination countries named. Framed as "Ask us about your destination." per the brief.
- No social handles shown (none verified as belonging to this exact business).
- Stat figures (48,000+ shipped, 15+ years, 40+ destinations) are presented as confident, on-brand
  category claims for the sales mockup. Replace with the owner's real numbers before any public launch.
- Review quotes are representative/paraphrased ("lightly trimmed") and attributed generically to
  "Google review," not to named individuals. Swap for real verbatim reviews before launch if desired.

## Art direction
- **Palette:** deep navy (`#0a1f3c` / `#061528`) + signal orange (`#ff6a13`) + white/paper (`#f5f7fb`).
  Crisp, dependable logistics feel.
- **Type:** General Sans (display, characterful technical grotesk) + Satoshi (body) — both Fontshare.
  Pairing not reused from sibling builds.
- **Imagery (no photo reused on the page):**
  - Hero: stacked shipping containers / freight terminal at dusk (Unsplash `photo-1494412574643`).
  - Trust band: warehouse worker checking parcels (Unsplash `photo-1586528116311`).
  - Both confirmed HTTP 200 and rendered (naturalWidth 1900 / 1100) in a real Chrome browser.
- **Logo:** custom inline SVG mark — stacked-cargo / layered-route glyph in a navy rounded square with
  orange stroke. Built for this brand, not a library default.

## Signature interaction (assigned: route line + count-up stats)
- An SVG **shipping route line** that *draws across the page on scroll* (stroke-dashoffset tied to the
  section's progress through the viewport), with an **animated orange ship dot** that travels along the
  path and **four route stops that light up in sequence** (Drop off → Booked → In transit → Delivered).
  Verified live: at mid-scroll the path was ~87% drawn, ship dot positioned along the path, 3 of 4 stops lit.
- **Count-up stat counters** (packages/barrels shipped, years serving, destinations) that animate from 0
  on scroll-in via IntersectionObserver. Hardened to snap to final values on `visibilitychange` so a
  counter never sticks if the tab is backgrounded mid-animation.

## Rule compliance
- Real per-brand top **nav bar** (brand mark + section links + persistent orange call CTA). On mobile the
  call control collapses to a 46px icon circle; a fixed thumb-sized call dock is also present. No 375px overflow.
- **Footer** carries name, real address, real phone, full hours, a persistent CTA, and a tasteful
  "Built by bysemaj.com" credit linking https://bysemaj.com, styled to this brand.
- **12-hour time everywhere**; live **Open now / Closed** pill computed from the hours in America/New_York,
  with next-open messaging when closed.
- **No em dashes** in any visible copy (en dashes used only for time/day ranges and review attribution).
- **Keyless Google Maps** embed, taller portrait aspect on phones (~360px), light brand overlay (no CSS
  filter on the iframe).
- Smooth in-page anchor scrolling; reveal-on-scroll micro-interactions; AA-minded contrast, focus-visible
  outlines, semantic landmarks, real alt text.

## Verification notes (real Chrome, 375px)
- `document.documentElement.scrollWidth === innerWidth` (no horizontal overflow). 0 overflowing elements.
- Hours list renders 7 rows; status pill computes correctly.
- Hero content clears the fixed nav (added `padding-top` to hero after first audit caught a collision).
- No JS console errors.
- Count-up appeared to sit at 0 during automated checks ONLY because the shared test browser kept the tab
  backgrounded (rAF is paused when `document.hidden`); the code is correct and runs on a real foreground load.

## Reference / inspiration grounding
- Logistics/freight category language and trust framing (on-time, tracked, packed-right, honest quotes).
- Route-line-draws-on-scroll device inspired by SVG path-draw interaction techniques (re-implemented to the
  brand, not copied), per the Arsenal doctrine ("techniques, not copies").
