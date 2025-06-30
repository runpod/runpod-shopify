- ## Minimal Shopify Theme Conversion Roadmap

### Milestone 1 – Project Audit & Planning
- [x] Clone / fork existing theme into development environment
- [x] Install Shopify CLI locally using pnpm (`pnpm add -D @shopify/cli @shopify/theme`)
- [ ] Review current templates, sections, snippets, assets and note dependencies
- [ ] Decide on brand-level design tokens (colors, fonts, spacing)
- [ ] Enable Theme Watch / Shopify CLI for live preview during development

### Milestone 2 – Global Layout Cleanup
- [x] Refactor `layout/theme.liquid` → remove unused announcements, mega-menus, etc.
- [x] Re-implement minimal header (logo + cart icon) using runpod-logo.svg
- [x] Simplify footer (copyright only)
- [x] Add fixed left sidebar navigation (ALL, HAT)
- [x] Update footer with navigation links (Policies + social placeholders)
- [x] Product card hover overlay info on desktop, info below on mobile
- [ ] Purge unused CSS/JS from `assets/` (keep only global + cart logic)

### Milestone 3 – Main (Home) Page ⇒ All Products Grid
- [x] Create `sections/main-all-products.liquid` to iterate over `collections.all.products`
- [x] Remove hero, featured-collection, newsletter and other home sections from `templates/index.json`
- [x] Update `templates/index.json` to include only the new section and minimal padding
- [x] Add basic responsive CSS grid → 3 cols desktop, 2 tablet, 1 mobile

### Milestone 4 – Product Page Simplification
- [x] Duplicate existing product section as `sections/product-minimal.liquid`
- [x] Strip to essentials: gallery (single featured image), title, vendor (optional), price, variant selector, ATC
- [x] Remove accordions / tabs / share buttons / recommended products
- [x] Update `templates/product.json` to use the new minimal section

### Milestone 5 – Cart Page Simplification
- [x] Replace existing cart section with `sections/cart-minimal.liquid`
- [x] Show line-items, quantity input, subtotal, checkout button only
- [x] Remove shipping calculators, notes, upsells, etc.

### Milestone 6 – Navigation Routing
- [x] Point store root ("/" or logo click) to `/` (index) displaying all products grid
- [ ] Hide/Remove collection list, search, blog, and other menu links

### Milestone 7 – Performance & Accessibility Pass
- [ ] Verify Lighthouse score; inline critical CSS & lazy-load images
- [ ] Check ARIA labels for buttons / images

### Milestone 8 – QA & Deployment
- [ ] Test add-to-cart, quantity edits, and checkout flow on desktop & mobile
- [ ] Cross-browser test (Safari, Chrome, Firefox)
- [ ] Push final theme to production store & publish

---
_This file will be updated as each task or milestone is completed._ 