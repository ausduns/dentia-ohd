# Orchard Heights Dental

## Purpose

This file is the canonical project memory and source-of-truth reference for the Orchard Heights Dental website.

It is intended to give any future AI agent, developer, or designer enough context to continue, rebuild, or migrate the site without starting over.

If any project files conflict with this document:
1. Confirmed Orchard Heights business facts override template content.
2. Confirmed current content decisions override legacy Framer/template defaults.
3. `@content.md` should be treated as the preferred copy source if present and current.
4. `@gemini.md` should be treated as the preferred design source if present and current.
5. Legacy exported template files are reference material only unless explicitly designated as active source files.

---

## Project Overview

- **Business:** Orchard Heights Dental is a family-oriented dental practice serving Salem / West Salem, Oregon.
- **Website purpose:** Present the practice professionally, build trust, explain services, introduce the team, surface contact details, and convert visitors into calls, appointment requests, and membership signups.
- **Primary conversion goals:** Phone calls, contact/appointment submissions, membership clicks, and general patient inquiry actions.
- **Secondary goals:** Support local SEO, establish trust through team and practice information, and support recruiting/careers if those pages remain active.
- **Current site state:** The project evolved from exported Framer/static template files and includes a `launch/` build used as the current client-preview / deployable static version.
- **Migration direction:** Move toward a cleaner implementation in React + TypeScript + Tailwind CSS + Vite + shadcn/ui if rebuilding, while preserving Orchard Heights branding, content rules, and information architecture.

---

## Priority and Hierarchy

When making future decisions, use this order of authority:

1. This `ohd-design.md` file
2. Confirmed client-approved Orchard Heights content
3. `@content.md` for copy decisions, if present and maintained
4. `@gemini.md` for design and visual system decisions, if present and maintained
5. Current launch-ready files in `launch/`
6. Legacy exported source files such as root `*2.html`
7. Original Dentia / template content only as layout reference, never as factual business content

---

## Brand and Tone

- **Brand personality:** Warm, professional, polished, approachable, and patient-first.
- **Tone of voice:** Reassuring, clear, trustworthy, welcoming, and slightly elevated rather than casual.
- **Emotional goal:** The site should feel calm, modern, high-end, competent, and family-friendly without feeling cold or overly corporate.
- **Trust signals to emphasize:** Real team names, real practice information, clear location/contact details, transparent membership/insurance notes, and polished UX.
- **What to avoid:** Generic template copy, fake placeholder team members, artificial “smile transformation” hype, blog content added just to fill space, and any language that feels spammy, salesy, or AI-generic.
- **Design guidance:** If `@gemini.md` exists and is current, use it for colors, typography, spacing, and brand presentation. Do not introduce placeholder colors; use explicit approved hex values only.

---

## Business Information

### Confirmed Facts

| Field | Value |
| --- | --- |
| Practice name | Orchard Heights Dental |
| Address | 675 Orchard Heights Rd NW, Suite 100, Salem, OR 97304 |
| Phone display | (503) 370-8787 |
| Preferred clickable phone format | `tel:+15033708787` |
| Contact email currently used on contact page | `info@orchardheightsdental.com` |
| Location framing | Salem / West Salem, Oregon |
| Membership URL | `https://www.mydentalmembership.com/orchard-heights-dental` |
| Insurance note | Orchard Heights Dental does **not** accept OHP medical insurance |

### Formatting Rules

- The phone number should always be rendered as a clickable phone link using the canonical format: `tel:+15033708787`.
- The email address should always be rendered as a clickable `mailto:` link.
- One canonical public email should be used sitewide once confirmed.

### Operational Notes

- The OHP medical insurance disclaimer is a real business constraint and must not be removed.
- Membership content should point to the external MyDentalMembership URL rather than imply an internal checkout flow.
- Business facts must never be replaced with template placeholders from old Dentia files.

---

## Team

### Confirmed Real Team Members

| Name | Role | Category |
| --- | --- | --- |
| Dr. Joseph Seare, DMD | General Dentist | Doctor |
| Tammy Lane | Patient Coordinator | Office Staff |
| Jill Matot | Patient Coordinator | Office Staff |
| Paige Mendez | Dental Hygienist | Hygienist |
| Amy Cartwright | Dental Assistant | Assistant |
| Denah Ignat | Dental Assistant | Assistant |
| Karina Nikatina | Dental Assistant | Assistant |

### Possible Additional Team Asset

| Name | Status |
| --- | --- |
| Kell Short | Image asset exists, but role and placement are not yet confirmed |

### Team Rules

- Only confirmed Orchard Heights team members may appear in live site copy.
- Never reuse template names from Dentia-era exports.
- If a bio is unknown, do not invent one.
- If a role/title is uncertain, place it in `Needs Verification` rather than guessing.

### Template Names to Exclude

The old exported files contain placeholder/template names and bios that are **not** Orchard Heights facts. These must never be used as live content. The legacy files clearly show Dentia placeholder doctors, placeholder service content, and generic footer/contact information, confirming the need to treat those files as template remnants rather than business truth.[file:51][file:53][file:54]

---

## Content and Tech Rules

### Required Content Rules

- Do **not** create a blog section unless the client explicitly requests one.
- Do **not** invent new doctors, staff members, reviews, FAQs, services, or policies.
- Do **not** introduce generic dental marketing filler just to fill empty sections.
- Do **not** imply Orchard Heights accepts OHP medical insurance.
- Do **not** rely on template placeholder text from Dentia files.

### Technical Direction

Target rebuild stack if migrating:
- React
- TypeScript
- Tailwind CSS
- Vite
- shadcn/ui

### Build Rules

- Favor a clean component-based structure over large inline-script exports.
- Replace brittle patch scripts with explicit structured content and components when rebuilding.
- Move away from legacy Framer export patterns and preserve only the useful layout/content decisions.
- Keep assets organized and explicitly referenced rather than relying on hidden DOM rewrites.
- Preserve canonical URLs, phone/email formatting, and approved page structure during migration.

---

## Active Information Architecture

These are the core pages Orchard Heights should be understood to have as part of the real site architecture.

### Home

**Purpose**
- Primary marketing landing page.
- Introduce the practice, establish trust, and drive appointment/contact action.

**Core content**
- Hero section
- Clear value proposition
- Services preview
- Team preview
- Testimonials / trust content
- Whitening or featured service visual content if approved
- Membership mention
- Contact CTA / footer contact details

**Primary CTA**
- Schedule a visit
- Call now
- Contact us

---

### About

**Purpose**
- Explain the practice, who leads it, and what kind of patient experience Orchard Heights offers.

**Core content**
- Practice overview
- Dr. Joseph Seare introduction
- Philosophy of care
- Family-friendly / patient-first positioning
- Why patients choose Orchard Heights

**Primary CTA**
- Schedule a visit
- Meet the team
- Contact us

---

### Services

**Purpose**
- Present the major service categories clearly and route users into service details or contact.

**Core content**
- Service overview
- Grouped service categories
- Service cards or structured sections
- Trust-building supporting copy
- CTA toward appointment/contact

**Primary CTA**
- Schedule a visit
- Contact us
- Learn more

---

### Service Detail

**Purpose**
- Support more focused service-level explanation where needed.

**Core content**
- Service summary
- Patient-friendly explanation
- What the service helps with
- Related services
- Appointment/contact CTA

**Important note**
- Static-hosting compatibility needs to be considered if old slug-based dynamic-style routes are still referenced.

---

### Team

**Purpose**
- Show the real Orchard Heights team and reinforce trust.

**Core content**
- Team list/grid
- Real names and roles
- Optional short bios or intros where confirmed

**Rules**
- No placeholder people
- No fabricated credentials
- No old Dentia bios

---

### Team Member Detail

**Purpose**
- Dedicated provider/team bio page where appropriate.

**Core content**
- Name
- Role
- Headshot
- Bio
- CTA to schedule or contact

**Rule**
- Only publish if the content is real and approved.

---

### Membership / Pricing

**Purpose**
- Explain membership offering and route users to the external membership platform.

**Core content**
- Membership explanation
- “Not insurance” clarification where required
- Pricing / plan overview if approved
- External CTA to MyDentalMembership

**Rule**
- Do not imply internal signup if the actual flow is external.

---

### Contact

**Purpose**
- Provide all direct contact and local conversion information.

**Core content**
- Address
- Phone
- Email
- Map/location context
- Contact or appointment request form
- OHP medical insurance disclaimer
- Office hours once confirmed

**Rules**
- Phone must be clickable with canonical `tel:+15033708787`
- Email must be clickable with `mailto:`
- Form endpoint must be real before production
- Do not add fake success states

---

### Careers

**Purpose**
- Support hiring if actively used.

**Core content**
- Open positions or a hiring message
- Practice culture
- Application CTA or instructions

**Rule**
- If careers are not active, do not invent job listings.

---

## Legacy and File Structure Notes

### Current Working Model

- `launch/` should be treated as the current deployable/client-preview static build.
- Root `*2.html` files should be treated as legacy authoring/export sources unless intentionally updated upstream.
- Experimental or obsolete template/test files should not be used as content truth.

### Known Legacy File Pattern

Likely mappings include:
- `home2.html` → `launch/index.html`
- `about2.html` → `launch/about.html`
- `services2.html` → `launch/services.html`
- `service-details2.html` → `launch/service-details.html`
- `dentists2.html` → `launch/team.html`
- `dentist-details2.html` → `launch/team-member.html`
- `pricing2.html` → `launch/membership.html`
- `contact-us2.html` → `launch/contact.html`

### Important Legacy Warning

Old Dentia exports still contain template pages and navigation references such as blog, gallery, FAQ, and placeholder staff/service content, so these files should be treated as structural artifacts rather than approved Orchard Heights content.[file:51][file:55][file:56]

---

## Services

### Confirmed / Supported Service Themes

The current project context supports Orchard Heights being positioned around:
- General / preventive care
- Cosmetic dentistry / cosmetic treatments
- Restorative dentistry
- Hygiene-related care
- Emergency-adjacent dental care
- Whitening-related content

### Service Rules

- Keep service naming consistent across nav, cards, and detail pages.
- Do not mix dynamic route assumptions with flat static deployment unless routing is intentionally configured.
- If service detail pages are not fully built, prefer a stable simplified structure over broken deep links.
- If `@content.md` defines exact service terminology, it should override inferred labels.

---

## SEO and Local Search

### Core SEO Intent

- Salem / West Salem family dentistry
- Preventive, cosmetic, restorative, and general dental care
- Local trust and discoverability
- Clear name-address-phone consistency

### SEO Rules

- Use one canonical NAP format sitewide.
- Use one canonical email sitewide.
- Normalize internal links to real deployable routes.
- Avoid broken service slug links on flat static hosting.
- Add LocalBusiness / Dentist schema once confirmed and implemented.
- Remove any remaining generic template metadata before production.

### Page-Level Intent

- **Home:** Orchard Heights Dental + Salem / West Salem family dentistry
- **About:** practice credibility + Dr. Seare + patient-first care
- **Services:** service overview + local intent
- **Membership:** membership / savings / non-insurance clarification
- **Contact:** location, phone, email, appointment/contact intent

---

## Design and UX Notes

- The current project history includes Framer-exported layouts and patch scripts, but the long-term goal should be a cleaner, more intentional structure.
- Preserve the overall feel of a premium, calm, trustworthy dental website.
- If `@gemini.md` exists, use its approved design system as the design authority.
- Use approved hex colors only; do not leave temporary color tokens or vague color placeholders.
- Keep CTAs consistent, especially “Schedule A Visit” if that is the approved phrasing.
- Preserve any approved before/after slider or featured service component only if it remains accessible and useful.
- Keep forms simple and credible.
- Do not add gimmicky motion, noisy gradients, or generic SaaS-style UI patterns that do not match a dental practice.

---

## Reusable Content Rules

### Preferred reusable business lines

Use confirmed or approved wording only. If exact copy is not approved, summarize conservatively.

### Safe reusable facts

- Orchard Heights Dental
- 675 Orchard Heights Rd NW, Suite 100, Salem, OR 97304
- (503) 370-8787
- `tel:+15033708787`
- `info@orchardheightsdental.com` (until canonical email is fully confirmed)
- OHP medical insurance is not accepted
- Membership URL: `https://www.mydentalmembership.com/orchard-heights-dental`

### Copy governance

- `@content.md` should be the preferred source for final copy if present.
- This file should define the structure and rules; `@content.md` should define finalized wording.
- If copy is missing, use placeholders only in clearly marked draft mode and never ship them as final.

---

## Implementation Constraints

- No blog unless explicitly requested.
- No placeholder staff.
- No placeholder colors.
- No fake reviews.
- No fake insurance claims.
- No fake form success behavior.
- No broken service-detail routing.
- No mixing template Dentia contact info with Orchard Heights contact info.
- No deployment with unresolved Formspree placeholder IDs.
- No silent conflict between `info@` and `information@`; one canonical email must be chosen before final launch.

---

## Assets and References

### Important known asset categories

- Team headshots
- Before/after whitening images
- Framer-exported assets and remote references
- Launch screenshots / QA artifacts if present
- Legacy HTML exports used for structure reference only

### Asset Rules

- Keep Orchard Heights-specific images distinct from template filler images.
- Confirm every staff image matches the real person.
- Confirm any before/after media is approved for use.
- Do not rely on file presence alone as proof of content approval.

---

## Needs Verification

The following items should remain unresolved until explicitly confirmed:

- Official office hours
- Canonical public email: `info@orchardheightsdental.com` vs `information@orchardheightsdental.com`
- Any additional team member beyond the confirmed roster, including Kell Short
- Final service taxonomy and exact service-detail page structure
- Whether careers pages remain active in the final production site
- JSON-LD / LocalBusiness / Dentist schema implementation
- Final map embed details and coordinates
- Final Formspree endpoint ID or replacement form backend
- Exact membership disclaimer wording in final rendered UI
- Whether `@content.md` and `@gemini.md` both exist and are current authoritative files
- Any remaining old template routes that should be removed rather than migrated
- Whether FAQ content should exist on the final Orchard Heights site; old template FAQ content exists in legacy exports and should not be assumed to be approved Orchard Heights content.[file:55]

---

## Final Rules

- This document is the durable Orchard Heights project memory.
- Use confirmed Orchard Heights facts over all template remnants.
- When uncertain, do not guess; add the item to `Needs Verification`.
- Keep the site professional, accurate, local, and conversion-focused.
- Future rebuilds should preserve business truth and user-facing clarity, not template history.