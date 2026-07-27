# Basic SEO Checklist — HerdGuard prototype

A practical, Shopify-oriented checklist. ✅ = demonstrated in this prototype · ⬜ = documented next step (needs a live store/tools).

## On-page

- ✅ Unique, keyword-led `<title>` on every page (under ~60 chars)
- ✅ Unique meta description on every page (under ~155 chars, in customer vocabulary)
- ✅ One clear `<h1>` per page, matching search intent
- ✅ Logical heading hierarchy (H1 → H2 → H3)
- ✅ Descriptive internal links / breadcrumbs (no "click here")
- ✅ Descriptive `alt` text / `aria-label` on images and SVGs
- ✅ Mobile-responsive layout (verified via mobile screenshots)
- ✅ `lang="en-NZ"` set for regional relevance
- ⬜ Product JSON-LD structured data (name, brand, price, availability)
- ⬜ Organisation / LocalBusiness schema on home page

## Technical (needs live Shopify store)

- ⬜ Clean, readable URL handles (`/products/teat-spray-concentrate`)
- ⬜ Canonical tags to avoid duplicate collection/tag URLs
- ⬜ XML sitemap submitted to Google Search Console
- ⬜ `robots.txt` sanity check (Shopify auto-generates)
- ⬜ Core Web Vitals: compress images, lazy-load, limit apps
- ⬜ HTTPS + fast theme (Shopify handles HTTPS by default)
- ⬜ 404 handling and 301 redirects for any changed handles

## Content & off-page

- ⬜ Publish the informational "Advice" articles mapped in the keyword map
- ⬜ Internal-link each article down to the relevant product
- ⬜ Google Business Profile (if a physical/dealer presence exists)
- ⬜ Earn rural-directory / dealer listings and relevant backlinks
- ⬜ Collect and mark up genuine product reviews (ratings shown in the prototype are illustrative placeholders)

## Measurement

- ⬜ Connect Google Search Console; track impressions, clicks, position by query
- ⬜ Connect GA4 (see `06-measurement/ga4-event-plan.md`)
- ⬜ Review top queries monthly; refine titles/descriptions against real CTR
