---
name: Alex Martin DDS
description: The selected photographic journal direction, documented from the homepage implementation.
colors:
  ink: "#23434f"
  sage: "#a0ae95"
  paper: "#fff"
  wash: "#eef1eb"
  rule: "#c4cec6"
  ink-hover: "#355966"
  focus: "#61764f"
  caption-muted: "#4e6558"
  disclosure-rule: "#a3b1a6"
typography:
  display:
    fontFamily: "Tenor Sans, sans-serif"
    fontSize: "clamp(50px,5.07vw,80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-.035em"
  headline:
    fontFamily: "Tenor Sans, sans-serif"
    fontSize: "clamp(34px,3.35vw,52px)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "-.025em"
  title:
    fontFamily: "Tenor Sans, sans-serif"
    fontSize: "clamp(23px,2vw,29px)"
    fontWeight: 400
    lineHeight: 1.25
    letterSpacing: "-.015em"
  body:
    fontFamily: "Archivo, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Archivo, sans-serif"
    fontSize: "13px"
    fontWeight: 400
spacing:
  inset: "clamp(24px,3.75vw,72px)"
  inset-mobile: "24px"
  text-gap: "20px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    padding: "16px 20px"
  button-primary-hover:
    backgroundColor: "{colors.ink-hover}"
  text-link:
    textColor: "{colors.ink}"
    padding: "10px 0"
  text-link-light:
    textColor: "{colors.paper}"
    padding: "10px 0"
  service-disclosure:
    backgroundColor: "{colors.wash}"
    textColor: "{colors.ink}"
    padding: "27px 0"
---

# Design System: Alex Martin DDS

## Overview

**Creative North Star: "The Scottsdale Journal"**

The Scottsdale Journal uses white photo-paper space, the original navy and sage identity, and rectangular photography to introduce the real practice. Tenor Sans gives headings an open, measured character; Archivo keeps supporting copy direct and readable. Thin rules and changes in background organize the page without ornamental containers.

Bryan selected this direction on the code-first direction board. This document captures the implemented homepage system; the completed homepage is still awaiting review and approval. The first-surface composition remains in `.impeccable/surfaces/src-pages-index-astro.md`. This record does not authorize additional pages or publication.

**Key Characteristics:**

- Original logo and navy/sage brand identity.
- Real practice photographs with rectangular crops and compact captions.
- Open display typography, readable body copy, and restrained rules.
- Flat surfaces, visible keyboard focus, and minimal motion.

## Colors

The original blue-green ink and muted sage sit on white photo-paper, with a pale green wash for quieter reading areas. Frontmatter values are normative and preserve the source CSS notation. The sidecar’s tonal ramps are derived panel previews, not additional implementation tokens or approved palette choices.

### Primary

- **Practice Ink** (`ink`): primary text, filled call actions, and the dark care band.
- **Ink Hover** (`ink-hover`): hover state for the filled call button and mobile phone bar.

### Secondary

- **Brand Sage** (`sage`): the original logo accent, text-selection background, light-link rule, and mobile-call focus ring. It is not used as body text on white.
- **Focus Green** (`focus`): the default high-visibility keyboard outline.

### Neutral

- **Photo Paper** (`paper`): the main canvas, masthead, photo captions, and text on dark surfaces.
- **Quiet Wash** (`wash`): service-section background.
- **Soft Rule** (`rule`): masthead, mobile menu, and footer boundaries.
- **Muted Caption** (`caption-muted`): secondary photograph-note text.
- **Disclosure Rule** (`disclosure-rule`): service-list separators.

**The Brand Continuity Rule.** Preserve the original logo and its ink/sage relationship; the supporting neutrals serve the selected identity.

## Typography

**Display Font:** Tenor Sans, with sans-serif fallback. **Body Font:** Archivo, with sans-serif fallback. Fontsource provides local Latin font files. Tenor Sans uses its regular weight; Archivo loads regular, medium, and semibold, with medium used for the mobile phone number.

The display face supplies spacious, rounded letterforms without rounded containers. Body copy stays matter-of-fact. There is no separate mono or decorative label face.

### Hierarchy

- **Display:** the main heading uses the frontmatter display role. At widths up to (1100px), it uses `clamp(48px,5.4vw,65px)`; up to (760px), `clamp(36px,8.8vw,60px)` with line-height (1.08); up to (360px), (33px).
- **Headline:** section headings use the frontmatter headline role. Compact band headings and mobile sections have context-specific overrides in the stylesheet.
- **Title:** service titles use the frontmatter title role; mobile titles use (24px), reducing to (22px) at the narrowest breakpoint.
- **Body:** most prose uses the body role, reducing to (16px) on mobile. Text measures vary with purpose: practice copy is limited to (54ch), service details to (55ch), and compact introductions to approximately (33–35ch).
- **Label:** the caption rail uses the label role; mobile photo captions reduce to (11px). Navigation uses (15px), then (14px) below the tablet breakpoint.

**The Readable Hierarchy Rule.** Keep display type for headings and the prominent phone number; use Archivo for navigation, body copy, captions, and ordinary actions.

## Layout

The canvas is fluid with a shared inline inset. Above (1700px), the body is centered with a maximum width of (1920px). The base desktop header is (100px) tall. Major content sections use generous vertical space: practice (110px), services (85px/100px), and visit (100px). These are observed section values, not a fabricated universal spacing scale.

Desktop sections use unequal columns: practice pairs a portrait up to (400px) with copy up to (580px), services uses (1fr/1.35fr), and visit uses (1fr/1.2fr). The selected homepage photo sequence has three unequal adjoining panels; its exact composition belongs to the surface brief rather than every future screen.

At (1100px) and below, navigation gaps and section spacing tighten. At (760px) and below, content becomes a vertical sequence, the header becomes (82px), and an explicit menu control reveals stacked navigation. The inset becomes fixed. The photo sequence retains one broad image above two smaller adjoining views. A fixed phone bar has a minimum height of (65px), bottom safe-area padding, and corresponding page bottom clearance. The (360px) breakpoint reduces logo, type, and image sizes.

Anchor scrolling reserves (120px) above targets on desktop and (92px) on mobile. Service disclosures add their own scroll margin. Preserve these clearances when changing sticky navigation.

## Elevation & Depth

The implementation has no box shadows, gradients, blur, or simulated material depth. White, wash, and ink backgrounds establish sections; thin rules establish boundaries. The sticky header and mobile call bar use stacking order for function, not visual elevation. Keep this flat character when extending existing components.

Motion is limited to smooth anchor scrolling and a short service-icon rotation. Reduced-motion preferences disable smooth scrolling and the icon transition.

## Shapes

Photographs, buttons, caption tabs, and section surfaces have square corners. Thin horizontal rules carry structure. There is no reusable rounded-card vocabulary and no radius scale in the code. SVG arrows and plus signs use open strokes with round line caps and joins; their strokes do not change the rectangular surface language.

## Components

### Buttons

Filled call actions are direct rectangular links, using ink with paper text, a minimum height of (50px), and the primary-button padding in frontmatter. Hover changes to the ink-hover color and suppresses the ordinary link underline. Keyboard focus uses an outline offset of (4px). No disabled, loading, or submission state exists because these are telephone links.

### Text Links

Editorial actions pair text with an inline arrow and a bottom rule. They have a minimum height of (44px) and a gap of (20px). Hover thickens the rule; ordinary text links elsewhere use an underline. Light links inherit white text over ink, use a sage rule, and receive a white focus outline. The prominent telephone link uses the display face without an arrow.

### Navigation

The sticky white masthead contains the original logo, three section anchors, and a phone action. Desktop navigation is horizontal. Mobile navigation is initially hidden and controlled by a real button exposing `aria-expanded` and `aria-controls`. Choosing a link, pressing Escape, clicking outside the header, or crossing the desktop breakpoint closes the menu. Escape returns focus to its control. The mobile menu has a bottom rule and no overlay or shadow.

### Service Disclosures

Native `details` and `summary` elements form a ruled list on the wash background. Summaries use display titles, generous block padding, and an inline plus icon. Opening a row reveals body copy and a telephone link; the plus rotates to (45deg) over (.25s ease-out), with no transition in reduced-motion mode. Native disclosure semantics and keyboard behavior remain intact.

### Photography And Captions

Real office images use explicit dimensions and controlled `object-fit: cover` crops. The adjoining photo sequence places compact white caption tabs against each image's lower edge. Portrait and location images use captions beneath the image. The location caption uses Archivo at (14px) on desktop and (13px) on mobile, keeping it subordinate to the section heading. Content images are not decorative substitutes for evidence; their alternatives describe the actual person, room, or location.

### Mobile Call Bar

A fixed ink bar at the viewport bottom presents a visit prompt and the verified phone number. It shares the filled-button hover color, has a sage inset focus outline, and accounts for the device safe area. It appears only at the mobile breakpoint.

No input, form, chip, card grid, tooltip, or dialog component is implemented. Do not invent these in documentation.

## Do's and Don'ts

### Do:

- Do preserve the original logo and the selected navy/sage identity.
- Do use actual practice imagery with meaningful alternatives and explicit image dimensions.
- Do capitalize the first letter of each word in visible titles, headings, and subheadings while preserving proper names and acronyms.
- Do preserve sticky navigation, visible keyboard focus, reduced-motion behavior, and responsive phone access.
- Do keep contact actions honest: use verified phone and contact anchors until scheduling is verified.

### Don't:

- Don't replace the chosen direction with generic rounded cards, shadows, or decorative gradients.
- Don't add invented reviews, credentials, results, or business facts.
- Don't add discounts, specials, coupon copy, or emergency-led hero headlines.
- Don't add forms that appear connected without a working destination.
- Don't treat direction selection as completed-homepage approval or permission to publish.
