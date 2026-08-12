# PressBench Store Disclosures — Provisional Release Worksheet

**Logic baseline:** PressBench v0.21.2, reviewed 12 August 2026  
**Status:** Provisional until the final signed Android App Bundle, iOS archive, store products, and runtime traffic are inspected.

## 1. Public URLs

This repository is private and cannot be used as a store privacy-policy URL.

Planned public routes after approval:

- Privacy: /privacy/
- Terms: /terms/
- Purchases: /purchases/
- Support: /support/
- Data choices: /data-choices/
- Safety: /safety/
- Third-party notices: /third-party-notices/

Before use in a store, each final URL must be public, stable, accessible without authentication, and tested. Google’s privacy URL must not be a PDF or editable document.

## 2. Apple App Privacy

Provisional answer, conditional on final-binary verification:

- **Data collection:** No, GoodUse Studios does not collect data from this App.
- **Tracking:** No.
- **Privacy Policy URL:** required.
- **Privacy Choices URL:** use the public Data Choices page.

On-device machine profiles, setups, batches, notes, optional references, settings, and active-work state are not developer collection if they remain on-device. User-directed exports are not transmitted to GoodUse Studios.

Do not use “Data Not Collected” if the final App, SDKs, or Apple services used by GoodUse Studios transmit accessible diagnostics, identifiers, usage, purchase, support, or other information requiring disclosure.

Support email and store financial records remain described in the Privacy Policy even if they qualify for optional or out-of-App treatment under Apple’s disclosure definitions.

## 3. Google Play Data Safety

Provisional answers, conditional on final AAB verification:

- No PressBench account creation.
- No operational data collected by GoodUse Studios.
- No operational data shared by GoodUse Studios.
- No advertising or tracking.
- No GoodUse Studios analytics or crash-reporting SDK.
- No remote push token.
- No location, camera, microphone, contacts, Bluetooth, health, or advertising-ID access required by the audited logic.
- User-directed exports remain under user control.
- Google Play processes purchases under its own terms.

A privacy policy and Data Safety form are required even when the final answer is no collection and no sharing.

Do not submit these answers until the final manifest, SDK list, data-safety dependencies, backup rules, network configuration, and runtime traffic are verified.

Because PressBench has no account creation, Google’s online account-deletion requirement should not apply. The public Data Choices page should still explain local deletion.

## 4. Purchase products

| Platform | Product identifier | Store product type | US base price | Renewal |
|---|---|---|---:|---|
| iOS | pressbench_unlimited_lifetime_ios | Non-consumable one-time purchase | US$4.99 | None |
| Android | pressbench_unlimited_lifetime_android | One-time in-app product | US$4.99 | None |

Both stores use geographic pricing. The exact local storefront price, currency, and tax shown before confirmation control.

There is:

- no subscription;
- no automatic renewal;
- no monthly or annual billing;
- no trial conversion; and
- no advertising.

Consumer-facing copy should say **one-time paid unlock** rather than “unlimited” or “lifetime.”

## 5. Free and paid disclosures

Free Tier:

- up to 3 saved setups;
- up to 10 saved batches;
- not time limited;
- JSON backup and CSV export available.

Paid access:

- permits creation up to 1,000 saved setups and 1,000 saved batches;
- unlocks paid reports and advanced analytics;
- remains subject to storage, record, report-row, device, compatibility, and App-availability limits.

A separate purchase is required on Apple and Google because there is no cross-platform PressBench account.

A refund or revocation may remove paid access but must not delete local records. Temporary offline operation must not by itself revoke a previously verified entitlement.

## 6. Purchase-flow checks

### Apple

Verify:

- exact non-consumable product type and identifier;
- localized price and tax;
- StoreKit 2 verified transaction;
- currentEntitlements on launch and resume;
- transaction updates;
- pending and cancelled states;
- Restore Purchases;
- refund and revocation handling;
- offline cached entitlement;
- wrong-product rejection; and
- no subscription or renewal copy.

### Google

Verify:

- exact one-time product type and identifier;
- localized price and tax;
- Play Billing purchase-token and signature/verification handling;
- PENDING state does not grant access;
- PURCHASED state grants access only after required verification;
- acknowledgement within Google’s required period;
- restoration/query on launch and resume;
- refund, chargeback, and revocation handling;
- wrong-product rejection;
- offline cached entitlement; and
- no subscription, base-plan, renewal, cancellation, or grace-period copy.

## 7. Permissions and platform features

The audited logic does not require:

- location;
- contacts;
- camera;
- microphone;
- Bluetooth;
- health data;
- advertising identifier;
- broad shared-storage permission; or
- remote push.

Notifications are optional, scheduled locally, and must use generic text without customer, job, or production references. Timer use inside the App must remain available without notification permission.

Backup import, export, file saving, and sharing should use user-initiated system interfaces.

The operational database is designed to be excluded from automatic OS/cloud application backup. Verify the final Android data-extraction/backup rules and iOS file backup attributes.

## 8. Store-listing claims

Permitted only if the final applications match:

- local-first operational records;
- no login or GoodUse Studios cloud account;
- no ads or tracking;
- no GoodUse Studios analytics SDK;
- optional generic notifications;
- user-directed JSON, CSV, XLSX, and PDF files;
- one-time paid unlock on both platforms;
- App does not control or measure equipment; and
- operators must verify current manufacturer and supplier instructions.

Avoid absolute claims such as “zero network,” “data can never leave the device,” “unlimited,” “lifetime access,” “manufacturer verified,” “certified,” or “measures temperature consistency.”

Preferred privacy claim:

> PressBench does not transmit operational records to GoodUse Studios. Files you export or share are controlled by you and the selected destination.

## 9. Trader, audience, and market information

- Intended audience: adult heat-press operators and production teams.
- Likely category: Business or Productivity.
- Not directed to children.
- No user-to-user communication.
- No medical, financial, government, calibration, certification, or professional-advice function.

For EU storefronts, complete Apple and Google trader verification and provide the required business address, email, and telephone information.

For Québec, complete French-first contract and distance-contract review before enabling distribution. Translate policies and purchase disclosures required for every launch market.

## 10. Final submission checklist

1. Inspect final signed binaries, SDKs, permissions, entitlements, privacy manifests, and traffic.
2. Verify exact product IDs, one-time types, US$4.99 anchors, geographic prices, tax, and family-sharing settings.
3. Test every purchase, restoration, refund, revocation, pending, wrong-account, offline, and failure state.
4. Verify legal links and effective document versions inside both Apps.
5. Verify Terms and safety acceptance and privacy-notice presentation.
6. Verify optional generic notification content.
7. Verify automatic backup exclusion and manual unencrypted export warnings.
8. Verify delete-all across both storage backends.
9. Complete Apple App Privacy and Google Data Safety from the final binaries.
10. Publish stable public policy and support URLs.
11. Complete trader information and required translations.
12. Generate final third-party licence notices.
13. Ensure store copy matches the App and contains no subscription or uncapped-access wording.
