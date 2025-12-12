# Contributing

Minerva Lifestyle welcomes contributions to this Shopify theme. Please keep brand alignment, performance, and accessibility at the center of every change.

## Before contributing
- Create an issue in this repository to align on scope and acceptance criteria before opening a PR.
- If a change touches copy, update and reference the source of truth in [../minerva-website/CONTENT.md](../minerva-website/CONTENT.md).
- Stay consistent with the brand direction in [../minerva-website/docs/Minerva-Brand-Manual-Final.md](../minerva-website/docs/Minerva-Brand-Manual-Final.md) and [../minerva-website/docs/VISUALSTYLE.md](../minerva-website/docs/VISUALSTYLE.md).

## Scope
This repository is only for the Minerva Lifestyle Shopify theme. It is not a general Shopify support forum. Use issues here for bugs, enhancements, or content updates that affect this theme.

## Theme code principles
- **Web-native first:** Server-rendered Liquid, minimal JavaScript, progressive enhancement only where needed.
- **Lean, fast, reliable:** Avoid render-blocking scripts and long tasks; no DOM manipulation before user input; target zero layout shift.
- **Accessible and inclusive:** Keyboard-friendly navigation, sensible focus states, and color contrast that matches our design tokens.
- **Consistent brand expression:** Typography (Tenor Sans, DM Sans, Inter) and color tokens must mirror the Next.js site.

## Contributing code
1. Install [Shopify CLI](https://shopify.dev/docs/themes/tools/cli) and log into the Minerva store.
2. Clone the repository and create a feature branch.
3. Run locally with `shopify theme dev` (or `shopify theme serve`).
4. Lint with `shopify theme check` before opening a PR.
5. Sync any copy edits with [../minerva-website/CONTENT.md](../minerva-website/CONTENT.md) and note them in the PR.
6. Open a PR using the template; include preview links for store and editor when possible.

## Reporting a bug
- Open an issue in this repository with clear reproduction steps, expected vs. actual behavior, theme version (commit hash), and the store context used for testing.
- Include screenshots or short clips when they help clarify the problem.

## Reviewing
Maintainers review every PR for brand alignment, performance, and accessibility.

Self-check before requesting review:
- [ ] Changes follow the principles above and keep performance lean.
- [ ] `shopify theme check` passes.
- [ ] Tested on mobile and desktop storefront flows (cart, checkout, account where applicable).
- [ ] Copy and labels match [../minerva-website/CONTENT.md](../minerva-website/CONTENT.md).
- [ ] Preview links provided for reviewers.
