# Product Requirements Document: Clearer Checkout

**Owner:** Adarsh Kumar  
**Status:** Portfolio proposal / hypothesis to validate  
**Product area:** Fashion e-commerce checkout

## 1. Context
Checkout is a high-intent stage. Unclear total cost, delivery expectations or offer eligibility can create uncertainty and abandonment. These are hypotheses, not verified findings about Myntra.

## 2. Problem
Shoppers need a clear, trustworthy view of what they will pay, when the order is expected and which discounts apply before they commit to payment.

## 3. Goal and non-goals
**Goal:** Reduce avoidable checkout friction and improve customer confidence.

**Non-goals:** Redesign the entire shopping app, change logistics operations, or introduce a new payment method.

## 4. Users and jobs-to-be-done
- Deal-conscious shopper: understand the actual payable price.
- Time-sensitive shopper: know the expected delivery date.
- First-time shopper: understand coupon eligibility and return-related information.

## 5. Proposed MVP requirements
1. Display item subtotal, discount, delivery fee and final payable amount together.
2. Explain why a coupon is or is not applicable.
3. Show an estimated delivery date before payment selection.
4. Keep cart and checkout selections persistent when navigating backwards.
5. Provide clear loading, error and retry states.

## 6. User stories and acceptance criteria
- As a shopper, I want to see the final payable amount before payment so there are no surprises. **Acceptance:** all price components and total are visible in the order summary.
- As a shopper, I want to understand coupon rejection. **Acceptance:** a human-readable reason and next step appear beside the coupon field.
- As a shopper, I want to know the delivery estimate. **Acceptance:** an estimate is shown for the selected address before payment.

## 7. Success metrics
**Primary:** checkout completion rate = completed purchases / checkout starts.

**Supporting:** bag-to-checkout rate, address-to-payment progression, coupon success rate, payment failure rate.

**Guardrails:** cancellations, returns, customer support contacts about pricing/delivery, page latency and accessibility defects.

## 8. Dependencies and risks
- Pricing and promotion service accuracy.
- Delivery promise data freshness.
- Analytics event consistency.
- Risk of cluttering the checkout interface.
- Experiment contamination across devices or sessions.

## 9. Rollout and validation
Start with usability tests, then a limited experiment after instrumentation and sample-size calculation. Roll out gradually only if the primary metric improves without guardrail regressions.

## 10. Open questions
- Which checkout step has the highest verified drop-off?
- Which customer segments experience the most friction?
- Are delivery estimates reliable enough to surface earlier?
- What legal and operational wording is required for returns and discounts?
