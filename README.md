# Minerva Lifestyle Shopify Theme

Custom Shopify theme for Minerva Lifestyle, built on Dawn 15.4.1 and tailored to our movement-born brand. This repository is the Shopify counterpart to the Next.js site in [minerva-website](../minerva-website/README.md). Use it for Shopify-managed surfaces (checkout, account, notifications) while mirroring the design, copy, and tone defined in the main site.

## References
- Brand and UX direction: [minerva-website/docs/Minerva-Brand-Manual-Final.md](../minerva-website/docs/Minerva-Brand-Manual-Final.md), [minerva-website/docs/VISUALSTYLE.md](../minerva-website/docs/VISUALSTYLE.md), [minerva-website/docs/Minerva-Website-Complete.md](../minerva-website/docs/Minerva-Website-Complete.md).
- Source of truth for copy: [minerva-website/CONTENT.md](../minerva-website/CONTENT.md). If you update any text or labels, sync the change back to this file.
- Technical architecture: [minerva-website/docs/Minerva-Fullstack-Spec.md](../minerva-website/docs/Minerva-Fullstack-Spec.md) and [minerva-website/docs/Minerva-Implementation-Roadmap.md](../minerva-website/docs/Minerva-Implementation-Roadmap.md).

## Getting started
1. Install [Shopify CLI](https://shopify.dev/docs/themes/tools/cli) and log into the Minerva store: `shopify login --store <store-domain>`.
2. From the repository root, run a local preview: `shopify theme dev` (or `shopify theme serve`).
3. Run linting before opening a PR: `shopify theme check`.
4. Keep copy, typography, and tone aligned with the references above. For any brand or content changes, update both the theme and [minerva-website/CONTENT.md](../minerva-website/CONTENT.md).

## Design and content alignment
- Color system (use CSS custom properties already defined in the theme): `--color-white`, `--color-bg-light`, `--color-neutral-warm`, `--color-accent-gold`, `--color-accent-green`, `--color-accent-earth`, `--color-text-primary`, `--color-text-secondary`, `--color-text-light`, `--color-border`, `--color-success`, `--color-error`, `--color-warning`.
- Typography: Tenor Sans for display headlines, DM Sans for titles/labels, Inter for body and UI text. Match the hierarchy used in the Next.js site.
- Voice: refined, intentional, movement-led. Avoid loud or trendy language; emphasize quiet power, precision, and care.
- Product and policy copy must stay consistent with [minerva-website/CONTENT.md](../minerva-website/CONTENT.md) and Shopify product data.

## Development guidelines
- Stay web-native and lean (Dawn defaults apply): server-rendered Liquid first, minimal JavaScript, progressive enhancement only where needed.
- Keep accessibility and performance in mind: no long tasks, no render-blocking scripts, keyboard-friendly navigation.
- Structure changes so they can be merged upstream if we choose to rebase onto newer Dawn versions. Avoid large-scale rewrites unless required by the brand brief.

## Releases
- Track notable changes in [release-notes.md](release-notes.md) with date, summary, and theme version.
- Keep a backup of the currently published theme in Shopify before deploying updates.

## License

This project remains under the upstream Dawn license. See [LICENSE.md](LICENSE.md) for details.
