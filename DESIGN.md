---
name: Mind & Soul
description: One-page editorial-minimalist site for a humanist psychotherapy practice in Texcoco, México
colors:
  paper-white: "#FFFFFF"
  hairline-gray: "#E5E5E5"
  quiet-gray: "#9E9E9E"
  reading-ink: "#333333"
  editorial-black: "#000000"
  editorial-red: "#E53935"
typography:
  display:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "clamp(2.6rem, 6vw, 4.4rem)"
    fontWeight: 500
    lineHeight: 1.05
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "clamp(2rem, 4vw, 2.9rem)"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  heading:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "clamp(1.6rem, 3vw, 2rem)"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Fraunces, Georgia, serif"
    fontSize: "1.25rem"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Manrope, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  secondary:
    fontFamily: "Manrope, -apple-system, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
  label:
    fontFamily: "Manrope, -apple-system, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0.18em"
rounded:
  none: "0px"
  pill: "50%"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  xl: "70px"
  section: "110px"
components:
  button-primary:
    backgroundColor: "{colors.editorial-red}"
    textColor: "{colors.paper-white}"
    rounded: "{rounded.none}"
    padding: "13px 26px"
  button-primary-hover:
    backgroundColor: "{colors.editorial-red}"
    textColor: "{colors.paper-white}"
  button-ghost:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.reading-ink}"
    rounded: "{rounded.none}"
    padding: "13px 26px"
  button-ghost-hover:
    backgroundColor: "{colors.editorial-black}"
    textColor: "{colors.paper-white}"
  card:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.reading-ink}"
    rounded: "{rounded.none}"
    padding: "38px 32px"
---

# Design System: Mind & Soul

## 1. Overview

**Creative North Star: "The Editorial Consulting Room"**

Mind & Soul reads like a well-set page in a printed magazine that happens to be about therapy, not like a wellness app or a Canva template with a leaf icon. The base is paper-white and three tiers of gray, set in a serif/sans pairing with generous whitespace and hairline rules instead of boxes and shadows. Red appears exactly where a decision needs to happen and nowhere else: it is punctuation, not paint.

This system explicitly rejects the generic "therapist template" (leaf/hand icons, pastel gradients, stock-photo warmth) and the cold corporate-clinical look (navy, sterile grids, hospital whites). It also rejects decorating for its own sake: no drop shadows as default elevation, no rounded-everything softness, no gradient text, no card-in-a-card nesting.

**Key Characteristics:**
- Paper-white and gray-scale carry over 90% of every screen; red is reserved for the single most important action or number in view.
- Serif display type (Fraunces) for anything that should feel considered and human; sans (Manrope) for everything functional.
- Flat surfaces, hairline dividers, sharp corners; the rare dark section (footer, one feature block, the closing CTA) exists for rhythm, not by default.
- Mobile is treated as the primary reading surface, not a squeezed-down desktop layout: long stacks (services, gallery) become single-row, swipeable carousels rather than tall vertical stacks.
- The page reveals itself as one rehearsed sequence on scroll (fade + rise, staggered per card), not as scattered micro-interactions; `prefers-reduced-motion` collapses it to an instant, fully-visible page.

## 2. Colors

Overwhelmingly neutral, restrained-strategy palette: five grayscale steps plus one saturated accent that is deliberately rationed.

### Primary
- **Editorial Red** (#E53935): the only saturated color in the system. Used for the primary booking CTA, the italicized emphasis word in the hero headline, the small numeral marks (value props, process steps, the years-of-experience badge), active/open states (FAQ), and destacar links ("Solicitar información"). Never used as a section background or large surface.

### Neutral
- **Paper White** (#FFFFFF): the default page background and card surface. The resting state of the whole site.
- **Hairline Gray** (#E5E5E5): secondary section backgrounds (alternating bands), all borders and grid dividers, image placeholders before real photography is dropped in.
- **Quiet Gray** (#9E9E9E): decorative/secondary icons only (service icons, location icons, the closed-state FAQ chevron) — never body copy, to protect legibility.
- **Reading Ink** (#333333): the default body-copy color. Every paragraph, description, and label that must actually be read sits here, not in a lighter gray, so contrast stays high on a page read by an older, less tech-fluent audience.
- **Editorial Black** (#000000): headings, the header/nav wordmark, and the handful of intentionally dark surfaces (footer, trust strip, the floating quote/stat badges on the "About" photo).

### Named Rules
**The Rationed Red Rule.** Red never covers a surface larger than a button or a badge. If a whole section wants to feel important, it goes to Editorial Black or a mid-gray dark surface, not red.
**The Readable Gray Rule.** Quiet Gray (#9E9E9E) is for icons and truly decorative marks only. Anything a visitor is meant to read is Reading Ink (#333333) or darker.

## 3. Typography

**Display Font:** Fraunces (with Georgia, serif fallback)
**Body Font:** Manrope (with -apple-system, sans-serif fallback)

**Character:** A warm, slightly editorial serif for anything that carries feeling or authority (headlines, names, pull quotes, numerals), paired with a clean, modern grotesque for everything functional (paragraphs, nav, labels, buttons). The pairing reads as "a magazine profile of a professional," not "a SaaS landing page."

### Hierarchy
A seven-step scale, `--text-*` custom properties, ratio ≥1.25 at every step that needs real separation:
- **Display** (500, `clamp(2.6rem, 6vw, 4.4rem)`, line-height 1.05): the hero headline only.
- **Headline** (500, `clamp(2rem, 4vw, 2.9rem)`, line-height 1.15): section titles ("Cómo puedo acompañarte", "Terapia con enfoque humanista").
- **Heading** (500, `clamp(1.6rem, 3vw, 2rem)`, line-height 1.15-1.2): third-level titles (the practitioner's name, "Consultorio").
- **Title / Subheading** (500, 1.25rem): card and item titles (service names, value-prop and process-step titles, FAQ questions). One size for every mid-level title on the page, no exceptions.
- **Body** (400, 1rem, line-height 1.6): every real paragraph, no exceptions, in Reading Ink. Previously several description paragraphs sat at 14-15px; all body copy is now 16px minimum. Capped near 38-65ch per container so no paragraph runs wider than a comfortable reading measure.
- **Secondary** (400, 0.875rem): nav links, button labels, footer links and blurb, testimonial attribution — supporting UI text that is deliberately quieter than body copy, never used for sentences meant to be read closely.
- **Label** (600, 0.75rem, letter-spacing 0.18em, uppercase): eyebrow kickers, micro-labels (about-tags, field labels, footer copyright), in Reading Ink.

Decorative display numerals (the 01-04 markers, the testimonial quote mark, the years-of-experience badge) sit outside this scale on purpose. They are singular accents, not part of the reading hierarchy, so they don't need to fit the ratio.

### Named Rules
**The Serif-Says-It-Matters Rule.** If a piece of text is switched into Fraunces italic (the hero's emphasis word, pull quotes, numerals), it is because that specific phrase or figure is the emotional or informational point of its section. Italic serif is never used decoratively.
**The One Title Size Rule.** Every mid-level title on the page (service, value prop, process step, FAQ question) is `--text-subheading` (1.25rem). A new card or grid does not get to invent its own title size.

## 4. Elevation

Flat by default. The system conveys hierarchy through hairline borders (Hairline Gray, 1px) and background contrast (Paper White vs. Hairline Gray bands), not through drop shadows. Shadows exist only as a state response — a hover lift on a card, or a small resting shadow under the two elements that are meant to feel like physical objects placed on the page (the "About" photo's stat/quote badges, the floating WhatsApp button).

### Shadow Vocabulary
- **Card hover lift** (`box-shadow: 0 22px 40px -20px rgba(0,0,0,0.16)`): applied only on `:hover`, paired with a small `translateY(-6px)`. Never present at rest.
- **Badge resting shadow** (`box-shadow: 0 20px 40px -20px rgba(0,0,0,0.2)`): the two small credential/quote badges that overlap the profile photo, giving them a "physically placed" feel against an otherwise flat page.
- **Floating action shadow** (`box-shadow: 0 10px 30px -8px rgba(229,57,53,0.5)`): the fixed WhatsApp button, tinted with the accent's own color rather than a neutral shadow.

### Named Rules
**The Flat-At-Rest Rule.** Nothing has a shadow until it does something (hover) or needs to read as a physical object overlapping a photo. A static card is always flat.

## 5. Components

### Buttons
- **Shape:** sharp corners, no radius, on every button in the system.
- **Primary** (`button-primary`): solid Editorial Red background, white text, 1px red border, `13px 26px` padding. This is the booking/WhatsApp action everywhere it appears, on both light and dark backgrounds.
- **Hover / Focus:** `filter: brightness(0.88)` plus `translateY(-2px)`. The color itself never changes hue on hover, only its luminance — a controlled variation of the same red.
- **Ghost / Secondary** (`button-ghost`): transparent background, Reading Ink border and text on light surfaces (or white-on-30%-opacity border when placed on a dark hero). Hover fills solid Editorial Black with white text — a deliberate step up in contrast rather than a tint.

### Cards
- **Corner style:** sharp, 0px radius, always.
- **Background:** Paper White.
- **Border:** cards inside a grid (services, value props) share a single Hairline Gray background behind a 1px gap, so the grid itself produces the dividing hairlines rather than each card owning its own border — an intentional "shared hairline" construction, not individually boxed cards.
- **Shadow strategy:** flat at rest; see Elevation.
- **Internal padding:** `38px 32px` for service cards; smaller (`22–30px`) for denser cards (value props, testimonials).

### Navigation
- Fixed header, fully transparent over the hero with white wordmark and nav text; crossfades to a translucent white, blurred bar with Editorial Black text once the page scrolls past 40px.
- The nav wordmark pairs upright Fraunces ("Mind & Soul") with an italic Editorial Red flourish word — the one place the accent color appears in permanent UI chrome, not just a CTA.
- Active/hover state on nav links is a thin red underline that grows from 0 to full width; no background pill, no color-fill hover.
- Mobile collapses to a single hamburger; the mobile menu is a full-screen white overlay with large serif links.

### Horizontal Carousel (signature mobile pattern)
- Used for both the services grid and the photo gallery on screens ≤999px, replacing what would otherwise be a tall vertical stack.
- Single row, horizontal scroll with CSS scroll-snap, each item sized to show a peek of the next (78–84% of viewport width for service cards, 68–78% for gallery photos), bleeding past the page's own side padding so the row reaches the screen edge.
- No visible scrollbar; the peeked next-item is the only affordance that more content follows.

### Scroll Reveal
- Every card-shaped grid (value props, services, process steps, gallery, testimonials) reveals its children individually, not as one flat block: fade + rise (`opacity` and `transform`, never layout properties), staggered ~0.05-0.08s per item, capped so a 7-item grid still finishes inside ~0.4s.
- Elements whose hover state already animates `transform` (service cards lift on hover) reveal on `opacity` alone, so the entrance and the hover never fight over the same property.
- `@media (prefers-reduced-motion: reduce)` forces every `.reveal` element to its final, fully-visible state and collapses all transition/animation durations to near-zero. Nothing on the page depends on motion to become visible or usable.

## 6. Do's and Don'ts

### Do:
- **Do** keep the accent to Editorial Red (#E53935) and nothing else. Every existing color in the system already exists to be reused; don't introduce a new hue for a new feature.
- **Do** put anything meant to be read in Reading Ink (#333333) or Editorial Black, never in Quiet Gray (#9E9E9E).
- **Do** use the shared-hairline-grid construction for new card rows (background: gray, 1px gap, white cards) instead of giving every card its own border and shadow.
- **Do** convert long, repetitive mobile stacks (3+ similar cards/photos) into the horizontal scroll-snap carousel pattern rather than letting them stack vertically for multiple screens of scroll.
- **Do** treat mobile as the primary surface: verify nothing overlaps the fixed header, and that floating/absolute-positioned elements (the hero logo, the About photo's badges) get an explicit static-flow fallback below ~999px.
- **Do** give a new grid's children a staggered `.reveal` entrance (opacity + transform, ~0.05-0.08s apart) instead of letting the whole grid pop in as one block; if the element already animates `transform` on hover, drop the reveal to opacity-only rather than fighting the hover transition for the same property.

### Don't:
- **Don't** use the generic "therapist template" look: leaf/hand icons, pastel gradient washes, stock-photo-warm color grading.
- **Don't** go cold-corporate/clinical: no navy-and-white hospital palette, no sterile grid layouts.
- **Don't** add drop shadows to a card or button at rest. Shadows only appear on hover or on the two designated "physical object" badges.
- **Don't** round corners. The system is sharp-edged everywhere except the circular floating WhatsApp button and the circular practice logo mark.
- **Don't** let red cover a background, a section, or more than a button/badge-sized area.
- **Don't** animate layout properties (`max-height`, `width`, `top`) for show/hide state; the FAQ accordion uses `grid-template-rows: 0fr → 1fr` for exactly this reason.
- **Don't** ship a new transition or animation without a `prefers-reduced-motion` fallback; every existing motion in the system collapses cleanly under it.
- **Don't** fabricate content to fill a section (credentials, testimonials, phone numbers, social handles) — every fact on this page must come from the practitioner directly.
