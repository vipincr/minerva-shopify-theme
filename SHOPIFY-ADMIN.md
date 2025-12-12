# Shopify Admin Runbook (Minerva Lifestyle)

Use this checklist to configure the Shopify admin so the Minerva theme renders as designed. All steps reflect the current Shopify admin (Checkout & Accounts editor, 2025 UI).

## Prerequisites
- Theme uploaded: `Minerva Lifestyle` (Dawn 15.4.1 based). Keep an unpublished duplicate for safety.
- Products/collections exist: `Terpsichorean` collection and `The Vienna Glide` product (handle should match storefront links). Add product media (hero, detail, care kit) and alt text.
- Assets: brand logo (transparent), checkout banner (optional), hero images for philosophy/support if desired.

## 1) Publish and Preview Theme
1. Online Store → Themes → Actions → Preview `Minerva Lifestyle`. When ready, **Publish**.
2. Keep a backup: Actions → Duplicate.

## 2) Assign Templates to Pages
Create pages first (Online Store → Pages), then apply templates (right sidebar “Theme template”).
- Philosophy → template: `page.philosophy`.
- Support → `page.support`.
- FAQ → `page.faq`.
- Returns & Exchanges → `page.returns`.
- Contact → `page.contact`.
- Track Order → `page.track-order`.
- Shipping → `page.shipping`.
- Terms → `page.terms`.
- Privacy → `page.privacy`.

## 3) Navigation
Online Store → Navigation.
- Main menu links:
  - Shop → `/collections/terpsichorean`
  - Philosophy → `/pages/philosophy`
  - Support → `/pages/support`
  - FAQ → `/pages/faq`
  - Contact → `/pages/contact`
- Footer menu: add Support, Returns (`/pages/returns`), Shipping (`/pages/shipping`), Terms, Privacy, Contact.

## 4) Collection & Product Defaults
- Collections: set `Terpsichorean` as featured where needed. Add collection image if desired.
- Product metafields: add `descriptors.subtitle` (Namespace `descriptors`, Key `subtitle`, type: Single line text) and populate for PDP subtitle. PDP collapsible tabs can use inline content or link to pages via theme editor.

## 5) Theme Editor (Online Store → Customize)
General:
- Header/Footer: confirm menus set to Main/Footer; enable announcement if needed.
- Homepage: ensure featured product block points to `The Vienna Glide`; set hero/section images; adjust color schemes (scheme-1/2/3 align to brand tokens).
- Cart template: set Featured Collection to `Terpsichorean` (Quiet pairings). Enable swipe on mobile is already configured.
- Newsletter/signup blocks: wire to your email app if required (or leave default for Shopify email capture).

Color cues (already coded as CSS vars):
- Primary text: #000000; Accent gold: #c99214; Accent earth: #676636; Neutral warm/border: #bfbfbf; Background light: #f6f6f6.

Typography (already set in theme): Tenor Sans (display), DM Sans (titles), Inter (body). No admin action needed unless overriding in Checkout.

## 6) Checkout Branding (Settings → Checkout → Customize)
In the Checkout & Accounts editor (latest UI):
- Logo: upload transparent logo; placement top-left (or center if preferred).
- Background: keep white/light; optional banner image for top.
- Colors: Primary buttons/accents to black `#000000`; Accent/links to gold `#c99214`; Secondary text `#676636`; Borders `#bfbfbf`; Error `#ef4444`; Success `#22c55e`.
- Buttons: solid, squared or small radius (2–4px) to match minimal aesthetic.
- Typography: choose a clean sans (Shopify default or closest to Inter/DM Sans). Use regular/medium weights.
- Order status page: enable “Show order status page” branding to match the same styles.

## 7) Payments, Shipping, Taxes (quick checks)
- Payments: confirm Shopify Payments (or gateways) active; enable Apple/Google Pay for express.
- Shipping: ensure rates align with the copy (complimentary standard; express optional). If duties are charged, clarify in Shipping page copy.
- Taxes: ensure display/pricing settings match your region.

## 8) Responsive QA (within Theme Customizer preview)
- Check mobile (375px) and tablet (768px) breakpoints for: hero text wrap, multicolumn sections collapsing to single column, PDP gallery swipe, cart drawer/buttons, featured collection swipe.
- Confirm buttons are >=44px height and focus-visible states appear.

## 9) Publish Changes
- After template assignment and branding updates, click Save in the editor. For live launch, publish the theme (if not already) and re-test on a private browser/mobile device.

## Quick Reference: Assigning a Template (current admin)
1) Online Store → Pages → select page → right sidebar “Theme template”.
2) Choose the matching template (e.g., `page.philosophy`).
3) Save.

## Quick Reference: Checkout Branding (current admin)
1) Settings → Checkout → Customize (opens Checkout & Accounts editor).
2) Use left panel “Branding” to set Logo, Colors, Typography, Buttons, Banner.
3) Save and test the Checkout preview (desktop + mobile).
