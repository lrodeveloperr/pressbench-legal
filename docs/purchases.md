---
layout: default
title: Purchases, Paid Access, and Refunds
nav_title: Purchases
permalink: /purchases/
---

# Purchases, Paid Access, and Refunds

> **Pre-release draft — not yet effective.** This draft is based on PressBench logic v0.21.2. Exact products and prices must be verified in the final Apple App Store and Google Play configuration.

**Draft date: 12 August 2026**

This page supplements the [Terms of Use]({{ '/terms/' | relative_url }}).

## 1. Free Tier

The Free Tier permits:

- up to **3 saved setups**; and
- up to **10 saved batches**.

It is not a timed trial. JSON backup, restore, CSV export, viewing, correction, and deletion remain available as described in the App, subject to technical and data-integrity limits.

When the applicable free limit has been reached, the App may block creation of an additional setup or batch unless paid access is active. Existing records are not deleted merely because paid access is absent or temporarily unverified.

## 2. Paid unlock

PressBench offers a one-time, non-consumable paid unlock on both platforms:

| Platform | Product identifier | Product type | United States base price |
|---|---|---|---:|
| iOS | pressbench_unlimited_lifetime_ios | One-time non-consumable | US$4.99 |
| Android | pressbench_unlimited_lifetime_android | One-time non-consumable | US$4.99 |

The stores apply geographic pricing, local currency, and tax treatment. The exact product, amount, currency, and tax shown in the Apple or Google purchase sheet immediately before confirmation control the transaction.

There is no PressBench subscription, automatic renewal, monthly charge, annual charge, or free-trial conversion on either platform.

## 3. Paid features and limits

Paid access permits creation subject to physical limits of up to:

- 1,000 saved setups; and
- 1,000 saved batches.

It also unlocks the paid analytics and PDF/XLSX report capabilities identified on the purchase screen. JSON backup and CSV export remain available without paid access.

“Unlimited” in the product identifier means removal of the Free Tier’s 3-setup and 10-batch commercial limits. It does not remove technical limits. The App remains subject to supported-device requirements, available storage, an 8 MB primary operational-data budget, a 2 MB compatibility-storage budget, a 1 MB individual-record limit, and a 12,000-row detailed XLSX limit.

No purchase guarantees perpetual development, indefinite store availability, compatibility with every future operating system, or a particular future feature.

## 4. Purchase confirmation

No charge is authorised until the user confirms the official store purchase sheet. Before confirmation, the App and store sheet should identify:

- that the charge is one time;
- the exact local price and currency;
- the included paid features;
- that purchases are platform-specific;
- the restoration method;
- links to Privacy and Terms; and
- that refunds are handled under store rules and mandatory law.

If the in-App description and store sheet do not clearly agree, do not complete the transaction and contact support.

## 5. Restore purchases

Use **Restore Purchases** while signed into the Apple or Google account that made the purchase.

Purchase restoration restores an eligible entitlement only. It does not restore setups, batches, active work, or exported files. Operational data must be restored separately from a valid user-created backup where available.

PressBench has no cross-platform account. An Apple purchase does not unlock Android and a Google Play purchase does not unlock iOS. A purchase may also be unavailable under a different store account.

## 6. Offline and verification states

After a valid entitlement has been verified and cached, a temporary offline state or temporary store-verification failure must not by itself erase the entitlement or delete operational records.

Pending, cancelled-before-completion, refunded, charged-back, or revoked transactions may not provide paid access. Existing records, correction, JSON backup, CSV export, and deletion remain available under the applicable App logic even if paid access is unavailable.

## 7. Refunds

Refund eligibility is determined by the applicable store rules and mandatory consumer law.

- **Apple App Store:** use [Apple’s refund process](https://support.apple.com/118223).
- **Google Play:** use [Google Play’s refund process](https://support.google.com/googleplay/answer/2479637).

Apple or Google may approve, reject, process, or revoke a transaction. GoodUse Studios can help troubleshoot entitlement delivery but cannot guarantee or override a store decision. If a refund or revocation is completed, paid access may be removed.

Nothing on this page limits a mandatory refund, warranty, cancellation right, or other remedy that applicable law does not permit us or the Store to exclude.

## 8. Local-data deletion and purchases

Deleting App data or uninstalling PressBench does not delete the purchase history held by Apple or Google. An eligible purchase may remain restorable from the same store account.

Deleting App data does not delete operational files previously exported or shared. Restoration of a purchase does not restore those operational files or the App database.

## 9. Contact

For an entitlement issue, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Purchase) with the subject **“PressBench Purchase.”**

Include the platform, App version, country storefront, approximate order date, and a description of the problem. If necessary, include only a redacted order or transaction reference. Never email payment-card information, passwords, purchase tokens, JSON backups, or confidential production records.
