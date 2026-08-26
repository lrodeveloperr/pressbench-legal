# PressBench Android — Google Play Disclosure Worksheet

**Release reviewed:** `1.0.0-closed-v16-native` (version code 1403)
**Package:** `com.goodusestudios.pressbench`
**Reviewed:** 25 August 2026

This worksheet describes the signed closed-test build when compiled by the approved GitHub workflow with Google's official Mobile Ads test identifiers. Recheck it before changing SDKs, identifiers, permissions, data flows or commercial features.

## Store model

- Free closed-test app; all implemented functionality is available without payment.
- Google test adaptive-banner ads; no live ad revenue.
- Google Mobile Ads SDK 25.4.0 and UMP SDK 4.0.0.
- Non-personalized-ad signal (`npa=1`) added to each banner request.
- No Google Play Billing dependency, paid product, purchase UI or subscription controls.
- No account/login, developer cloud sync, GoodUse Studios analytics, crash-reporting or attribution SDK.
- Local operational data in Android private storage; Android backup and device-to-device transfer disabled with explicit exclusions.
- User-initiated PDF/CSV export through Android's system share sheet.
- Intended and access-restricted audience: adults/professional heat-press operators aged 18 and over; Google Play's minor-access restriction is enabled; not directed to children.

## App content declarations

- **Privacy policy:** `https://lrodeveloperr.github.io/pressbench-legal/privacy/`
- **Contains ads:** Yes.
- **In-app purchases/subscriptions:** No.
- **App access:** No credentials or special access required.
- **Target audience:** 18 and over; Google Play minor-access restriction enabled.
- **Account deletion:** Not applicable; no account is created. Local deletion is available in Settings.
- **Government, financial and health features:** No.

## Data Safety declaration

Google Mobile Ads may automatically collect and share data as disclosed by Google:

| Data type | Collected | Shared | Purposes |
| --- | --- | --- | --- |
| Approximate location (derived from IP) | Yes | Yes | Advertising/marketing; analytics; fraud prevention, security and compliance |
| App interactions | Yes | Yes | Advertising/marketing; analytics; fraud prevention, security and compliance |
| Diagnostics | Yes | Yes | Analytics; fraud prevention, security and compliance |
| Device or other IDs | Yes | Yes | Advertising/marketing; analytics; fraud prevention, security and compliance |

- Data transmitted by Google Mobile Ads is encrypted in transit according to Google.
- PressBench does not automatically upload machine, setup, run, report or free-text fields.
- User-selected PDF/CSV sharing is a user-initiated transfer through the system share sheet.
- The non-personalized-ad signal does not eliminate the SDK disclosures above.

## Release controls

1. Keep only Google's official test App and adaptive-banner IDs in the closed-test artifact.
2. Sign with the dedicated PressBench upload key.
3. Upload only to the intended testing track until production readiness is separately approved.
4. Keep store assets, descriptions, ads declaration, target audience and Data Safety answers synchronized with this exact binary.
5. Do not advertise or activate a paid ad-removal product until Play Billing, the Play product/base plan, entitlement lifecycle and updated disclosures are implemented and tested.
