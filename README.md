# Myntra Product Teardown: Checkout Experience

A product-management case study exploring how an Indian fashion e-commerce app can reduce checkout friction and improve customer confidence. This is an independent portfolio exercise, not affiliated with or endorsed by Myntra.

## Problem statement
Customers may drop off between product discovery, cart and payment because of unexpected costs, unclear delivery/return information, coupon friction or payment failures. The hypotheses below should be validated through research; they are not claims about Myntra's actual internal performance.

## Product goal
Make checkout more predictable and easier to complete while protecting customer trust.

## Target users
- First-time shoppers who need reassurance about delivery and returns.
- Repeat shoppers who value speed and saved preferences.
- Deal-seeking shoppers who compare discounts and final payable price.

## Proposed discovery plan
1. Map the journey: product page → size selection → bag → address → delivery option → payment → confirmation.
2. Conduct 5–8 user interviews and a short survey.
3. Review publicly available app-store feedback and competitor flows.
4. Tag observed friction by frequency, severity and confidence.
5. Validate the highest-impact issue before building.

## Opportunity hypotheses
| Hypothesis | Potential intervention | Success metric |
|---|---|---|
| Final cost appears later than expected | Show an itemised payable estimate earlier | Checkout completion rate |
| Delivery promise is hard to compare | Display delivery date and fee consistently | Address-to-payment progression |
| Size uncertainty causes hesitation | Surface fit guidance and size confidence | Size-related returns; add-to-bag rate |
| Coupon rules create friction | Explain eligibility and best applicable offer | Coupon error rate; checkout completion |

## Prioritisation (illustrative RICE)
Use Reach × Impact × Confidence ÷ Effort. Scores must be replaced with research and product data before making a real roadmap decision.

| Feature idea | Reach (1–10) | Impact (1–3) | Confidence (0–1) | Effort (person-weeks) | RICE |
|---|---:|---:|---:|---:|---:|
| Itemised price summary | 8 | 2 | 0.8 | 2 | 6.4 |
| Delivery promise clarity | 7 | 2 | 0.7 | 2 | 4.9 |
| Size confidence prompt | 5 | 3 | 0.6 | 3 | 3.0 |
| Coupon eligibility explainer | 4 | 1 | 0.8 | 1 | 3.2 |

## MVP proposal
- Keep item subtotal, delivery fee, discounts and final payable amount visible.
- Explain coupon eligibility inline.
- Show delivery estimate before payment.
- Preserve cart state when users move between checkout steps.

## Experiment design
Run an A/B test only after instrumentation and sample-size planning. Primary metric: checkout completion rate. Guardrails: payment failure rate, cancellation rate, refund/contact rate and page latency. Segment results by new vs returning users and device type. Do not declare success from conversion lift alone if guardrails worsen.

## Event instrumentation
Suggested events: `view_bag`, `begin_checkout`, `select_address`, `view_delivery_promise`, `apply_coupon`, `coupon_error`, `select_payment`, `payment_failure`, `purchase_complete`.

## Deliverables
- `docs/product_requirements.md`: lightweight PRD
- `docs/research_plan.md`: interview and validation plan
- `docs/metrics.md`: metric definitions and guardrails

## Limitations
This repository is a portfolio case study based on hypotheses. It does not use Myntra internal data, does not represent an official Myntra product proposal, and does not claim measured business impact.

## Author
Adarsh Kumar · [GitHub](https://github.com/adarshkumar9199)

## License
MIT
