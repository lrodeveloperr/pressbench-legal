# PressBench Android — Google Play Disclosure Worksheet

**Release reviewed:** `1.0.1` (version code 2)  
**Package:** `com.goodusestudios.pressbench`  
**Source reviewed:** `lrodeveloperr/press-bench-android`  
**Reviewed:** 13 September 2026

This worksheet describes the Android 1.0.1 source. Recheck the exact signed AAB and Play Console product state before rollout.

## Store model

- Free allowance: ten qualifying press runs under the same completion-and-save rule used on iOS. Failed, canceled or unsaved runs do not consume the allowance.
- Neither tier contains advertising or an advertising SDK.
- PressBench Pro: one-month auto-renewable Google Play subscription.
- Google Play supplies the current localized offer before purchase; public policies contain no fixed amount.
- Pro benefits: unlimited press runs and PDF/CSV report export while active and verified.
- Product ID: `pressbench_unlimited_monthly_android`; base plan: `monthly`.
- A verified existing `pressbench_unlimited_annual_android` subscription remains recognized until expiry but is not offered to new customers.
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

Google Play Billing processes purchase and subscription information. PressBench receives purchase status and tokens for acknowledgement and entitlement checks. For restart continuity, the Android App stores the recognized product ID, purchase token, latest successful verification time, bounded expiry time and acknowledgement state in an app-private record authenticated with an Android Keystore HMAC. The record cannot extend itself and is accepted for no more than 30 days from that verification.

| Data type | Collected | Shared | Purposes |
| --- | --- | --- | --- |
| Purchase history / subscription status | Reconfirm in Play Console against Google Play Billing’s current SDK declaration | No independent developer sharing | App functionality; entitlement management; fraud prevention |

- Data transmitted to Google services is encrypted in transit according to Google’s service documentation.
- PressBench does not automatically upload machine, setup, run, report or free-text fields.
- PDF/CSV export is user initiated through Android’s system document interface and writes only to the document destination the user selects.
- GoodUse Studios has no developer backend receiving production records or purchase tokens.
- Reconfirm every Data Safety answer from the exact signed AAB and the SDK declarations shown in Play Console before submission.

## Subscription disclosure controls

1. Show Play’s localized price and monthly billing period before purchase.
2. State that the subscription renews monthly until canceled.
3. Identify all recurring benefits: unlimited runs and PDF/CSV reports.
4. Keep **Restore purchase** and the direct Google Play subscription-management route working.
5. Do not promise a trial or introductory price unless the active Play offer supplies it.
6. Preserve access to existing records after expiry.
7. Test purchase, acknowledgement, pending purchase, cancellation, expiry, refund/revocation, reinstall/restore and the signed 30-day offline-continuity boundary.

## Release controls

1. Verify the signed 1.0.1 AAB is version code 2 and contains no advertising SDK, advertising components or advertising identifiers.
2. Confirm the Play subscription and `monthly` base plan are active in every selected country/region.
3. Keep the listing, **Contains ads**, **In-app purchases**, Data Safety and subscription disclosures synchronized with the binary.
4. Recheck target API, permissions, Play SDK status, 16 KB compatibility, signing and dependency inventory.
