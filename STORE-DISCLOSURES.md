# PressBench Android — Google Play Disclosure Worksheet

**Release target reviewed:** Android 1.0.0-closed-v14-native

**Reviewed:** 25 August 2026

**Package:** `com.goodusestudios.pressbench`

**Approved source commit:** `52547ce51e50134004e34dd9da899ac014cd3d9a`

This worksheet matches the closed-test AAB built from the approved source with Google’s official Mobile Ads test identifiers. Recheck it before replacing test IDs, adding billing or changing SDKs.

## Store model

- Free closed-test app.
- Google test adaptive-banner ads; no live ad revenue.
- Google Mobile Ads SDK 25.4.0 and UMP SDK 4.0.0.
- Non-personalized-ad signal added to every banner request.
- No Google Play Billing dependency and no paid product.
- Local **Remove Ads** preference only; no purchase or subscription entitlement.
- No account/login or developer cloud sync.
- No GoodUse Studios analytics, crash-reporting or attribution SDK.
- User-initiated PDF and CSV export through Android’s system share sheet.
- Intended audience: adults / professional heat-press operators; not directed to children.

## App content declarations

- **Privacy policy:** `https://lrodeveloperr.github.io/pressbench-legal/privacy/`
- **Contains ads:** Yes.
- **In-app purchases/subscriptions:** No.
- **App access:** All implemented functionality is available without credentials.
- **Target audience:** 18 and over.
- **Account deletion:** Not applicable; PressBench creates no account. Local deletion is available in Settings.
- **Government app:** No.
- **Financial features:** No.
- **Health features:** No.

## Data Safety declaration

Google Mobile Ads may automatically collect or share the following, as disclosed by Google for SDK 25.4.0:

| Data type | Collected | Shared | Purposes |
| --- | --- | --- | --- |
| Approximate location (derived from IP) | Yes | Yes | Advertising or marketing; analytics; fraud prevention, security and compliance |
| App interactions | Yes | Yes | Advertising or marketing; analytics; fraud prevention, security and compliance |
| Diagnostics | Yes | Yes | Analytics; fraud prevention, security and compliance |
| Device or other IDs | Yes | Yes | Advertising or marketing; analytics; fraud prevention, security and compliance |

Operational machine, setup, run and report data stays in private app storage and is not automatically uploaded by PressBench.

- Data is encrypted in transit by Google.
- The App does not offer account creation.
- PDF/CSV disclosure is covered as user-initiated transfer through the system share sheet.
- The App supplies Google’s non-personalized-ad signal, but the technical SDK data above still requires disclosure.

## Exact dependency baseline

Direct release dependencies include AndroidX/Jetpack Compose, AndroidX DataStore, Google Mobile Ads 25.4.0 and Google UMP 4.0.0. Play Billing is absent.

## Closed-test launch controls

1. Use only Google’s official Android test app and adaptive-banner test IDs.
2. Sign every upload with the dedicated PressBench upload key.
3. Upload the AAB to a closed-testing draft; do not publish production.
4. Add required store icon, feature graphic and phone screenshots.
5. Complete the 12-testers-for-14-continuous-days requirement before applying for production access.
6. Before production, replace test IDs with approved production IDs, link the AdMob app to its Play listing, finish AdMob account/app review and re-audit the final AAB.
7. Do not advertise a paid ad-removal product until Play Billing and a real product are implemented and tested.
