# Junior's Tire Service — demo site

Demo built by Wilson Innovations for **Junior's Tire Service** (Sarasota, FL).
Live at https://wilsoninnovations.net/juniors-tire-service/

- **Wave:** 84 (south territory — Sarasota / Charlotte / Venice / DeSoto)
- **Built:** 2026-08-28
- **Tier:** 1 — Clean Slate
- **Status:** demo / unpitched. `noindex` is in the `<head>` with a removal comment.

## Business facts (all verified, nothing invented)

Source: Google Places API, matched on phone **and** address (place id `ChIJlzVkLaJBw4gRyveeiAHm3Lk`).

| Field | Value |
|---|---|
| GBP name | Junior's Tire Service llc and mobile tire service |
| Phone | (941) 203-8464 — matched GBP, and matched the painted number on their own storefront banner |
| Address | 5356 McIntosh Rd, Sarasota, FL 34233 |
| Rating | 4.8 from 190 Google reviews |
| Hours | Mon–Fri 8:00–5:00, Sat 8:00–3:00, Sun closed |
| Existing website | **None** (confirmed at enrichment and re-confirmed at build — Places returns no `websiteUri`) |

Nothing else is asserted on the page. No email, no license number, no founding year, no
pricing, no service radius for the mobile lane, no owner name.

**Deliberately NOT on the site:** motorcycle tires. A reviewer states the shop does not work on
them, so no moto service is listed anywhere.

## Reviews used

All five Places reviews appear exactly once each, verbatim, attributed first name + last initial,
no dates. The aggregate (4.8 / 190) is shown as plain stat text, never styled as a quote.

- **Ask H.** — the car-wash referral story → featured "Word of mouth" block
- **Marlena** — 10-minute rental-car rescue → reviews grid
- **Bryan B.** — Monday-morning walk-in, under 20 minutes → reviews grid
- **Carlos G.** — the 24x14 fitment nobody else would mount → oversized-wheels block
- **DC H.** (the one 4-star) → "Safety standards" block

The 4-star is not a complaint — it documents the shop's own policy of refusing an inside patch on
a tire more than five years old. It is used on the page as **integrity evidence**: a shop turning
down work on a safety judgment. Only the policy sentence is quoted; the price sentence and the
motorcycle sentence are left off.

## Images

**All photos are the business's own Google Business Profile media**, pulled through the Places API
media endpoint, re-encoded with PIL (each ≤350KB, progressive JPEG), and self-hosted in `img/`.
**Zero stock photography — no Unsplash, so no cross-site image collision is possible.**

| File | Subject | Attribution on GBP |
|---|---|---|
| `hero-whitewall.jpg` / `og-cover.jpg` | red steel wheel + whitewall on a classic pickup | business |
| `inside-patch.jpg` | inside of a tire showing interior patches | business |
| `truck-chrome.jpg` | grey F-150 on large chrome wheels | business |
| `mud-terrain.jpg` | mud-terrain tire on machined wheel, red caliper | business |
| `alloy-allterrain.jpg` | black alloy + all-terrain on a white truck | business |
| `shop-bay.jpg` | mounting/balancing equipment in the bay | customer |
| `jeep-oversize.jpg` | lifted Jeep on oversized mud-terrains | customer |
| `storefront.jpg` | the banner over the door + office hours on the glass | customer |

Every shipped photo was visually inspected before use:

- **Painted-phone check:** the storefront banner reads `(941) 203-8464` — an exact match to the GBP
  number. No mismatch.
- **GPS/watermark check:** no location, GPS or timestamp overlays on any shipped photo.
- **Plates:** no license plates are legible in any shipped photo, so no blurring was required.
- **Foreign-brand screen:** two of the ten available GBP photos were **rejected** because a
  neighboring tenant's sign and a distant car-dealership sign were legible in frame.

Alt text describes only what is actually visible in each frame.

## Build notes

- Fonts: **Offside** (display) + **Jost** (body), both verified live on `fonts.googleapis.com/css2`.
- Palette: flat matte **pit-lane red** `#B01E28` over cool **asphalt grey** `#3A4148 / #2D343B / #20252A`
  on white. Deliberately differentiated from the nearby tire/auto siblings — Junior's red is flat and
  matte with no chrome and no candy gloss, on a cool grey base rather than a warm one.
- Signature motif: a road lane-marking stripe divider and red "pit" rules under each section eyebrow.
- Self-contained single file. Scroll reveals are JS-gated and JS-off safe; all motion is disabled
  under `prefers-reduced-motion`. Verified: 32/32 reveals fire on scroll; page is fully readable
  with JavaScript disabled.
- Reviews grid is 2-column on desktop, 1-column on mobile.
- Base `img` rule includes `height:auto`.
- No contact form. No fixed bottom call bar. Header call CTA is flush right at all widths and goes
  icon-only at ≤900px.
- Verified with puppeteer-core + Edge at true 390px and 1440px: **zero horizontal overflow**, H1 is
  exactly 2 lines at both widths, and the full hero stack sits above the fold at 1440×900 and 1366×768.
- JSON-LD `TireShop` with address, hours and aggregate rating. `og:`/`twitter:` use absolute URLs.

## Call items / pitch openers

1. **The B2B nugget (lead with this).** Detailers at Eager Beaver Carwash spotted a bubbling tire on
   a customer's Land Rover and sent him straight to Junior's — "Juniors is fast and good." Other local
   trades are already routing work to him by word of mouth. Ask how much of his business comes in that
   way, and point out that those referrals currently land on a Google listing with no website behind it.
2. **The sign says something different from the listing.** The banner over the door reads
   "JUNIOR'S TIRE SERVICES" (plural) while the Google listing reads "Junior's Tire Service llc and
   mobile tire service." Worth flagging — inconsistent naming splits searches.
3. **The mobile lane is invisible.** "Mobile tire service" is half the business name and there is
   nowhere online that explains what it covers. The site has a section for it but it is deliberately
   vague, because nothing about coverage area, hours or call-out capability could be verified. Get
   those details on the call and the section can be filled in properly.
4. **Owner name unconfirmed.** "Junior" is not confirmed anywhere — ask who to address.
5. **The 4-star is a selling point, not a problem.** He turns down inside patches on tires over five
   years old. That is on the site as a safety-standards block. Owners usually like seeing a policy
   they thought was costing them stars turned into a trust signal.
6. **Specialty fitment is under-sold.** 24x14s that "nobody would mount," lifted trucks, whitewalls on
   a classic — that is higher-margin work and none of it is visible outside the review text.
7. Re-check website status at the call; it was verified as none on 2026-08-28.

---

Website by Wilson Innovations — https://wilsoninnovations.net
