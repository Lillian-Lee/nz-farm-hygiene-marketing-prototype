# GA4 Event & Measurement Plan — HerdGuard prototype

> Portfolio prototype. GA4 could not be attached to a live store in this build, so this is a **measurement *plan*** (event spec + funnel) ready to implement on a real Shopify + GA4 setup. No live analytics data is claimed.

## 1. Measurement principle: separate awareness, engagement and sales

A core principle of this plan: **don't collapse three different things into one number.** Traffic is not interest; interest is not intent; intent is not a sale. Each layer gets its own events and its own success measure.

| Layer | Question it answers | Example measures |
|---|---|---|
| **Awareness** | Did we reach the right people cheaply? | Sessions, new users, reach/impressions (Meta), traffic by source/medium |
| **Engagement** | Did they show real interest? | Product views, scroll/route depth, `view_item`, `add_to_cart`, email CTR |
| **Sales / demand** | Did interest convert to intent/purchase? | `begin_checkout`, `purchase`, stockist `generate_lead` (enquiry) |

## 2. GA4 event specification

Using GA4 **recommended ecommerce events** where possible (so standard reports and the funnel exploration work out of the box).

| Event | Trigger | Key parameters | Layer |
|---|---|---|---|
| `page_view` | Any page load (automatic) | `page_location`, `page_title`, source/medium | Awareness |
| `view_item_list` | Collection page viewed | `item_list_name` = "Farm hygiene" | Engagement |
| `select_item` | Product card clicked | `item_id`, `item_name` | Engagement |
| `view_item` | Product page viewed | `item_id`, `item_name`, `price`, `item_category` | Engagement |
| `add_to_cart` | "Add to cart" clicked | `item_id`, `quantity`, `value`, `currency`=NZD | Engagement→Intent |
| `begin_checkout` | Checkout started | `value`, `currency`, cart items | Intent |
| `purchase` | Order completed | `transaction_id`, `value`, `tax`, `shipping`, items | Sales |
| `generate_lead` | Stockist form submitted | `form_name` = "become_a_stockist" | Sales (B2B) |
| `newsletter_signup` | Email captured | `method` = footer/band | Engagement |
| `view_promotion` / `select_promotion` | "Free delivery over $150" banner | `promotion_name` | Engagement |

**Custom dimensions to register:** `item_category` (dairy vs poultry), `product_format` (concentrate vs RTU), traffic `campaign` (UTM).

## 3. Conversion funnel (GA4 Funnel Exploration)

```
 100%  Session / page_view            ← Awareness (paid + organic + email)
   │
   ▼   view_item_list  (collection)   ← Engagement
   │
   ▼   view_item       (product)      ← Engagement
   │
   ▼   add_to_cart                     ← Intent
   │
   ▼   begin_checkout                  ← Intent
   │
   ▼   purchase   +   generate_lead    ← Sales / demand
```

Watch the **biggest drop-off step** — that's where the next optimisation goes (e.g. if `view_item → add_to_cart` leaks, test price framing, delivery messaging or CTA).

## 4. Campaign attribution (UTMs)

Tag every paid/email/social link so GA4 can split performance:

- Meta ad A: `?utm_source=facebook&utm_medium=paid_social&utm_campaign=launch&utm_content=variant_a_problem`
- Meta ad B: `...&utm_content=variant_b_routine`
- Newsletter: `?utm_source=newsletter&utm_medium=email&utm_campaign=launch`
- Organic social: `utm_medium=social`

## 5. Reporting

- **Weekly:** traffic by source/medium, funnel step conversion, top products viewed, email CTR, Meta cost-per-result. 
- **One-page dashboard:** see `measurement-dashboard.html` / `.png` — a mock of the summary view (awareness → engagement → sales) with **clearly-labelled illustrative numbers**, not real results.

## 6. If traffic produces no enquiries

Find the funnel step that leaks (GA4 funnel exploration), then test that step — one variable at a time: landing-page relevance/message match, delivery-cost framing, CTA clarity, mobile speed, audience/message fit, and whether the *offer* (not just the ad) is the problem.
