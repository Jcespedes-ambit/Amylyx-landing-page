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

## What NCFB is (plain-language anchor, from the brief)
- **NCFB = non-cystic fibrosis bronchiectasis** — a chronic lung condition where the airways
  (bronchi) become permanently widened and damaged, leading to mucus buildup, recurrent infections,
  and a persistent cough — *not* caused by cystic fibrosis.
- It's a **generic** demo, so copy stays disease-education-flavored and neutral; it does **not**
  carry Amylyx product specifics.

> **Compliance / review — read before any client-facing use.** This is **demo copy, not approved
> material.** The source brief contained **no clinical brief and no statistics for NCFB**, so:
> - **No prevalence figures, statistics, or clinical claims were invented.** The "Facts About NCFB"
>   band ships with **placeholder stat cards** (`[ stat ] CONFIRM`) that must be sourced before use.
> - Every unconfirmed item is marked inline with a small amber **`CONFIRM` / `placeholder` / `refine`**
>   flag (`.flag` class) so reviewers can see exactly what is placeholder. Remove the flags once the
>   real copy is confirmed.
> - The partner line ("In Partnership with **[Partner — CONFIRM]**"), the offer wording, the
>   qualifying questions, consent copy, and the phone number (shown as the AmbitCare default,
>   flagged) are all placeholders pending confirmation with **Jenna / Mark / Rob**.
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
5. **All NCFB clinical copy and every statistic** — needs a real source before client-facing use.
6. **Contact details** — reuse AmbitCare's (as shipped) or pitch-specific.
