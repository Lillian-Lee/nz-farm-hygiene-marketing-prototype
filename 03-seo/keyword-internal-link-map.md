# Keyword & Internal-Link Map — HerdGuard prototype

> Portfolio prototype. Search volumes are **not** claimed — this map shows the intent grouping and internal-linking logic a real keyword tool (e.g. Google Keyword Planner, Ahrefs) would later be used to size.

## 1. Keyword intent groups

**Transactional (bottom of funnel) — map to product pages**

| Keyword theme | Target page | Intent |
|---|---|---|
| teat spray NZ / buy teat spray | Teat spray product | Ready to buy |
| emollient teat spray / post-milking teat spray | Teat spray product | Comparing products |
| teat spray concentrate / 20L teat spray | Teat spray product | Size/format decision |
| farm disinfectant NZ / footbath disinfectant | Disinfectant product | Ready to buy |
| poultry shed disinfectant / biosecurity disinfectant | Disinfectant product | Comparing products |

**Commercial (mid funnel) — map to collection**

| Keyword theme | Target page |
|---|---|
| farm hygiene products NZ | Collection |
| dairy hygiene products | Collection |
| poultry biosecurity products | Collection |

**Informational (top of funnel) — map to Advice content (future blog)**

| Keyword theme | Suggested article | Links down to |
|---|---|---|
| how to teat spray correctly / teat spray coverage | "The 4-point teat-spray routine" | Teat spray product |
| teat spray emollient percentage | "How much emollient does teat spray need?" | Teat spray product |
| farm footbath setup / biosecurity footbath | "Setting up footbaths that actually work" | Disinfectant product |
| cleaning vs disinfecting sheds | "Clean first, then disinfect: why order matters" | Disinfectant product |

## 2. Internal-link map (implemented in prototype)

```
                 ┌────────────────────────────┐
                 │           HOME              │
                 │  (brand + both products)    │
                 └───────────┬────────────────┘
             ┌───────────────┼────────────────┐
             ▼               ▼                 ▼
      ┌────────────┐  ┌──────────────┐  ┌──────────────┐
      │ COLLECTION │  │ Teat spray   │  │ Disinfectant │
      │ (hub)      │◄─┤ product      │  │ product      │
      └─────┬──────┘  └──────┬───────┘  └──────┬───────┘
            │  cross-links   │                 │
            └────────────────┴─────────────────┘
              (collection ↔ both products,
               products link back to collection
               via breadcrumb + footer)
```

Link rules applied in the prototype:

- Every page's breadcrumb links Home → Collection → Product.
- Home features both products and links to the collection.
- Collection lists both products.
- Footer on every page links to Home, Collection and both products (site-wide equity distribution).
- Advice section anchors (`index.html#advice`) sit ready to become the informational hub that links *down* to the money pages.

## 3. Anchor-text guidance

Use descriptive, keyword-relevant anchors (e.g. "emollient teat spray", "shed & footbath disinfectant") rather than "click here". Keep exact-match anchors natural and varied to avoid over-optimisation.
