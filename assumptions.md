# Assumptions & Constraints

This portfolio prototype was built with the following assumptions and deliberate limits, so a reviewer knows exactly what is real, what is simulated, and what is intentionally not claimed.

## Assumptions made

- **Fictional brand.** "HerdGuard", its logo, prices, product specs and reviews are invented for demonstration. Prices (e.g. $89/20L) are placeholders, not market-researched.
- **Audience.** Modelled on the NZ dairy (primary) and poultry (secondary) hygiene market in New Zealand, using publicly available industry vocabulary.
- **Two hero products** chosen to cover both sectors: a dairy teat spray and a dual dairy/poultry disinfectant.
- **Illustrative metrics.** Every number in the measurement dashboard and the "126 reviews / 4.8★" style figures are placeholders to show *layout and method*, not results.

## Constraints (what couldn't be done in this build, and how it was handled)

| Constraint | How it was handled |
|---|---|
| No live Shopify development store was provisioned | Built a faithful static HTML/CSS storefront that mirrors a Shopify theme; captured real desktop + mobile screenshots |
| No GA4 property attached to a live store | Wrote a full GA4 **event spec + funnel plan** ready to implement, instead of claiming live data |
| No Meta Ads Manager account / no spend authorised | Produced ad **drafts and visual mock-ups** only; explicitly no publish, no spend |
| No real email list | Wrote a **sandbox** newsletter (copy + HTML) with audience, subject-line A/B and measures; not sent |
| Product efficacy can't be substantiated | Efficacy/kill claims are **omitted**; the one performance stat (teat spraying ↔ ~50% fewer new mastitis infections) is attributed to *practice* per DairyNZ, not to the product |

## What is intentionally NOT claimed

For honesty, this project does **not** claim any of the following:

- Paid campaign management or ad-spend results
- Improved sales, revenue or ROI
- Any work for, or affiliation with, a real company
- Validation by real farmers or customers
- A Shopify store delivered in a real workplace
- Personal agricultural/farming expertise
- Real GA4 results or analytics data

## Verification done

- All four store pages rendered and screenshotted at desktop (1280px) and mobile (390px) widths and visually checked.
- Ad mock-ups and dashboard rendered and visually checked.
- Every page and artifact carries a visible "portfolio prototype / fictional brand" label.
- Industry facts (teat-spray practice, emollient %, biosecurity basics) cross-checked against DairyNZ and MPI sources cited in `01-research`.
