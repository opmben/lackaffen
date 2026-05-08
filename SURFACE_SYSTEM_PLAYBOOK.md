# SURFACE_SYSTEM_PLAYBOOK.md - Lack Affen

This file translates the creative direction into practical implementation rules.

Use it when building or refactoring:
- page sections
- service modules
- price tables
- review panels
- contact shells
- navigation
- buttons
- badges

It should help Claude build a coherent workshop-premium UI system without creating a rigid UI kit.

---

## 1. Purpose

The goal is to build a recognizable material language for Lack Affen.

The site should feel:
- clean
- robust
- tactile
- precise
- service-oriented
- easy to scan

It should not feel:
- flat and template-based
- copied from a SaaS design system
- copied from Metz & Partner glass surfaces
- visually noisy
- like a coupon flyer

---

## 2. Source Of Truth

Use the docs in this order:

1. `PRD.md`
   - business truth
   - conversion priorities
   - service and shop requirements

2. `DESIGN_SYSTEM.md`
   - aesthetic principles
   - brand material direction
   - CTA and imagery rules

3. `SURFACE_SYSTEM_PLAYBOOK.md`
   - practical UI families
   - reusable class names
   - implementation hierarchy

4. `CLAUDE.md`
   - coding behavior
   - implementation guardrails
   - review criteria

---

## 3. Recommended Build Layers

### Layer A: CSS tokens

Keep recurring values as CSS variables:
- surface fills
- borders
- shadows
- radius values
- brand colors
- spacing rhythm
- focus states

Avoid scattering hardcoded color and shadow recipes across components.

### Layer B: Reusable utility classes

Recommended class families:
- `.surface-workshop`
- `.surface-detail`
- `.surface-price`
- `.surface-review`
- `.surface-contact`
- `.button-primary`
- `.button-secondary`
- `.badge-stamp`

These should carry the recurring visual behavior.

Components should compose layout and content rather than repeatedly redefining material styles.

### Layer C: Typed content modules

Use typed data modules for:
- services
- price tiers
- testimonials or approved reviews
- contact information
- gift card amounts
- navigation items

This keeps facts centralized and easier to verify.

---

## 4. Surface Families

### `.surface-workshop`

Use for:
- hero content shell
- main service sections
- contact block
- large section containers

Should feel:
- robust
- clean
- lightly elevated
- workshop-like but polished

Suggested qualities:
- tinted warm neutral background
- subtle border
- restrained shadow
- low radius, usually 8px or less unless the app establishes otherwise
- strong spacing hierarchy

Do not turn it into:
- heavy glassmorphism
- generic rounded SaaS cards
- dark luxury panels

### `.surface-detail`

Use for:
- image captions
- before/after modules
- process details
- supporting service notes

Should feel:
- precise
- compact
- subordinate to major surfaces

### `.surface-price`

Use for:
- price tiers
- vehicle category pricing
- service package comparison

Rules:
- price must be easy to find
- vehicle category must be clear
- included services must be scannable
- unknown or custom pricing should use `auf Anfrage` or `nach Begutachtung`, not invented values

### `.surface-review`

Use for:
- approved testimonials
- review summaries
- Google Maps review prompts

Rules:
- never fake ratings or review counts
- never scrape Google reviews
- keep quote length controlled
- link to Google Maps for full external reviews

### `.surface-contact`

Use for:
- contact form
- phone/email/maps section
- appointment inquiry shell

Rules:
- contact options must be prominent on mobile
- form fields must have labels
- privacy consent must be explicit
- `Termin anfragen` should be the dominant action

---

## 5. Button System

### `.button-primary`

Use only for the primary appointment action.

Required visible text:

`Termin anfragen`

Characteristics:
- strong contrast
- clear focus state
- large touch target
- direct placement near decision points

### `.button-secondary`

Use sparingly for non-conversion actions that do not compete with appointment inquiry.

Do not use `.button-secondary` for `Gutschein kaufen`.

Acceptable uses:
- quiet utility actions
- form-adjacent actions
- non-prominent navigation controls

### Link treatment

Gift card access should usually be a normal text link or low-emphasis nav/footer link.

Do not style gift card access as a major button.

---

## 6. Badge System

### `.badge-stamp`

Use for:
- small trust labels
- service category labels
- brand-flavored markers
- verified local notes

Visual direction:
- inspired by the red stamp in the logo
- restrained
- never overused
- not a replacement for real proof

Do not use badge styling to invent credibility.

---

## 7. Service And Price Execution

Service sections should be built for scanning.

Recommended structure:
- service group name
- short practical description
- included work
- price or pricing rule
- vehicle category where relevant
- `Termin anfragen` action where useful

Avoid:
- long paragraph walls
- equal-weight generic cards for every minor service
- icons as decoration
- hiding important price qualifiers

For premium/custom work, prefer:
- `nach kostenloser Begutachtung`
- `auf Anfrage`
- clear explanation that vehicle condition affects scope

---

## 8. Review And Proof Execution

Proof should come from:
- real photos
- before/after visuals
- approved customer quotes
- Google Maps link
- clear service examples

Review sections should:
- show a small curated set only if approved
- provide a link to Google Maps for more reviews
- avoid copying large review blocks from external platforms

Never fabricate review data.

---

## 9. Mobile Rules

Mobile is a primary experience.

Required behavior:
- `Termin anfragen` remains easy to reach.
- Phone, email, and route are easy to tap.
- Service prices remain readable.
- Images do not hide essential text.
- Forms are not cramped.
- Sticky UI must not cover content.

Avoid:
- oversized hero text that pushes contact access too far down
- multiple competing buttons
- decorative content before practical contact paths

---

## 10. Final Review

Before shipping UI work, confirm:
- the only visible CTA text is `Termin anfragen`
- surfaces feel related and specific to Lack Affen
- services and prices are scan-friendly
- reviews are handled legally and honestly
- mobile contact flow is fast
- no Metz & Partner glass language remains

