# PressBench Android — Google Play Disclosure Worksheet

**Release reviewed:** `1.0.0-closed-v18-native` (version code 1405)  
**Package:** `com.goodusestudios.pressbench`  
**Source reviewed:** `lrodeveloperr/pressbench-apk-compiler` at `92ba7dd7a4beab7d9294d044a8d2fc10d1f6b499`  
**Reviewed:** 1 September 2026

This worksheet describes the Android v18 source and the release configuration used by the approved GitHub AAB workflow. Recheck the exact signed AAB and Play Console product state before rollout.

## Store model

- Free allowance: five successfully completed and saved press runs. Failed, canceled or unsaved runs do not consume the allowance.
- Neither tier contains advertising or an advertising SDK.
- PressBench Pro: one-month auto-renewable Google Play subscription.
- US base price: US$6.99 per month; regional prices are supplied through Google Play geo-pricing.
- Pro benefits: unlimited press runs and PDF/CSV report export while active and verified.
- Product ID: `pressbench_unlimited_monthly_android`; base plan: `monthly`.
- Verified legacy subscription `remove_ads_monthly` and lifetime product `pressbench_unlimited_lifetime_android` remain recognized.
- Existing records remain readable after the limit or subscription expiry.
- In-App deletion does not reset the separately stored free-run counter.
- No PressBench account, developer cloud sync, GoodUse Studios analytics, crash-reporting or attribution SDK.
- Local operational data in Android private storage; Android backup and device-to-device transfer disabled.
- Intended audience: adults and professional heat-press operators; not directed to children.

## App content declarations

- **Privacy policy:** `https://lrodeveloperr.github.io/pressbench-legal/privacy/`
- **Contains ads:** No.
- **In-app purchases/subscriptions:** Yes.
- **Subscription:** Monthly auto-renewable; localized Play price shown before purchase.
- **App access:** No account or reviewer credentials required. App Review must be able to exercise the free workflow; use Play licence-test configuration if the subscription flow must be tested.
- **Target audience:** Adults/18+; not directed to children.
- **Account deletion:** Not applicable; PressBench creates no developer account. Local deletion is available in Settings.
- **Government, financial and health features:** No.

## Data Safety working declaration

No advertising, consent-management, analytics, crash-reporting, attribution or tracking SDK is included. No advertising data categories should be declared for this release.

Google Play Billing processes purchase and subscription information. PressBench receives purchase status and tokens for acknowledgement and entitlement checks, processes tokens transiently, and stores locally only the time of the latest successful paid verification.

| Data type | Collected | Shared | Purposes |
| --- | --- | --- | --- |
| Purchase history / subscription status | Reconfirm in Play Console against Google Play Billing’s current SDK declaration | No independent developer sharing | App functionality; entitlement management; fraud prevention |

- Data transmitted to Google services is encrypted in transit according to Google’s service documentation.
- PressBench does not automatically upload machine, setup, run, report or free-text fields.
- PDF/CSV sharing is user initiated through Android’s system share sheet.
- GoodUse Studios has no developer backend receiving production records or purchase tokens.
- Reconfirm every Data Safety answer from the exact signed AAB and the SDK declarations shown in Play Console before submission.

## Subscription disclosure controls

1. Show Play’s localized price and monthly billing period before purchase.
2. State that the subscription renews monthly until canceled.
3. Identify all recurring benefits: unlimited runs and PDF/CSV reports.
4. Keep **Restore purchase** and the direct Google Play subscription-management route working.
5. Do not promise a trial or introductory price unless the active Play offer supplies it.
6. Preserve access to existing records after expiry.
7. Test purchase, acknowledgement, pending purchase, cancellation, expiry, refund/revocation, reinstall/restore and the 72-hour offline continuity boundary.

## Release controls

1. Verify the signed v18 AAB is version code 1405 and contains no advertising SDK, advertising components or advertising identifiers.
2. Confirm the Play subscription and `monthly` base plan are active in every selected country/region.
3. Keep the listing, **Contains ads**, **In-app purchases**, Data Safety and subscription disclosures synchronized with the binary.
4. Recheck target API, permissions, Play SDK status, 16 KB compatibility, signing and dependency inventory.
