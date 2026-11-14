# Website Kit Recipe v2 — "Gorilla × Savage"

**What this is:** a single paste-ready master prompt that spins up a complete, good-looking
service-business / agency website by default — design system, conversion structure, copy
slots, and QA bar all baked in. Fill in the `{{parameters}}`, paste, and the builder produces
the whole site in one pass instead of improvising layout, color, and funnel order every time.

**When to use it:** any new single-page (or small multi-page) site for a local service
business (trades, automotive, repair, clinics, studios) or a small agency — the kind of site
Jon builds in the **Website-Templates** project. For Divi/WordPress production builds, pair
it with the pack's Divi locks (`website-templates-pack-gaps-2026-10-12/RULES.md` — native
Divi 5 modules only, clone-and-mutate, never builder JSON from scratch).

**What's new vs the prior recipes (v1):**
- **v1 was taste rules + a handoff format.** The pack already had Jon's locked taste
  (`design-skills/jon-taste-SKILL.md`: charcoal/red/gold, hairline borders, 2–3 signature
  moments, ship bar) and Manzari's design→code handoff prompt shape. v1 never specified a
  *complete buildable design system* or a *conversion structure* — every build still
  improvised both.
- **v2 adds the Gorilla Tek design system** (round 23): a proven, fully-specified visual
  machine — three-token color, two-font discipline, the skew geometry, band rhythm,
  one-sheet imagery — with Jon's red/gold adaptation worked out token-for-token.
- **v2 adds the Savage conversion IA** (round 23): the section order, radical price/terms
  transparency block, free-review funnel, and anti-agency copy formula from an agency that
  closes clients before the first sales call.
- **v2 adds a signature-moment menu** from the motion harvests: FeralUI physics
  micro-interactions (round 22), the gaze form mascot (FeralUI Blob / page-mascot, round
  22), and the islandcn live status pill (round 23) — pick 2–3 per build, per Jon's lock
  that consistency is the floor, not the ceiling.
- **v2 adds the Pricing Pages anatomy** (round 6 design deck) for the pricing section:
  one highlighted tier, switch with a numeric saving, table under cards, billing-fear FAQs,
  proof adjacent.

Sources: `2026-11-13-raindrop-round23.md` (Gorilla Tek, Savage, islandcn),
`2026-11-13-raindrop-round22.md` (FeralUI, page-mascot), `2026-10-18-raindrop-round6-next-eight.md`
(Pricing Pages), pack `RULES.md` + `jon-taste-SKILL.md`, `~/MEMORY.md` design locks.

---

## The master prompt

```
Paste into Cursor — Website-Templates project:

Build a complete single-page website for a local service business using the design system
and conversion structure specified below. Do NOT improvise a different layout system,
palette, or section order — this spec IS the design. Your job is fidelity to the system,
parameterized with the business details given.

## PARAMETERS (defaults are the house brand — override only where a value is given)
- BUSINESS_NAME: {{business name}}
- TRADE: {{trade, e.g. motorcycle & automotive service}}
- CITY / SERVICE_AREA: {{city, state}}
- PHONE: {{phone, display format}} (tel: link uses digits only)
- ADDRESS: {{street address or "service area only"}}
- HOURS: {{hours, e.g. Mon–Fri 8–6 · Sat by appointment}}
- SERVICES: {{4–6 services, each: name + one-line description + 2–3 bullet details}}
- STATS: {{4 stats, e.g. years in business / jobs done / rating / response time}}
- OWNER: {{owner first+last name + one-line creed}}
- TESTIMONIALS: {{1–3 real testimonials with names — NEVER invent testimonials;
  if none are supplied, omit the section rather than faking one}}
- PRICE_ANCHOR: {{starting price + what it covers, e.g. "Full builds start at $X"}}
- PRICE_INCLUDES / PRICE_EXCLUDES: {{explicit lists}}
- TIMELINES: {{3 tiers keyed to job type}}
- FREE_REVIEW_OFFER: {{the no-cost entry offer, e.g. "Free 21-point inspection"}}
- COLORS (default house brand — Jon's lock: dark charcoal + grays, red/gold accents;
  NEVER teal, aqua, or purple):
  --charcoal: #17181a (drifts to #222326 across gradients)
  --paper:    #f2efe9
  --gold:     #c9a227  (the signal accent — every accent slot below)
  --red:      #b3202a  (used EXACTLY twice: the closing banner + one hover)
- FONTS: display = Montserrat (900 italic for headlines, regular weights for body —
  same family), instrument = Barlow (800, reserved for numbers / phone / buttons /
  eyebrows). Never a third family. Name fonts by their real names; load via Google Fonts
  with display=swap.

## DESIGN SYSTEM (Gorilla Tek machine, red/gold adaptation)
1. LAYOUT: one column, width min(89%, 1320px). Sections are full-bleed BANDS alternating
   dark → light → dark. Rhythm comes from band contrast, NOT from floating cards.
   Dark bands are never flat: linear gradient 100–110° or radial-at-right, drifting
   ~8–10 lightness points. Light-band section intros: heading left / paragraph right,
   1px gold left border on the paragraph.
2. TYPE: H1 clamp(36px, 6vw, 62px), line-height 1.05, letter-spacing −1.7px, UPPERCASE,
   Montserrat 900 italic. The headline's second line is set in gold via <em>.
   Eyebrows: 12px Barlow 800 italic, letter-spacing 2px, gold, preceded by a 90×1px
   gold rule. Body text minimum 15px (the original's 11–13px body is a known flaw —
   do not repeat it). Stat numerals: Barlow 800, 20px minimum.
3. SKEW SYSTEM (the brand gesture — geometry, not hue):
   - Buttons: gold background, near-black text, Barlow 800 13px uppercase, padding
     12px 27px, transform: skew(-14deg). Hover = filter: brightness(1.15) ONLY.
     Icons sit INSIDE the skew — never counter-skew button contents.
   - Closing CTA banner: full-width red parallelogram —
     position:relative; top:-30px; margin-bottom:-30px; background:var(--red);
     transform:skew(-26deg); box-shadow:0 1px 0 rgba(255,255,255,.55) inset.
     Children counter-skewed skew(26deg). Contents: H2 + one-line sub, the PHONE NUMBER
     itself as the CTA copy (Barlow 800, 24px, white), one charcoal button with gold text.
4. CARDS/SURFACES (Jon's lock): NO flat single-color top strokes or bands on cards.
   Hairline warm border (1px, rgba gold ~18%) + soft layered shadow. The accent lives in
   a small editorial detail — a short gold rule under the title, a red index numeral —
   never a colored slab.
5. IMAGERY — ONE-SHEET RULE: all photography comes from ONE tall reference sheet
   (assets/sheet.png — logo zone, hero, service tiles, gallery, decorative strips laid
   out in a grid, one consistent grade). Every placement is an SVG crop:
   <svg viewBox="x y w h" preserveAspectRatio="xMidYMid slice"><image href="assets/sheet.png"/></svg>
   — the viewBox IS the crop. One HTTP image, guaranteed consistent lighting, and a
   reskin = regenerate one sheet. Hero crop: subject anchored right, under a shade
   gradient solid charcoal to 43%, clearing by 54% — text zone guaranteed dark,
   image zone guaranteed clear. NEVER bake text/labels into image crops (labels are
   HTML, so the site survives image failure). If real photos are supplied instead,
   byte-verify each file before use and keep them as separate files, never one
   giant inline bundle.
6. MODALS — native <dialog>, no library: service tiles open a dialog fed from a JS
   dictionary keyed by data-service (name, one REAL descriptive paragraph — never
   lorem or one generic sentence — bullets, price-from if known), sole CTA a tel:
   button. Gallery dialog: prev/next + arrow keys + blurred backdrop. ~40 lines of
   vanilla JS total.

## CONVERSION STRUCTURE (Savage IA — this exact order, nothing else)
1. TOPBAR (30px): address + phone as proof, above everything. Phone hover = the
   second and only other use of red.
2. STICKY HEADER: logo left, nav (Services / Why Us / Work / Pricing / FAQ), one
   skewed gold call button.
3. HERO: outcome headline (what the customer GETS + locality — not the business name
   as the headline), one-line sub, skewed gold CTA + free-review secondary action.
4. STATS BAR: 4 cells × 1fr, 1px dividers, instrument numerals. Real numbers only.
5. FREE-REVIEW FUNNEL: the no-cost entry offer as a short form (name / phone / what
   do you need) directly after the hero-stats block — above the fold on desktop.
   Copy promises honesty: "We'll tell you what actually makes sense — even if
   that's less work, or no work."
6. SERVICES: 3×2 grid of dialog tiles.
7. WHY CHOOSE / ANTI-AGENCY BLOCK: name the industry's pains and negate them in a
   row ("No service writers. No upsell scripts. No getting passed from person to
   person." — adapt to the trade), then the OWNER section: real name, real photo,
   one-line creed. A named human is a conversion feature.
8. PROCESS: 3 steps. Step 2 must explicitly include recommending LESS than the
   full job when that's the honest call — recommending-against-yourself, in print,
   is the trust mechanism.
9. GALLERY / RECENT WORK: sheet-crop tiles opening the gallery dialog.
10. TESTIMONIAL(S): real only, name + context. One strong one beats five vague ones.
11. PRICING — radical transparency block (Savage) built on the Pricing Pages anatomy:
    - ONE flat starting anchor, stated in the open ("{{PRICE_ANCHOR}}").
    - Tier cards (max 3) with exactly ONE highlighted; if plans bill periodically,
      a monthly/annual switch showing the NUMERIC saving, and a comparison table
      UNDER the cards.
    - Explicit INCLUDES list and explicit EXCLUDES list, side by side.
    - Payment posture in plain language with a trades analogy ("Paid when the
      work's done — like any job on the bench.").
    - Three timeline tiers keyed to job type.
    - Every figure in this section is repeated IDENTICALLY in the FAQ — the two
      may never contradict.
12. FAQ: the full objection list — price, contract/terms, timeline, platforms/
    parts, warranty. Billing-fear questions answered in plain words.
13. CLOSING BANNER: the red parallelogram (see §3) — phone number as the headline.
14. FOOTER: hours, address, real links to Pricing and (if it exists) the Lab/demos
    page. No dead "#" links.

OPTIONAL SECOND PROPERTY — THE LAB (Savage two-site system): if this build includes
a demos/lab page, it sells TASTE while the main site sells SAFETY. Structure:
manifesto hero (claim + undercut: "WE BUILD {{THINGS}}. Nobody asked us to.") →
numbered concept chapters, each with EXACTLY: number + category/location → name H2 →
one-line tagline → full-page screenshot → "↗ Enter this world" → three mood
adjectives → verdict line → 2–3 sentence description → tag row → disclosure line
"Independent concept / Not commissioned" ON EVERY ITEM → grid repeat with live
count ("Showing 04 / 04") → why section → ONE closing CTA back to the main site
("IMAGINE WHAT WE'D BUILD IF YOU ACTUALLY HIRED US."). Every concept a DIFFERENT
design language — range is the argument. The two sites cross-link exactly once
each, at peak intent.

## SIGNATURE MOMENTS (Jon's lock: 2–3 per build — consistency is the floor)
The skew system + red banner already count as one. Pick 2 MORE from this menu and
implement them properly (no half-versions):
- PULL-CORD TOGGLE (FeralUI): a Verlet-rope pull cord (~15 points, distance
  constraints, pinned top, 3 relaxation iterations/frame) as the theme or menu
  toggle; fires on pull distance past threshold on spring-back.
- GAZE FORM MASCOT (FeralUI Blob / page-mascot): a small character by the review
  form whose gaze/lean tracks the focused field and LOOKS AWAY on password/
  sensitive fields. (page-mascot variant: two aligned 3×3 sprite sheets —
  9 head directions × 9 expressions — pointer angle picks the cell, dead zone
  kills jitter, click = 0.5s reaction; zero per-frame JS, background-position only.)
- STATUS PILL (islandcn): a Dynamic-Island-style live pill at top-center for
  async states (form sending → sent, booking steps) — closed-form springs
  (response, dampingFraction) that retarget mid-flight, content crossfades with
  blur + scale, NO animation library.
- FOIL CARD (FeralUI DeskFolio/Hologram): pointer-tilt specular sheen on the
  featured testimonial or owner card; spring-overshoot entrance.
- PHYSICS DELETE (FeralUI): cart/list removal as crumple/vacuum physics instead
  of a fade (only where the site has removable items).

## MOBILE RULES (<760px — non-negotiable)
- ALL skew REMOVED (banner and buttons go rectangular); banner stacks vertically.
- Grids collapse to one column; stats bar 2×2. Hero text zone stays readable —
  gradient becomes a bottom-up scrim.
- Tap targets ≥44px. Phone number is a tel: link everywhere it appears.
- Verify at 390px width before calling anything done.

## ACCESSIBILITY / SEO / PERFORMANCE BASELINE
- prefers-reduced-motion: disable physics/springs, crossfade instead. Focus-visible
  outlines in gold. Dialogs trap focus and close on Esc. Alt text describes the
  crop's subject. Contrast: gold on charcoal is the tightest pair — eyebrows and
  numerals already bumped (12px / 20px) for it; body text is paper-on-charcoal or
  charcoal-on-paper only.
- Semantic landmarks, one H1, title/meta description with trade + city, LocalBusiness
  JSON-LD (name, phone, address, hours, geo if known), Open Graph with a versioned
  og:image URL (?v=YYYYMMDD).
- Performance: the one-sheet image rule is the budget — total page weight target
  <1.5MB; fonts subset + preloaded; NO JavaScript frameworks for a page this size —
  vanilla JS only. Share/preview targets stay LEAN: small HTML, images as separate
  files (a 13.5MB single-file page breaks iMessage link previews).

## QA CHECKLIST (run every item; report results, don't just claim them)
[ ] Verify against the LIVE DOM (getBoundingClientRect / computed styles), not
    screenshots of a stitch — seams lie.
[ ] 390px phone-width pass: no skew, no horizontal scroll, banner stacked.
[ ] Every CTA reaches the same action (call or review form); every tel: link works.
[ ] Pricing figures identical in Pricing section and FAQ, character for character.
[ ] No invented testimonials, stats, or prices — parameters or omit.
[ ] Reduced-motion pass + keyboard-only pass (dialogs, gallery, form).
[ ] Page weight measured and under budget; og:image URL is versioned.
[ ] After ANY visual change: retake screenshots (hero at desktop + 390px) and
    refresh the share image in the SAME pass — no stale captures.
[ ] Byte-verify the deployed files match the local build before handing over
    any preview link.

## OUTPUT
Produce: index.html, style.css, script.js (vanilla, no build step), assets/sheet.png
placeholder grid (or instructions for generating the sheet), and a short BUILD-NOTES
summary listing: which signature moments were picked, any parameter left unfilled,
and the QA checklist results.
```

---

## Pattern index (mix & match)

| Pattern | One line | Source |
|---|---|---|
| Skew-and-signal buttons | Accent bg, black text, skew(−14°), hover = brightness only, icon inside the skew | Gorilla Tek |
| Parallelogram CTA banner | Full-width accent skew(−26°), children counter-skewed, −30px overlap, phone number AS the headline | Gorilla Tek |
| Two-font discipline | Heaviest italic grotesque for display + one instrument font for numbers/buttons/eyebrows; never a third | Gorilla Tek |
| Three-token color | Charcoal / paper / one signal accent; accent is signal, detonates once (the banner) | Gorilla Tek |
| Band rhythm | Full-bleed dark→light→dark bands, gradients drift 8–10 points; rhythm from contrast, not cards | Gorilla Tek |
| One-sheet imagery | Every photo/logo/tile is an SVG viewBox crop of one reference sheet; reskin = regenerate one sheet | Gorilla Tek |
| Shade-gradient hero | Solid dark to 43%, clear by 54% — text zone guaranteed dark, image zone guaranteed clear | Gorilla Tek |
| Native dialog modals | Service + gallery dialogs from a JS dictionary, ~40 lines vanilla, no library | Gorilla Tek |
| Red/gold adaptation | Gold takes every signal slot; red exactly twice (banner, one hover); bump eyebrow/numeral sizes for contrast | Round 23 adaptation of Gorilla Tek |
| Two-site split | Lab sells taste, main site sells safety; cross-link once each at peak intent | Savage |
| The Unsolicited Lab | Numbered concept chapters, fixed metadata schema, per-item "Not commissioned" disclosure, manifesto closer | Savage |
| Radical transparency block | Flat anchor price, includes AND excludes, plain-language payment posture, 3 timeline tiers, figures identical in FAQ | Savage |
| Free-review funnel | No-cost audit/review form above the fold; promise to recommend less — even nothing | Savage |
| Anti-agency copy formula | Negate the pains in a row → name the human → one-line creed | Savage |
| Conversion section order | Topbar proof → stats → services → why → work → testimonial → phone banner; one CTA action throughout | Gorilla Tek + Savage IA merged |
| Pricing anatomy | One highlighted tier; switch with numeric saving; table under cards; billing-fear FAQs; proof adjacent | Pricing Pages deck (round 6) |
| Pull-cord toggle | Verlet rope toggle, fires on spring-back past threshold | FeralUI (round 22) |
| Gaze form mascot | Mascot tracks focused field, looks away on password fields | FeralUI Blob (round 22) |
| Sprite page mascot | Two aligned 3×3 sprite sheets, pointer-angle cells, dead zone, zero per-frame JS | page-mascot (round 22) |
| Status pill | Dynamic-Island-style live status pill; closed-form springs retarget mid-flight; no animation library | islandcn (round 23) |
| Foil card | Pointer-tilt specular sheen + spring-overshoot entrance on a featured card | FeralUI (round 22) |
| Physics delete | Removal as crumple/vacuum physics instead of a fade | FeralUI (round 22) |
| Hairline card treatment | Warm hairline border + soft layered shadow; accent in a small editorial detail, never a top slab | Jon's lock (pack RULES / jon-taste) |
| 2–3 signature moments | Bespoke moments required per pass; consistency is the floor, not the ceiling | Jon's lock (MEMORY / jon-taste) |
| Lean share targets | Small HTML, separate image files, versioned og:image — link previews must survive iMessage | Jon's lock (pack RULES) |
| Screenshot freshness | Retake hero/gallery/share image in the same pass as any visual change; `?v=` stamps beat the camo cache | Jon's lock (pack RULES) |
