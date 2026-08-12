# PressBench Pricing Review

**Logic baseline:** PressBench v0.21.2, reviewed 12 August 2026.  
**Decision status:** Commercial structure locked for the current release plan.

## Locked structure

| Platform | Free allowance | Paid product | US base price | Geographic pricing |
|---|---|---|---:|---|
| iOS | 3 saved setups and 10 saved batches | One-time non-consumable unlock | US$4.99 | Yes |
| Android | 3 saved setups and 10 saved batches | One-time non-consumable unlock | US$4.99 | Yes |

There is no subscription, automatic renewal, free-trial conversion, or advertising on either platform.

Exact product identifiers:

- iOS: **pressbench_unlimited_lifetime_ios**
- Android: **pressbench_unlimited_lifetime_android**

The store-displayed localized price, currency, and tax treatment control the transaction.

## Paid capabilities and limits

Paid access removes the Free Tier’s 3-setup and 10-batch commercial creation gates and enables paid analytics and PDF/XLSX reports. JSON backup and CSV export remain available without paid access.

Paid access remains subject to:

- up to 1,000 saved setups;
- up to 1,000 saved batches;
- 8 MB primary operational-data storage;
- 2 MB compatibility-mode storage;
- 1 MB per record;
- 12,000 detailed XLSX rows;
- available device storage and supported operating systems; and
- future App and store availability.

Consumer-facing copy should use **“one-time paid unlock”** or **“remove the Free Tier limits”** rather than “unlimited” or “lifetime.” The internal product identifiers are not a promise of uncapped records or perpetual support.

## Platform separation

PressBench has no cross-platform account. An Apple purchase does not unlock Android and a Google Play purchase does not unlock iOS. Restoration requires the same platform and eligible purchasing store account.

## Refund and revocation treatment

A completed refund, chargeback, or store revocation may remove paid access. It must not delete existing local operational records. Viewing, correction, deletion, JSON backup, and CSV export remain available under the App’s access rules.

A temporary offline state or temporary store-verification failure must not by itself revoke a previously verified purchase.

## Remaining implementation checks

Before release:

1. confirm both products exist in the stores with the exact expected product types and price anchors;
2. verify storefront prices and tax categories;
3. test purchase, pending, cancellation-before-completion, restoration, refund, revocation, wrong-product, wrong-account, offline, and response-loss states;
4. confirm Google purchase acknowledgement within the required period;
5. confirm StoreKit 2 current-entitlement and transaction-update handling;
6. ensure every paywall says one time and contains no subscription wording; and
7. ensure store listing, App logic, Terms, and refund copy remain identical in substance.
