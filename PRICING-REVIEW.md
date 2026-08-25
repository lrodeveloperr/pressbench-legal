# PressBench Pricing Plan

**Reviewed:** 25 August 2026
**Current closed-test baseline:** `1.0.0-closed-v16-native` (version code 1403)

## Current build

The current Android closed-test build is free. It has no Google Play Billing dependency, paid product, purchase screen, subscription controls or entitlement. All implemented features are available without payment. Its Google banner ads use official test identifiers and generate no revenue.

## Future internal plan

The working reference price for a future Android ad-free subscription is **US$9.99 per month**. This is an internal planning value only—not an offer, displayed price or entitlement in the current build.

Before offering it:

1. Implement and test current Google Play Billing requirements and a durable entitlement lifecycle.
2. Create and activate the subscription/base plan in Play Console.
3. Show the user's localized Play-provided price and billing period; do not hard-code a worldwide storefront price.
4. Clearly explain that the recurring benefit is removal of advertising while entitlement is active.
5. Implement purchase acknowledgement, restoration, grace/hold/expiry/refund handling and subscription management access.
6. Update the privacy policy, terms, Data Safety/store declarations, listing and regional merchant/tax disclosures before distribution.

Until all conditions are complete, the App and listing must not claim that an ad-free purchase or subscription is available.
