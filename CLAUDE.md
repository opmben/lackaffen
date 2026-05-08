# CLAUDE.md - Lack Affen Implementation Guardrails

This document defines how Claude Code should operate in this repository.

It is not a copy deck, not a fixed page script, and not a component specification.

---

## 1. Purpose

Claude should build a website that feels:
- trustworthy
- local
- polished
- hands-on
- premium in craft, not fake luxury
- clear enough for fast mobile decisions

The commercial goal is simple: turn visitors into qualified appointment inquiries for Lack Affen auto detailing in Boppard/Bad Salzig.

The website may include gift card purchasing, but that flow is secondary and must not compete with the appointment inquiry path.

---

## 2. Source Of Truth

Use the documents in this order:

1. `PRD.md`
   - verified business truth
   - audience context
   - conversion priorities
   - legal and honesty constraints

2. `DESIGN_SYSTEM.md`
   - brand feel
   - visual principles
   - imagery, composition, and copy direction
   - explicit no-gos

3. `SURFACE_SYSTEM_PLAYBOOK.md`
   - practical UI execution rules
   - reusable surface and button families
   - section and component guidance

4. `CLAUDE.md`
   - repository behavior
   - implementation guardrails
   - review checklist

If documents conflict:
- preserve verified facts from `PRD.md`
- preserve the single CTA rule from this file and `PRD.md`
- preserve the design direction from `DESIGN_SYSTEM.md`
- do not invent missing business facts

---

## 3. Hard Constraints

### Primary conversion
- The only visible CTA text is `Termin anfragen`.
- Do not use `Gutschein kaufen` as a CTA.
- Gift cards may exist as a secondary feature, but should not be framed as a major conversion path.

### Truth and integrity
- No fake testimonials.
- No fake review counts or ratings.
- No fake opening hours.
- No fake guarantees.
- No invented certificates, partner logos, trust badges, or awards.
- No unsupported claims such as "best", "number one", or quantified outcomes unless verified.

### Technical baseline
Preferred implementation baseline:
- Next.js App Router
- TypeScript strict
- Tailwind CSS
- React Hook Form + Zod
- Resend for contact email
- Stripe Checkout for gift cards
- Lucide React for icons

Treat the repository itself as the source of truth if the stack evolves.

### Repository integrity
- Prefer TypeScript.
- Avoid `any`.
- Read relevant files before changing them.
- Keep implementation maintainable and production-grade.
- Keep business data in typed modules where practical.

---

## 4. Creative Expectations

Claude is expected to:
- avoid generic SaaS or agency website patterns
- use real vehicle-detailing imagery as persuasion
- make services and prices easy to scan
- keep the mobile journey direct and useful
- make contact paths obvious without creating multiple competing CTAs
- build trust through concrete work, local presence, reviews, and clarity
- use the logo and monkey mascot with restraint

Claude may:
- improve the information architecture
- merge or remove weak sections
- propose better content structure
- use strong visual hierarchy and asymmetry
- use motion if it improves comprehension and perceived quality

Claude should not:
- make the website feel like a cartoon brand site
- make it feel like a luxury car showroom detached from real workshop work
- use fake premium language
- bury the appointment inquiry path
- over-emphasize the gift card flow

---

## 5. Content Rules

### Language
- German is the default website language.
- Use plain, confident, concrete wording.
- Short English terms are acceptable only where natural.

### Copy quality
Avoid:
- empty marketing phrases
- generic "premium service" filler
- unsupported superiority claims
- long blocks of explanation where images or structured details would be clearer

Prefer:
- concrete services
- clear value for leasing returns, resale, hygiene, odor, pets, family use, and enthusiast care
- direct appointment-oriented microcopy
- local trust signals
- short, scan-friendly sections

### Review content
Use the Google Maps link as the primary external review and route source:
`https://maps.app.goo.gl/5xgYCMWZzYuMqq3L7`

Do not scrape Google reviews. If review quotes appear on the site, they must be:
- manually curated and approved, or
- sourced from existing approved customer quotes, or
- displayed through a legally acceptable third-party or official widget.

---

## 6. Implementation Rules

Prefer:
- image-led sections
- clear price tables and service modules
- large touch targets on mobile
- sticky or easily reachable appointment inquiry access
- typed data modules for repeated content
- semantic HTML and accessible forms

Avoid:
- generic feature-card grids
- decorative icon spam
- gradient text
- glassmorphism copied from unrelated projects
- excessive dark luxury styling
- visible secondary CTA competing with `Termin anfragen`
- hardcoded business facts scattered across components

Gift card pages may exist, but links to them should read as navigation or utility links, not prominent CTAs.

---

## 7. Motion Rules

Motion should be restrained and functional.

Use motion for:
- section entrances
- before/after reveal moments
- form feedback
- hover and focus states
- subtle detail polish

Do not use motion that:
- slows down appointment inquiry
- makes the mobile site feel heavy
- creates gimmick energy
- distracts from vehicle results

Always respect reduced-motion preferences.

---

## 8. Review Checklist

Before considering work complete, check:

- Is `Termin anfragen` the only visible CTA text?
- Is the appointment path obvious within seconds?
- Is the gift card flow secondary?
- Are all business facts verified or clearly marked as placeholders?
- Are reviews handled without scraping or fabrication?
- Does the design feel like premium workshop craft, not generic SaaS or fake luxury?
- Are services and prices easy to scan?
- Does mobile feel intentionally designed?
- Do phone, email, and Google Maps links work?
- Is TypeScript strict and free of `any`?
- Do lint, typecheck, and build pass?

