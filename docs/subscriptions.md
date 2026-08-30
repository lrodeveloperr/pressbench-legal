---
layout: default
title: Advertising and Purchases
nav_title: Purchases
permalink: /subscriptions/
---

# Advertising and Purchases

**Effective: 30 August 2026**

## iOS model

The current PressBench iOS model is implemented as follows:

- Free use includes a fixed Google banner and up to five successfully completed and saved press runs.
- A failed, canceled or unsaved run does not use the free allowance.
- Deleting a run or clearing local operational data does not restore free uses.
- PressBench Pro is an auto-renewable one-month subscription. In the US storefront, the configured price is **US$9.99 per month**.
- While active, Pro provides unlimited press runs, removes the banner and unlocks PDF/XLSX production reports.
- Machines, setups, search, corrections, deletion and access to existing records are not separately capped.
- Existing records remain readable if a subscription expires.
- Any former verified iOS lifetime purchase remains honored and does not become a subscription.

The App shows the localized price supplied by Apple. The App Store purchase sheet is authoritative for the price, currency, billing period, taxes and any regional terms that apply to a transaction. The subscription automatically renews unless canceled at least 24 hours before the end of the current period. Apple charges the user’s Apple Account and manages renewal, cancellation, billing, refunds and subscription status. Users can manage or cancel through their Apple Account subscription settings and can use **Restore purchase** in PressBench.

The subscription becomes available only after the product is active in App Store Connect for the applicable storefront. This page does not override the availability or terms shown by Apple.

## iOS advertising status

The current iOS code uses PressBench’s production AdMob app and 320 × 50 banner identifiers. It requests production banner ads when the consent gate permits an ad request and an ad is available. Ad personalization is disabled in the SDK configuration and the maximum ad content rating is set to General.

The iOS TestFlight build includes Google UMP 3.1.0. It requests current consent information, presents a required form when available, and sends an ad request only when UMP reports that ads may be requested. A **Privacy Choices** entry is shown in the App when Google reports that a privacy-options form is required.

The in-app **Support** route may be used to report an inappropriate advertisement. Include a screenshot if safe to do so, but redact production or customer information.

## Android status

The reviewed Android closed-test build has no Google Play Billing dependency, paid product, purchase interface or subscription controls. Its Google banners use official test identifiers. The iOS subscription described above does not create an Android entitlement.

Do not send payment-card details, StoreKit transaction data or purchase tokens by email.

## Contact

Email: [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Purchases%20or%20Advertising)

Subject: **PressBench Purchases or Advertising**
