# Lack Affen Website

Website project for Lack Affen / Lack Affen Die Autoaufbereiter in Boppard/Bad Salzig.

The repository is guided by the Markdown documents in the project root:

- `PRD.md` - business truth, goals, audiences, service context, compliance notes
- `DESIGN_SYSTEM.md` - creative direction and visual principles
- `SURFACE_SYSTEM_PLAYBOOK.md` - practical UI surface and component guidance
- `CLAUDE.md` - implementation guardrails for Claude Code
- `AGENTS.md` - local agent instructions

## Project Goal

Build a modern website that generates qualified appointment inquiries for professional auto detailing and vehicle preparation.

The only visible CTA text is:

```text
Termin anfragen
```

Gift cards remain a secondary feature and should not compete with the appointment inquiry path.

## Planned Stack

| Layer | Technology |
| --- | --- |
| Framework | Next.js App Router |
| Language | TypeScript strict |
| Styling | Tailwind CSS + CSS variables |
| Forms | React Hook Form + Zod |
| Email | Resend |
| Payments | Stripe Checkout |
| Icons | Lucide React |

## Planned Environment Variables

```env
STRIPE_SECRET_KEY=sk_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_SITE_URL=https://...
RESEND_API_KEY=re_...
CONTACT_TO_EMAIL=info@lack-affen.de
```

## Business References

- Current website: https://lack-affen.de
- Services and prices: https://lack-affen.de/leistungen-und-preise/
- Contact: https://lack-affen.de/kontakt/
- Gift card product: https://lack-affen.de/produkt/gutschein-freude-verschenken-lackaffen-die-autoaufbereiter/
- Google Maps: https://maps.app.goo.gl/5xgYCMWZzYuMqq3L7

## Verified Contact Details

```text
Lack-Affen / Lack Affen Die Autoaufbereiter
Unten in der Aab 6
56154 Boppard/Bad Salzig

info@lack-affen.de
06742 - 89 74 16 5
```

## Implementation Notes

- Keep business facts centralized in typed data modules once the app is scaffolded.
- Do not invent reviews, review counts, ratings, opening hours, guarantees, or certificates.
- Do not scrape Google reviews.
- Use Google Maps as the external route and review source.
- Treat current prices and services as starting data that must be verified before launch.
- New real photography is required before launch.
- Legal pages are required because gift card purchasing is planned: Impressum, Datenschutz, AGB, Widerruf, Versand & Zahlung.

## Planned Commands

These commands should exist once the app is scaffolded:

```bash
npm run dev
npm run lint
npm run build
npx tsc --noEmit
```
