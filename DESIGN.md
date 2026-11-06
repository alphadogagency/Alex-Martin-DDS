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
    fontSize: "clamp(42px,4.1vw,67px)"
    fontWeight: 400
    lineHeight: 1.06
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
    borderRadius: "8px"
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

## Approved Hosted Preview Revision — November 6, 2026

**Creative North Star: The Scottsdale Journal.** Retain the original logo, ink/sage/white palette, Tenor Sans display typography and Archivo body text. Real courtyard, doctor, waiting-room and reception photographs tell the story of this Scottsdale practice. Editorial rules and unequal adjoining compositions organize the page.

Bryan approved this whole-homepage refinement on November 6 and explicitly requested committing and pushing it to update the existing hosted preview. This supersedes the earlier local-only boundary. Approval of this preview does not authorize additional pages or production-domain launch.

## Colors And Typography

Frontmatter names the actual color and typography roles. Ink #23434f carries text, controls and the closing contact panel; sage #a0ae95 remains the original brand accent. White and wash #eef1eb alternate reading surfaces. No gradients, shadows or decorative replacement palette. White on ink and ink on white/wash carry body text; sage is not body text on white.

Tenor Sans headings use regular weight and balanced wrapping except the deliberately composed hero. Archivo body text is 17px desktop and 16px mobile, with line-height 1.65 (hero 1.55). Headings use the documented fluid roles. Context-specific exceptions: care band clamp(26px,2.2vw,36px), mobile29px; mobile doctor/services35px and visit38px; phone clamp(29px,2.5vw,38px), mobile32px/narrow28px. Header navigation15px (14px tablet), captions13px (11px hero mobile), mobile bar13px (12px narrow). These supporting sizes are intentional, not additional headline roles.

## Composition And Spacing

Shared inset clamp(24px,3.75vw,72px), mobile24px; body capped at1920px on wide displays. Sticky white header100px desktop,82px mobile. Anchor clearance120px desktop/92px mobile. Footer retains a restrained logo, practice descriptor, phone and copyright.

- Hero: one original courtyard photograph, height clamp(500px,40vw,650px), with a white lower-right editorial panel (49% width, capped650px). Headline/copy/Plan Your Visit are grouped. A compact factual caption rail follows. Tablet uses500px height and a53% editorial panel. Mobile reorders headline,250px photograph, copy and action; narrow image210px.
- Care introduction: a compact three-column ruled strip on white. At tablet the action sits under the body column; mobile stacks naturally. This replaces the full-width dark band, reserving ink for the final invitation.
- Doctor: copy left and high-resolution original portrait right, generous but bounded gap and88px vertical padding. Portrait uses a4/4.8 crop with the face retained. One pale-sage offset backplate adds depth without a shadow and is included in the layout footprint. Mobile copy precedes a square portrait, with56px section padding.
- Services: wash background, intro/real waiting-room photo left and ruled disclosure list right;76px vertical padding. The first family-care row is initially open to reveal how the list works. Other rows stay independent native disclosures. Mobile places the image before the list with54px section padding.
- Contact: rounded adjoining reception photo and ink information panel, inset from page edges with80px desktop margins. Phone, address and directions remain readable and actionable. Mobile stacks a240px photo above the panel with52px outer vertical margins.

## Shapes And Controls

Media and the contact composition use24px radii (20px mobile outer hero/contact); filled buttons8px. The white editorial panel has one softened upper-left corner. Flat rules still structure the page; there is no repeated rounded-card grid.

Primary links are ink buttons with white text and at least50px height. Text links use an arrow, bottom rule and minimum44px height. Visible focus outlines remain; dark-panel focus is white. Phone actions use the verified tel destination. Plan Your Visit and Plan A Visit point to the actual contact section, not a simulated booking form.

Mobile menu exposes aria-expanded/aria-controls and closes on link selection, Escape, outside click and desktop breakpoint changes. Escape restores focus to Menu. The fixed phone bar retains its65px clearance and safe-area padding. Native service disclosures preserve keyboard semantics and visible focus; the plus rotates45deg when open.

## Motion And Accessibility

Five selected below-fold groups (doctor copy, doctor portrait, services introduction, service list and reception photograph) fade once from opacity0 to1 over650ms with cubic-bezier(.2,.7,.3,1) easing as they enter view. This replaces scale-only photo settling. No layout or spatial animation is added. Groups already visible on arrival and the hero/navigation/contact controls remain immediately visible. Default HTML/CSS never hides content: observation starts the short animation only when a group enters view. Unsupported or failed enhancement leaves content visible. Focus and anchor navigation cancel/skip a group’s fade immediately. Controls have180ms background/arrow feedback, disclosures250ms icon rotation, and anchors smooth scrolling. No animation dependency was added. Reduced-motion at load prevents observer setup; preference changes disconnect it and cancel running animations, restoring opacity1 immediately. CSS disables smooth scrolling and decorative transitions under reduced motion.

All images have meaningful alternatives and explicit intrinsic dimensions; lower images are lazy loaded, hero high priority with960/1440 responsive sources. Fonts are local. Titles capitalize each word while preserving proper names/acronyms. No invented proof, discounts, emergency hero, new pages or fake-working forms.

## Verification And Stage

Built with the existing Astro static configuration. Codex browser review covers1440×1000,1280×800,390×844 and320×740, section navigation, native disclosure keyboard activation, mobile menu/Escape, image/font loading, sticky header and overflow. Independent screenshot-only review:8.6/10, no required design fixes. Source detector reports advisory font-ramp differences only; actual sizes are described above. November 6 fade release: actual opacity progression measured in Codex at1440×900 and390×844, with focused/anchor-targeted groups restored immediately. Controlled local browser fixtures using the built script verified reduced-motion at load and during animation, no-JavaScript visibility and observer-setup failure. These inject test preferences rather than changing the OS setting. Source detector for this scoped script change found no issues. Physical devices and a full cross-browser audit remain outside this pass.

Keep staging noindex meta, robots and headers. Bryan approved this version for the hosted review preview. Client approval, further-page instruction and production-domain launch remain separate steps.
