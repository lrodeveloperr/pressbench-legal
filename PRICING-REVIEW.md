# PressBench Pricing Review

**Evidence base:** supplied PressBench source v0.17.1, reviewed 10 August 2026.

**Commercial model confirmed by the publisher on 10 August 2026:** iOS has a limited Free Tier followed by a one-time non-consumable Pro unlock with no recurring charge; Android has the same limited Free Tier followed by an auto-renewing Pro subscription; neither platform has ads. Exact prices, the Android billing interval, product identifiers, and the native purchase configuration remain pending.

## Bottom line

The source defines a **freemium creation-gate model**, but it does not define a sale price, currency, Android billing period, product identifier, trial, introductory offer, recurring Android benefit, or finished purchase integration. The current paywall and bridge are Android-subscription-oriented and do not yet implement the confirmed iOS one-time unlock.

| Tier | Source-defined creation rights and exports |
|---|---|
| Free | May add a setting while fewer than 3 operator-created settings are currently stored and add a batch while fewer than 5 batches are currently stored; JSON backup and CSV export remain available. |
| Pro | Intended to permit creation of up to 1,000 operator-created settings and 1,000 batch records; PDF and XLSX report exports are added. |

Free and Pro are new-record creation gates, not lifetime creation allowances or total storage limits. Deleting a record below the applicable Free threshold reopens a slot. Restore may load as many as 1,000 settings and 1,000 batches without restoring Pro. When a Free runtime is at or above a threshold for one record type, those records remain stored, viewable, editable or correctable, JSON-backupable, and CSV-exportable, but a new record of that type and PDF/XLSX report export remain blocked.

Canonical starter templates are excluded from the displayed user-created setting count, but the raw storage cap currently counts all recipe rows. Because five starters are installed by default, v0.17.1 can block a normal user at 995 operator-created settings while displaying `995 / 1000`. The final build must count canonical starters separately or disclose that the ceiling includes them. The UI, backup parser, and IndexedDB paths otherwise target a maximum of 1,000 records per type, but compatibility-storage mutation and replacement paths do not all enforce the same invariant. The source also imposes an 8 MB total internal data budget in the primary store, 2 MB in compatibility mode, and 1 MB per record, so a user may reach an internal limit before the numerical ceiling.

## What is implemented versus missing

Implemented in the supplied source:

- Free/Pro labels and usage counters.
- Paywall copy for settings, batches, capacity, report exports, Subscribe, and Restore Purchase.
- Free-tier enforcement functions.
- JSON backup and CSV export without a Pro check; PDF and XLSX report generation behind verified Pro entitlement.
- A design in which purchase status is not restored from an editable JSON backup.

Not established by the supplied source:

- any price or billing interval;
- the Android billing period and whether more than one subscription base plan will be offered;
- store product identifiers;
- a trial or introductory price;
- a complete native Apple or Google purchase service;
- cross-device entitlement behaviour;
- final cancellation, grace-period, billing-hold, refund, and expiry behaviour; or
- the recurring value delivered throughout the Android subscription period.

The web source explicitly states that a verified store purchase service is unavailable in that build, and its normalised local settings force `subscriptionActive` to false. A native store wrapper is therefore a release dependency, not a completed feature.

## Store-policy risk

The current Pro benefits are primarily a static creation-limit and export unlock. Google Play states that subscriptions must provide sustained or recurring value and must not be used for what is effectively a one-time benefit.

Because PressBench is intentionally offline, has no cloud service, and the identified Pro entitlement is static, auto-renewing billing has a material rejection and customer-fairness risk.

## Confirmed structure and required alignment

1. **iOS:** Limited Free Tier, then a **one-time non-consumable Pro unlock** that does not expire and has no recurring charge.
2. **Android:** Limited Free Tier, then an **auto-renewing Pro subscription**. The product must deliver and disclose genuine sustained or recurring value throughout the subscription period.
3. **Both platforms:** No advertising.
4. Display the current local price in the store purchase sheet. The Android sheet must also show the billing interval and automatic renewal. Do not hard-code a worldwide price into the legal policy.
5. Preserve stored records, viewing, editing or correction, JSON backup, and CSV export if Android Pro expires or cannot be verified; block PDF/XLSX report export and a new record of a type while its current stored count is at or above the applicable Free threshold.

The iOS purchase has no recurring charge and does not expire merely with time. The disclosed record, internal-data, device-compatibility, and App-availability limits still apply.

## Android subscription release conditions

Before release, add and document genuine recurring value throughout the subscription period, choose the exact billing period, create the Play product and base plan, implement secure entitlement verification and restoration, and show all of the following before purchase:

- product name and Pro benefits;
- actual local price, currency, and taxes where applicable;
- billing period and automatic renewal;
- trial or introductory conversion terms, if any;
- cancellation method and the fact that uninstalling does not cancel;
- an in-App link to an easy online subscription-management and cancellation method;
- what happens to existing records when access lapses; and
- working links to Privacy, Terms, and purchase management.

Policies cannot cure a product offer that lacks recurring value or omits these facts from the purchase screen.
