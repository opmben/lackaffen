# PRD.md - Lack Affen Website Product Brief

This document defines business truth, website goals, audience context, conversion priorities, and non-negotiable honesty rules.

It does not define fixed copy, exact layouts, or final component structure.

---

## 1. Project Overview

**Brand:** Lack-Affen / Lack Affen Die Autoaufbereiter  
**Current website:** `https://lack-affen.de`  
**Location:** Boppard/Bad Salzig, Rheinland-Pfalz, Germany  
**Google Maps:** `https://maps.app.goo.gl/5xgYCMWZzYuMqq3L7`

**Core purpose of the website:**  
Generate more qualified appointment inquiries for professional auto detailing, vehicle preparation, and vehicle care.

**Primary contact paths:**
- Contact / appointment inquiry form
- Phone
- Email
- Google Maps route

**Primary CTA text:**  
`Termin anfragen`

No other visible CTA text should compete with this.

---

## 2. Verified Business Truths

The following facts may be treated as verified unless explicitly updated:

- Lack Affen is an auto detailing / vehicle preparation business in Boppard/Bad Salzig.
- The business provides professional vehicle cleaning, preparation, polishing, care, and related detailing services.
- The current public contact address is:
  - Unten in der Aab 6
  - 56154 Boppard/Bad Salzig
- The current public email address is `info@lack-affen.de`.
- The current public phone number is `06742 - 89 74 16 5`.
- The current website includes services, prices, contact, legal pages, and a gift card product.
- The website should preserve gift card purchasing as a secondary function.
- The website should make appointment inquiries the dominant conversion path.

Anything not listed here should be treated as unverified until confirmed.

---

## 3. Website Goals

### Primary Goal
Generate qualified appointment inquiries.

### Secondary Goals
- Improve perceived quality and trust.
- Present services and pricing more clearly than the current website.
- Support local search and Google Maps usage.
- Preserve gift card purchase capability through Stripe Checkout.
- Make mobile contact paths faster and easier.

### Success Signals
- More contact form submissions.
- More phone taps from mobile.
- More route clicks to Google Maps.
- Visitors quickly understanding what Lack Affen offers.
- Gift card orders working without distracting from appointment inquiries.

---

## 4. Audience Context

### Primary Audiences
- Private vehicle owners who want their car cleaned, refreshed, or protected.
- Leasing customers preparing for vehicle return.
- Car enthusiasts who care about paint, gloss, polish, and protection.
- Families with heavily used interiors.
- Dog owners and pet owners dealing with hair and odor.
- Business customers with company cars or fleet vehicles.
- Gift buyers looking for a vehicle-care gift card.

### User Psychology
Visitors likely care about:
- trust
- visible results
- clean pricing
- fast appointment contact
- whether the team can handle their specific vehicle issue
- local credibility
- reviews and recommendations

Visitors may be turned off by:
- outdated visuals
- unclear pricing
- too much text
- cartoonish execution
- fake luxury language
- hidden contact options
- competing calls to action

---

## 5. Offer And Service Framing

The website should present Lack Affen as a professional auto detailing and vehicle preparation provider.

Current service categories and examples from the existing site include:
- Basic interior cleaning
- Basic exterior cleaning
- Premium package after free vehicle inspection
- Ozone treatment
- Engine bay cleaning and sealing
- Headliner cleaning
- Leather repair
- Ceramic coating
- Rim refinement
- Upholstery or carpet cleaning
- Glass sealing
- Pet hair removal
- Convertible top cleaning
- Leather cleaning and intensive care
- Dent technique
- Polishing
- Wax sealing
- Tar removal
- Iron fallout removal

Prices from the current site may be used as starting data, but must be verified before launch.

### Appointment Inquiry Framing
All major conversion moments should lead to `Termin anfragen`.

The inquiry flow should support:
- desired service
- vehicle type
- contact details
- free message
- privacy consent

### Gift Card Framing
Gift cards are a secondary function.

They may be available through:
- a quiet navigation link
- footer link
- dedicated gift card page
- informational mention inside legal/shop context

They should not use a visible CTA labeled `Gutschein kaufen`.

---

## 6. Google Maps And Reviews

Google Maps link:
`https://maps.app.goo.gl/5xgYCMWZzYuMqq3L7`

Use this link for:
- route planning
- external review access
- local trust
- contact section utility
- LocalBusiness structured data where appropriate

Do not scrape Google reviews.

Review content may only be used if:
- manually curated and approved,
- sourced from existing approved website testimonials,
- or displayed through a legally acceptable official or third-party integration.

Review counts, ratings, and excerpts must not be invented.

---

## 7. Legal And Compliance

Because gift card purchasing is planned, the website should include:
- Impressum
- Datenschutz
- AGB
- Widerruf
- Versand & Zahlung

Legal text should be copied from approved current sources or reviewed externally before launch.

Do not freely rewrite legal pages as final legal advice.

Contact forms must include privacy consent.

Cookie and analytics behavior must match the actual implementation.

---

## 8. Technical Direction

Preferred stack:
- Next.js App Router
- TypeScript strict
- Tailwind CSS
- React Hook Form + Zod
- Resend for contact emails
- Stripe Checkout for gift cards
- Lucide React for icons

Expected environment variables:
- `STRIPE_SECRET_KEY`
- `STRIPE_WEBHOOK_SECRET`
- `NEXT_PUBLIC_SITE_URL`
- `RESEND_API_KEY`
- `CONTACT_TO_EMAIL`

---

## 9. Current Content Sources

Use these sources as starting points:
- Current website: `https://lack-affen.de`
- Services and prices: `https://lack-affen.de/leistungen-und-preise/`
- Contact page: `https://lack-affen.de/kontakt/`
- Gift card page: `https://lack-affen.de/produkt/gutschein-freude-verschenken-lackaffen-die-autoaufbereiter/`
- Google Maps: `https://maps.app.goo.gl/5xgYCMWZzYuMqq3L7`
- Logo asset currently provided by the project owner: `Lackaffen-Logo-Mobile.jpg`

New real photography is a launch requirement.

---

## 10. What This Document Must Not Become

This file must not become:
- a fixed homepage screenplay
- a final copy deck
- a component specification
- a legal document
- a rigid creative cage

It should preserve verified business truth and conversion priorities while leaving implementation room for better design decisions.

