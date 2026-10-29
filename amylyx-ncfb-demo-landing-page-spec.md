# Amylyx Pitch — Generic NCFB Patient Activation Demo Landing Page (Build Spec)

> Hand this file to Claude Code as the brief for generating the demo landing page.
> ⚠️ Read §1 first: the deck and the demo are intentionally on **different indications**.

---

## 1. Read this first — the indication mismatch is intentional

- The **Amylyx PA deck** Mark built is for **post-bariatric hypoglycemia (PBH)** and used **BioMarin** as the design starting point.
- The **demo** to incorporate into that pitch is a **generic NCFB (non-cystic fibrosis bronchiectasis)** demo. Per Mark: *Jenna/Rob wanted to use a generic NCFB demo for this pitch — which is why the indications don't match.*
- **So: build the landing-page demo around NCFB (generic), not PBH.** The PBH framing stays in the deck; the demo is the reusable NCFB asset.
- **Open item (confirm with Jenna):** exactly how she wants the demo incorporated — linked from a slide, embedded, or standalone. This affects nothing about the page build itself, but determines how it's delivered.

---

## 2. What this is

A **click-through Patient Activation (PA) demo landing page** — the direct-to-patient/caregiver funnel (**ad → landing page → form → CRM**) — matching Ambit's standard PA demo pattern. Indication: **generic NCFB**. It plugs into the Amylyx pitch deck as the live/clickable demo artifact.

This is the same build pattern as the Rocket/Danon landing page (see that spec for the detailed section-by-section template and the Zoho-form approach). The structure below mirrors it; only the indication content changes.

---

## 3. Demo scope & technical notes

- **Click-through demo.** Like past PA Commercial demos, it shows what the ads / landing page / form look like. Does **not** need to capture real data or handle consent unless published live.
- **Form options** (same decision as the Danon build):
  - **Live page** → embed a **Zoho native CRM webform** so leads flow into the demo CRM; each submission lands as a **new patient at the intake stage**. Style the form to match the page.
  - **Prototype / click-through** → simulate the form submission (fake success state); no real data captured.
- **Design source:** there is a **Figma file** tied to this demo (Mark confirmed the Amylyx demo relates to the Figma file referenced in the thread — Juan noted one sent the prior day). **Confirm which Figma file** and pull exact colors / logo / imagery from it.
- **Design lineage:** the deck used **BioMarin** as a starting point. Confirm whether the *demo* should visually echo BioMarin, the generic Ambit/AmbitCare look, or Amylyx branding.
- U.S. residents only. Brand framing: **AmbitCare / Ambit Guides** (confirm partner/brand line for this pitch).

---

## 4. Indication content — NCFB (generic)

⚠️ **The source email contains no clinical brief for NCFB.** Do **not** invent prevalence figures, statistics, or clinical claims. Use clearly-labeled placeholder copy and leave `[CONFIRM]` tags for anything factual, to be supplied by Jenna/Mark or a clinical source before the demo goes in front of a client.

Plain-language anchor (high level only):
- **NCFB = non-cystic fibrosis bronchiectasis** — a chronic lung condition where the airways (bronchi) become permanently widened and damaged, leading to mucus buildup, recurrent infections, and persistent cough — *not* caused by cystic fibrosis.
- Because it's a **generic** demo, copy can stay disease-education-flavored and relatively neutral; it doesn't need Amylyx product specifics.

Everything below marked `[CONFIRM]` is a placeholder:
- Prevalence / epidemiology → `[CONFIRM]`
- Signs & symptoms specifics → `[CONFIRM]`
- Diagnostic pathway / testing → `[CONFIRM]`
- Any statistics in the "facts" section → `[CONFIRM]`

---

## 5. Page structure — section-by-section (Ambit PA template)

Reuse the standard Ambit PA landing-page flow (same scaffold as the Danon page). Keep the "no-cost • educational support • no obligations" and "not medical providers" framing throughout.

### 5.1 Top nav
- AmbitCare logo · "In Partnership with **[partner — CONFIRM]**" · `Start Questionnaire →` (anchors to `#questionnaire`).

### 5.2 Hero
- Eyebrow: **"Bronchiectasis & Your Lungs"** (or similar — generic).
- H1: **"Living with chronic cough and recurring lung infections?"** `[refine]`
- Body: Short, plain-language intro to NCFB and the idea that an Ambit Guide can connect them with no-cost educational support / counseling and help determine if they qualify for next steps. `[CONFIRM clinical specifics]`
- CTAs: `Start Questionnaire` (#questionnaire) · `Meet Your Guide` (#guide)
- Trust line: **"No-cost • educational support • no obligations"**

### 5.3 Questionnaire  `#questionnaire`
- Heading: **"See If You Qualify for No-Cost [Counseling/Support]"** `[CONFIRM offer]`
- Badge: **⏱ 5 minutes**
- Intro: Complete if you or a loved one has `[symptom/criteria — CONFIRM]` and would like to speak with an Ambit Guide.
- **Form** = Zoho webform (live) or simulated (prototype). Suggested fields: First name, Last name, Email, Phone, ZIP, Relationship (self / caregiver / other), `[condition-specific qualifying questions — CONFIRM]`, consent checkbox (non-functional in prototype). On submit → success state → new patient @ intake in CRM.

### 5.4 Meet Your Ambit Guide  `#guide`
- Heading: **"Meet Your Ambit Guide"** · "Guides Available Now"
- Guide value prop + contact block: `mail guide@ambitcare.com` · `phone [CONFIRM]` · `schedule Mon–Fri, 9–5pm ET` (reuse AmbitCare defaults unless this pitch has its own).
- Value-prop strip: Talk to a Guide · Access no-cost support · Speak one-on-one · Get answers · Support for you or a loved one · Move forward with confidence.
- **Important Notice:** Ambit Guides are not medical providers; they can neither diagnose nor endorse/recommend treatments.
- CTA: `Start Questionnaire →`

### 5.5 About the condition
- Heading: **"About Non-Cystic Fibrosis Bronchiectasis (NCFB)"**
- 2–3 short paragraphs, plain language, `[CONFIRM clinical content]`. Close with how speaking to a Guide / next steps can help.
- CTA: `Start Questionnaire →`

### 5.6 "The Facts" stat cards (carousel)
- Mirror the template's research-backed stat carousel. **All figures `[CONFIRM]` — none supplied in the email; do not fabricate.** Leave placeholder cards with clearly-marked `[CONFIRM: stat]`.

### 5.7 Explore Topics (blog cards)
- Three educational placeholder cards + "Read Article →":
  - **What Is Bronchiectasis (and What Isn't)?** `[placeholder]`
  - **Why Recurring Infections Shouldn't Be Ignored** `[placeholder]`
  - **Talking to Your Care Team About Your Lungs** `[placeholder]`

### 5.8 Final CTA band
- Heading: **"You don't have to figure this out alone."**
- Copy + buttons: `Complete the Questionnaire →` · `Email Us Instead`
- Contact line: `phone [CONFIRM] · mail guide@ambitcare.com · schedule Mon–Fri, 9am–5pm ET`

### 5.9 Footer
- Logo · contact · FAQs · Terms & Conditions · Privacy Policy.
- Reuse AmbitCare disclaimer verbatim (U.S. residents only; not a medical provider; etc.).
- `© 2026 AmbitCare. All Rights Reserved.` · "In Partnership with [partner — CONFIRM]"

---

## 6. Design direction
- Calm, clinical, trustworthy: clean sans-serif, generous whitespace, soft brand accent, rounded cards, sticky "Start Questionnaire" CTA.
- Fully responsive; questionnaire reachable from every section via anchor links.
- Accessibility: real field labels, sufficient contrast, keyboard-navigable.
- Pull exact colors/logo/imagery from the confirmed Figma file (§3).

---

## 7. Open items to confirm (don't invent — ask Jenna/Mark/Rob)
1. **How Jenna wants the demo incorporated** into the Amylyx pitch — linked on a slide, embedded, or standalone.
2. **Which Figma file** is the design source (confirm it's the one referenced in the thread).
3. **Live vs. prototype** → real Zoho embed vs. simulated form.
4. **Branding** — generic Ambit/AmbitCare look, BioMarin-derived (as the deck), or Amylyx-branded? And the "In Partnership with…" line.
5. **All NCFB clinical copy and every statistic** — needs a real source before client-facing use.
6. **Contact details** — reuse AmbitCare's, or pitch-specific.

---

## 8. Source thread (for reference)
Outlook thread **"Amylyx PA Deck" / "Re: Amylyx PA Deck"** (Mark Daniels → Jenna Utecht, cc Juan Cespedes, Oct 29 2026).
- Mark (4:06 PM): PA deck for Amylyx (post-bariatric hypoglycemia); demo not yet included; BioMarin used as starting point; deck link in the email.
- Juan (4:23 PM): confirmed the demo ties to the Figma file Mark sent the prior day.
- Mark (4:27 PM): confirmed yes; Jenna/Rob chose a **generic NCFB demo** for this pitch (hence the indication mismatch); ask Jenna how she wants it incorporated.
