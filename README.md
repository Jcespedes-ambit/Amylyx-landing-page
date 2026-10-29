# Amylyx Pitch — Generic NCFB Patient Activation landing page demo

A zero-build, single-page static landing-page demo for the **Amylyx** pitch Patient Activation
funnel (**ad → landing page → form → CRM**), targeting a **generic non-cystic fibrosis
bronchiectasis (NCFB)** indication. It plugs into the Amylyx pitch deck as the live/clickable demo
artifact.

Built from the same pattern and scaffold as the **Rocket / Danon** patient-activation demo
(`Jcespedes-ambit/rocket-danon-landing-page`), used here as the template. Only the indication
content changes — the AmbitCare purple palette, Inter type, Feather-style line icons, sticky
"Start Questionnaire" CTA, and the single-page flow (disease education → "see if you qualify" →
in-page questionnaire → inline success state) all carry over.

> ⚠️ **Indication note (intentional mismatch):** the Amylyx PA deck is for **post-bariatric
> hypoglycemia (PBH)**; per the brief, Jenna/Rob wanted a **generic NCFB** demo for this pitch, so
> the demo and the deck are deliberately on different indications. The demo is the reusable NCFB
> asset; PBH stays in the deck.

## What NCFB is (plain-language anchor, from the Tampa General Hospital page)
- **NCFB = non-cystic fibrosis bronchiectasis** — a chronic, inflammatory lung condition in which the
  airways (bronchi) become permanently widened; excess mucus builds up, can harbor bacteria, and
  makes the lungs more susceptible to infection — and it is *not* the genetic, cystic-fibrosis type.
- It's a **generic** demo, so copy stays disease-education-flavored and neutral; it does **not**
  carry Amylyx product specifics.

> **Compliance / review — read before any client-facing use.** This is **demo copy, not approved
> material.** The in-page review flags were removed for a clean demo presentation, but the items they
> marked still need confirmation before this goes in front of a client:
> - **Clinical copy and the "Facts About NCFB" stat cards are sourced** from Tampa General Hospital's
>   patient-education page *"Non-Cystic Fibrosis Bronchiectasis"*
>   (<https://www.tgh.org/institutes-and-services/conditions/non-cystic-fibrosis-bronchiectasis>),
>   cited in-page. No figures were invented — the stat band uses plain descriptive facts (2 types,
>   months–years, chronic, treatable) rather than invented numbers. It's a single U.S. hospital's
>   education page, so still have a clinical reviewer confirm it before client-facing use.
> - The page is written **age-neutral** (self or a loved one). Confirm the intended audience for this
>   pitch.
> - **Demo placeholder values** that still need confirming with **Jenna / Mark / Rob**: the partner
>   line (set to "In Partnership with **Amylyx Pharmaceuticals**" for the demo), the no-cost offer
>   wording, the qualifying questions, the consent copy, and the phone number (AmbitCare default
>   `1-877-584-8995`). The three "Explore Topics" cards link to articles that don't exist yet.
> - Imagery is intentionally CSS/gradient only (no licensed stock photos); the hero uses a gradient
>   rather than the Danon mother-and-son photo, which is off-indication for a lung condition.

## Structure
```
Amylyx-landing-page/
├── index.html                                 # the single landing page (CSS/JS inline; AmbitCare logo embedded as a base64 data URI)
├── wrangler.toml                              # Cloudflare Workers assets-only config
├── .assetsignore                              # keeps README/config/spec out of the served site
├── .gitignore
├── amylyx-ncfb-demo-landing-page-spec.md      # the build brief this page was generated from
└── README.md
```

## Page sections (per the build spec §5)
Top nav · Hero · Questionnaire (`#questionnaire`) · 3-icon feature row · About NCFB (`#about`) ·
"The Facts" stat band · Meet Your Ambit Guide (`#guide`) · Explore Topics cards · Final CTA band ·
Footer. The questionnaire is reachable from every section via anchor links and a sticky CTA.

## Run it locally
No build step, no dependencies. Serve the folder from any static server and open `index.html`.
(In this environment, the Launch preview panel serves it for you.)

## Deploy to Cloudflare Workers
This repo is an **assets-only Worker** (no server script).
1. Add the repo as a new Worker in the Cloudflare dashboard (Workers & Pages → Create → connect this
   repo), **or** deploy from the CLI:
   ```
   npx wrangler deploy
   ```
2. The `[assets]` binding in `wrangler.toml` serves `index.html` at `/`.
3. Worker name is `amylyx-ncfb-demo` — change it in `wrangler.toml` to rename.

## The questionnaire
`index.html` includes a self-contained **prototype** questionnaire: on submit it validates and shows
its own success state inline — **no real data is captured or stored** (per the click-through demo
scope). To go live, swap the simulated form for the shared **Zoho native CRM webform** so each
submission lands as a **new patient at the intake stage** in the demo CRM.

## Re-theme
All color is driven by CSS custom properties in `:root` at the top of `index.html`. Swap the hex
values to re-theme (e.g. to BioMarin-derived or Amylyx tokens once branding is confirmed). Type is
Inter via Google Fonts — swap the `<link>` and font-family tokens to change it.

## Open items to confirm (don't invent — ask Jenna / Mark / Rob)
1. **How Jenna wants the demo incorporated** into the Amylyx pitch — linked on a slide, embedded, or
   standalone.
2. **Which Figma file** is the design source; pull exact colors / logo / imagery from it.
3. **Live vs. prototype** → real Zoho embed vs. the simulated form here.
4. **Branding** — generic Ambit/AmbitCare look (as shipped), BioMarin-derived (as the deck), or
   Amylyx-branded? And the "In Partnership with…" partner line.
5. **NCFB clinical copy and the stat cards** — now sourced from the APSU parents' fact sheet, but
   that source is Australian and paediatric; **validate against a U.S. clinical source** before
   client-facing use, and confirm the intended audience (age-neutral vs. caregiver/paediatric).
6. **Contact details** — reuse AmbitCare's (as shipped) or pitch-specific.
