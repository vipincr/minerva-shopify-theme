# Copilot Instructions for Minerva Lifestyle Shopify Theme

This repository customizes Shopify (built on Dawn 15.4.1) to mirror the Minerva Lifestyle brand and the primary Next.js site in ../minerva-website. Use these guardrails when assisting on this theme.

## Core Context
- Brand: Movement-born luxury; quiet power; intentional, precise tone.
- Tech: Shopify Liquid (server-rendered), minimal JS, CSS with custom properties, Shopify CLI.
- Source of truth for copy: ../minerva-website/CONTENT.md. Keep labels, headings, and UX text in sync.
- Brand/visual references: ../minerva-website/docs/Minerva-Brand-Manual-Final.md, ../minerva-website/docs/VISUALSTYLE.md, ../minerva-website/docs/Minerva-Website-Complete.md.

## Voice & Copy
- Tone: refined, confident, warm but not casual. Avoid hype, slang, or trendy language.
- Vocabulary to lean on: movement, flow, choreography, quiet power, intentional, disciplined elegance, archive, ritual, precision.
- Avoid: loud, gimmicky, discount language; "girl"; aggressive sales tone.
- When altering text, also propose updates to ../minerva-website/CONTENT.md.

## Design System (align with tokens already present)
- Colors via CSS custom properties: --color-white, --color-bg-light, --color-neutral-warm, --color-accent-gold, --color-accent-green, --color-accent-earth, --color-text-primary, --color-text-secondary, --color-text-light, --color-border, --color-success, --color-error, --color-warning.
- Typography: Tenor Sans (display), DM Sans (titles/labels), Inter (body/UI). Mirror hierarchy from the Next.js site.
- Spacing: 4px base grid; prefer multiples (4, 8, 12, 16, 24, 32, 40, 48, 64, 80...).
- Interactions: subtle fades; hover transitions 150-200ms ease; keyboard-friendly focus states.

## Shopify Theme Guidance
- Web-native first: Liquid-rendered HTML, minimal JS, progressive enhancement only when required.
- Performance: avoid render-blocking scripts and long tasks; prefer lazy loading for heavy assets; keep CLS near zero.
- Accessibility: semantic markup, focus-visible styles, sufficient contrast using brand tokens; test keyboard flows (nav, cart, checkout surface where applicable).
- Structure: prefer incremental, mergeable changes; keep compatibility with Dawn updates when possible.
- Images: use existing responsive patterns; keep alt text aligned to brand tone and CONTENT.md.

## Content Mapping
- Navigation/footer/product/care/newsletter text must follow ../minerva-website/CONTENT.md.
- Product nomenclature: The Terpsichorean (italic display), The Vienna Glide, Care Kit, etc., as defined in CONTENT.md.
- Policies and support: match Support/FAQ/Returns language from CONTENT.md.

## Workflow Notes
- Before PRs: run `shopify theme check`; provide store/editor preview links; document copy changes against CONTENT.md; update release-notes.md for customer-facing shifts.
- Do not introduce new dependencies without strong justification; keep JS small and scoped.
- If requested to add fonts/colors, use existing variables; avoid inline styles for brand-critical elements.

## What Not To Do
- No aggressive sales copy, discounts, or trend language.
- No large framework additions; avoid heavy client-side rendering.
- Do not diverge from typography and token system without brand approval.

