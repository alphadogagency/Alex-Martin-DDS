# Alex Martin, DDS

Initial Scottsdale homepage built with Astro. The selected design direction is **The Scottsdale Journal**: real practice photography, an editorial layout, and the existing blue-green/sage brand identity.

## Development

```sh
npm ci
npm run dev
```

The scripts use the project-local Node runtime supplied by the `node` development dependency. This avoids changing the system installation. The current runtime is Node 22.23.4.

## Build And Preview

```sh
npm run build
npm run preview -- --port 4397
```

Static output is generated in `dist/`. Use the URL printed by the preview command.

Cloudflare Pages build settings:

- Build command: `npm run build`
- Output directory: `dist`
- Node version: `22.23.4`
- Install development dependencies, including the project-local Node runtime.

## Project Structure

- `src/pages/index.astro`: homepage and navigation behavior
- `src/styles/global.css`: responsive styles
- `public/images/`: original practice logo and sourced practice photographs
- `DESIGN.md`: implemented design system
- `.impeccable/design.json`: component/design documentation

Image provenance is recorded alongside the WebP assets. Fonts are self-hosted through Fontsource packages.

## Current Stage

The homepage is ready for review. This repository is not a production deployment. Additional pages and publication follow homepage approval and separate authorization.

The preview deliberately uses `noindex` in HTML, `public/robots.txt`, and `public/_headers`. Reconcile all three during an authorized launch. The current appointment actions are telephone links; there is no appointment form or booking backend.

Before launch, confirm practice details and approved source assets, complete the remaining site content and integrations, and perform the full launch checks. The implementation must retain the original logo, sticky header, title-style heading capitalization, and accessible mobile navigation. Do not add discounts, specials, fabricated reviews, credentials, or emergency-led hero copy.

## Verification

The production build passes. Desktop, tablet and phone viewport checks covered navigation, keyboard service disclosures, sticky behavior, images and horizontal overflow. Real-device and full production-launch checks remain outstanding.
