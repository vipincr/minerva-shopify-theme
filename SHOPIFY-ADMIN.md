# Shopify Admin Runbook (Minerva Lifestyle)

Use this checklist to configure the Shopify admin so the Minerva theme renders as designed. All steps reflect the current Shopify admin (Checkout & Accounts editor, 2025 UI).

> ⚠️ **Critical First-Time Setup**: The theme contains templates and branding defaults, but Shopify admin data (store name, pages, menus, products, collections) must be created separately. Without these, the store will show generic placeholders or 404 errors.

---

## 0) Store Settings (Required First)
Settings → Store details:
- **Store name**: `Minerva Lifestyle`
- **Store contact email**: `concierge@minervalifestyle.com`
- **Sender email**: same or branded email

This ensures the header/footer display "Minerva Lifestyle" instead of "My Store".

---

## 1) Create Products & Collections (Required)
Products → Add product:
- Create `The Vienna Glide` product with media, pricing, variants (sizes). Set handle to `the-vienna-glide`.
- Add product metafield `descriptors.subtitle` (Settings → Custom data → Products → Add definition).

Products → Collections:
- Create collection `Terpsichorean` with handle `terpsichorean`. Add `The Vienna Glide` to it.

---

## 2) Create Pages (Required)
Online Store → Pages → Add page for each:

| Page Title | Handle | Theme Template |
|------------|--------|----------------|
| Philosophy | `philosophy` | `page.philosophy` |
| Support | `support` | `page.support` |
| FAQ | `faq` | `page.faq` |
| Returns & Exchanges | `returns` | `page.returns` |
| Contact | `contact` | `page.contact` |
| Track Order | `track-order` | `page.track-order` |
| Shipping | `shipping` | `page.shipping` |
| Terms | `terms` | `page.terms` |
| Privacy | `privacy` | `page.privacy` |

After creating each page, assign its template in the right sidebar "Theme template" dropdown.

---

## 3) Navigation Menus (Required)
Online Store → Navigation:

**Main menu** (create or edit):
- Home → `/`
- Shop → `/collections/terpsichorean`
- Philosophy → `/pages/philosophy`
- Support → `/pages/support`
- Contact → `/pages/contact`

**Footer menu** (create or edit):
- Support → `/pages/support`
- FAQ → `/pages/faq`
- Returns → `/pages/returns`
- Shipping → `/pages/shipping`
- Terms → `/pages/terms`
- Privacy → `/pages/privacy`
- Contact → `/pages/contact`

---

## 4) Publish Theme
Online Store → Themes:
1. Find `minerva-shopify-theme/main` (or your theme name).
2. Click **⋯** → **Publish** (or **Actions → Publish**).
3. Keep a backup: Actions → Duplicate before publishing if desired.

---

## 5) Theme Editor (Online Store → Customize)
After pages/products exist:
- **Header**: confirm menu is set to `main-menu`; logo can be uploaded here.
- **Footer**: confirm menu is set to `footer`; newsletter heading is "Join the Archive".
- **Homepage**: 
  - Hero image-banner: upload hero image.
  - Featured product: select `The Vienna Glide`.
- **Cart template**: Featured Collection → select `Terpsichorean`.
- **404 template**: Featured Collection → select `Terpsichorean` (fallback products).

Color cues (already coded as CSS vars):
- Primary text: #000000; Accent gold: #c99214; Accent earth: #676636; Neutral warm/border: #bfbfbf; Background light: #f6f6f6.

Typography (already set in theme): Tenor Sans (display), DM Sans (titles), Inter (body). No admin action needed unless overriding in Checkout.

---

## 6) Checkout Branding (Settings → Checkout → Customize)
In the Checkout & Accounts editor (latest UI):
- Logo: upload transparent logo; placement top-left (or center if preferred).
- Background: keep white/light; optional banner image for top.
- Colors: Primary buttons/accents to black `#000000`; Accent/links to gold `#c99214`; Secondary text `#676636`; Borders `#bfbfbf`; Error `#ef4444`; Success `#22c55e`.
- Buttons: solid, squared or small radius (2–4px) to match minimal aesthetic.
- Typography: choose a clean sans (Shopify default or closest to Inter/DM Sans). Use regular/medium weights.
- Order status page: enable "Show order status page" branding to match the same styles.

---

## 7) Payments, Shipping, Taxes (quick checks)
- Payments: confirm Shopify Payments (or gateways) active; enable Apple/Google Pay for express.
- Shipping: ensure rates align with the copy (complimentary standard; express optional). If duties are charged, clarify in Shipping page copy.
- Taxes: ensure display/pricing settings match your region.

---

## 8) Responsive QA (within Theme Customizer preview)
- Check mobile (375px) and tablet (768px) breakpoints for: hero text wrap, multicolumn sections collapsing to single column, PDP gallery swipe, cart drawer/buttons, featured collection swipe.
- Confirm buttons are >=44px height and focus-visible states appear.

---

## 9) Publish Changes
- After template assignment and branding updates, click Save in the editor. For live launch, publish the theme (if not already) and re-test on a private browser/mobile device.

---

## Quick Reference: Assigning a Template (current admin)
1) Online Store → Pages → select page → right sidebar "Theme template".
2) Choose the matching template (e.g., `page.philosophy`).
3) Save.

## Quick Reference: Checkout Branding (current admin)
1) Settings → Checkout → Customize (opens Checkout & Accounts editor).
2) Use left panel "Branding" to set Logo, Colors, Typography, Buttons, Banner.
3) Save and test the Checkout preview (desktop + mobile).

---

## Troubleshooting

### Theme preview not loading / blank thumbnails
- Clear browser cache and try incognito mode.
- Ensure no browser extensions block Shopify scripts.
- Wait 1-2 minutes for GitHub sync to complete if theme was just pushed.

### 404 "Page not found" on homepage or pages
- The **pages must be created in Shopify admin** (step 2 above). The theme provides templates, not page content.
- Ensure the page handle matches exactly (e.g., `philosophy` not `Philosophy`).

### Store shows "My Store" instead of "Minerva Lifestyle"
- Update **Settings → Store details → Store name**.

### Navigation shows "Home, Catalog, Contact" (defaults)
- Edit the **main-menu** and **footer** menus in Online Store → Navigation (step 3).

### Featured product/collection shows nothing
- Ensure the product `The Vienna Glide` and collection `Terpsichorean` exist and are published.
- In Theme Editor, select them in the appropriate section settings.
