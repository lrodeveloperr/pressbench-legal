---
layout: default
title: Purchases, Pro Access, Cancellations, and Refunds
nav_title: Purchases
permalink: /subscriptions/
---

# Purchases, Pro Access, Cancellations, and Refunds

> **Pre-release draft — not yet effective.** The platform offer structure is fixed, but the prices, Android billing period and recurring value, product configuration, and native purchase implementation remain pending.

**Draft date: 10 August 2026**

This page supplements the [Terms of Use]({{ '/terms/' | relative_url }}). Before any purchase, the official Apple App Store or Google Play interface will show the product, local price, currency, tax and other applicable transaction terms. For Android, it will also show the billing period, automatic-renewal terms, any trial or introductory offer, and renewal date.

## 1. Free Tier and Pro features

The audited PressBench configuration provides:

| Access | Creation rights and features |
|---|---|
| Free Tier | May add a setting while fewer than 3 operator-created settings are currently stored and add a batch while fewer than 5 batches are currently stored. JSON backup and CSV export remain available. |
| Pro | Intended to permit creation of up to 1,000 operator-created production settings and 1,000 batch records, and adds PDF and XLSX report exports. JSON backup and CSV export remain available. |

Deleting a record of a type reopens a Free Tier slot. Restore may place a database above either Free count; restored records remain stored, viewable, editable or correctable, JSON-backupable, and CSV-exportable, but no new record of that type may be added until the stored count falls below its threshold or Pro is active.

Factory or starter examples do not count against the user-created setting allowance in the intended release. Local device and internal data limits still apply. The audited v0.17.1 runtime uses an 8 MB total limit in primary storage, a 2 MB total limit in compatibility storage, and a 1 MB individual-record limit. A user may therefore reach an internal limit before the numerical record ceiling. The final build must count starter examples separately and enforce every disclosed limit consistently.

## 2. Platform offers

The confirmed commercial structure is:

- **iOS:** a limited Free Tier followed by a one-time, non-consumable Pro unlock. The unlock does not renew and has no recurring charge.
- **Android:** a limited Free Tier followed by an auto-renewing Pro subscription.
- **Both platforms:** no advertising.

No charge is authorised until the user confirms the platform purchase sheet. If the in-App description and platform purchase sheet do not clearly agree, do not complete the purchase and contact support.

The iOS unlock is a one-time purchase with no recurring charge and does not expire merely with time. Record, storage, device-compatibility, and App-availability limits still apply.

## 3. Android auto-renewing access

For the Android subscription:

- the store account is charged the displayed amount and applicable tax for the displayed billing period;
- access renews automatically at the end of each period until cancelled;
- the store may charge shortly before renewal as permitted by its terms;
- a free trial or introductory price applies only if the store sheet expressly offers it, and it converts on the date and at the price shown there unless cancelled in time;
- cancellation stops future renewal but normally leaves Pro active until the end of the paid period; and
- uninstalling or deleting PressBench does **not** cancel the subscription.

PressBench does not independently charge a payment card. Google Play handles subscription billing.

## 4. Cancel or manage

Manage the subscription in Google Play under **Payments & subscriptions → Subscriptions**, or use Google’s [subscription management instructions](https://support.google.com/googleplay/answer/7018481).

The released Android build must also provide an easy-to-use in-App link to the applicable online subscription-management and cancellation method.

Users can self-cancel through the purchasing Google Play account. GoodUse Studios may also cancel a verified subscription request where Play Console and applicable rules permit. Sending an email or deleting the App does not cancel billing unless and until Google Play or GoodUse Studios confirms cancellation.

To ask GoodUse Studios to consider developer cancellation, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Android%20Cancellation) with the subject **“PressBench Android Cancellation.”** Include the Google Play order ID, purchase date, country storefront, and reason. Do not send a password, payment card, or purchase token.

The iOS Pro unlock is a one-time purchase, not a subscription, so it has no future renewal to cancel. Refunds are addressed in Section 8.

## 5. Restore purchases and device changes

Use **Restore Purchase** where the App provides it. The device must use the same store account and a supported platform. Purchase restoration verifies entitlement through the platform; entitlement is not imported from a JSON backup.

PressBench has no cross-platform account. An Android purchase does not automatically transfer to Apple, and an Apple purchase does not automatically transfer to Android, unless the purchase screen expressly states otherwise.

## 6. Expiry, billing failure, and local records

The iOS Pro entitlement does not expire merely with time. A completed refund or store revocation may terminate it. An unsupported device or operating-system version, temporary store outage, or temporary inability to verify or restore may prevent access without terminating the underlying entitlement. The final iOS build must cache a verified entitlement appropriately and must not downgrade Pro solely because the device is temporarily offline or the store is temporarily unavailable. Android Pro ends when the paid entitlement expires or is otherwise no longer active.

In the audited runtime, inactive or unverified Pro does not delete existing or restored local production records. Those records remain stored, viewable, editable or correctable, available to JSON backup, and available to CSV export. PDF/XLSX report export is blocked. A new record of a type is blocked while its current stored count is at or above the applicable Free Tier threshold; deleting records below that threshold reopens a slot. Final native builds must be tested to preserve this behaviour for Android expiry, cancellation, billing failure, grace or hold states, and for a refund, revocation, pending purchase, or offline verification state on either platform.

Device failure, uninstall, storage clearing, or backup replacement can still remove records. Export a current JSON backup before changing device, store account, or plan.

## 7. Price changes

Storefront prices may differ by country, currency, tax, and platform. The iOS transaction is charged once at the price confirmed on its purchase sheet. Any Android subscription price change is handled under applicable store rules, including notice or consent where required. Android users who do not accept a change may cancel before it takes effect.

## 8. Refunds

Refund eligibility is determined by the applicable store rules and mandatory consumer law.

- **Apple App Store:** Apple handles App Store refund requests. [Request an Apple refund](https://support.apple.com/118223).
- **Google Play:** A user may [request a Google Play refund](https://support.google.com/googleplay/answer/2479637). Google may decide the request. A user may also ask GoodUse Studios to consider a developer-issued full or partial refund by following Section 9. We consider discretionary Android requests case by case, including the request timing and reason, transaction status, prior refunds, apparent use or abuse, technical circumstances, Google Play rules, and mandatory law. Where permitted, GoodUse Studios may issue the refund through Play Console. See Google’s [developer order and refund guidance](https://support.google.com/googleplay/android-developer/answer/2741495).

We can help identify the correct product or troubleshoot entitlement, but cannot guarantee that a refund request will be approved. Nothing on this page limits a mandatory refund or other remedy available under applicable law.

## 9. Contact

For an entitlement issue, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Purchase) with the subject **“PressBench Purchase.”** Include the platform, App version, country storefront, order date, and a description of the issue.

For developer consideration of an Android refund, use the subject **“PressBench Android Refund Review”** and include the Google Play order ID, purchase date, country storefront, App version, and reason for the request. Never email full payment-card information, passwords, purchase tokens, JSON backups, or confidential production records. A request is not approved unless Google Play or GoodUse Studios confirms the refund.
