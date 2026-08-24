# PressBench Android — Google Play Disclosure Worksheet

**Release target:** Android 1.0.0  
**Reviewed:** 24 August 2026  
**Package:** `com.goodusestudios.pressbench`

This is a release worksheet, not a substitute for inspecting the final signed AAB and Play Console forms.

## Store model

- Core functionality: free.
- Advertising: yes — one Google-served anchored adaptive banner when privacy state permits ads.
- Ad personalization: publisher personalization disabled; Android advertising-ID permission removed.
- Paid product: optional Google Play auto-renewing monthly subscription `remove_ads_monthly` that removes PressBench banner ads while active.
- No account, login, developer cloud sync, interstitial ads, or app-open ads.
- Intended audience: adults / professional heat-press operators; not directed to children.

## App content declarations

- **Privacy policy:** required. Use `https://lrodeveloperr.github.io/pressbench-legal/privacy/` only after the GitHub Pages site is publicly reachable without authentication. The repository itself may remain private if the GitHub plan/settings allow a public Pages site.
- **Contains ads:** Yes.
- **App access:** All functionality can be accessed without special credentials. No reviewer login is required.
- **Target audience:** 18+ only, provided this accurately reflects the Play Console audience selection and marketing.
- **Content rating:** Complete the IARC questionnaire accurately. The app must not remain Unrated.
- **Account deletion:** Not applicable because PressBench does not create user accounts.
- **High-risk permissions:** none intended. Release manifest requests Internet and Google Play Billing only; `AD_ID` is explicitly removed.

## Data safety — release baseline

Production records entered into PressBench are stored locally and are not transmitted to GoodUse Studios. However, the app contains Google Mobile Ads and Google Play Billing, so **do not answer “no data collected or shared.”**

Google documents that Mobile Ads SDK 25.4.0 may automatically collect/share for advertising, analytics, and fraud prevention:

- IP address / approximate general location;
- user product interactions;
- diagnostics/performance information; and
- device/account identifiers. The release manifest removes the Android advertising-ID permission, but other app/device identifiers may still be processed by Google.

Google states Mobile Ads SDK data is encrypted in transit. UMP consent information is refreshed on each launch, ads fail closed if privacy state cannot be updated, and the App exposes Google’s Privacy Options form when required.

Google Play Billing processes purchase/subscription information needed to complete and verify the Remove Ads entitlement. PressBench does not receive full payment-card details.

Before submission, complete the Data safety form against the exact final AAB and current Google SDK disclosure documentation.

## Subscription disclosure

The Remove Ads screen must clearly show:

- that the core App is usable without the subscription;
- the local price returned by Google Play;
- that the subscription is monthly and auto-renewing until cancelled;
- that the benefit is removal of PressBench banner ads while active;
- Restore Purchases; and
- a direct Manage subscription / cancellation link in Settings for active subscribers.

No free trial should be advertised unless a Play Console offer is deliberately configured and the in-App/store disclosures are updated.

## Technical release gates

- `targetSdk = 36` (meets the Google Play requirement taking effect 31 August 2026).
- Build and publish an Android App Bundle (AAB).
- Verify 16 KB page-size compatibility on the final bundle, including every bundled native library from third-party SDKs. Google currently says apps targeting API 35+ must support 16 KB page sizes for Play updates by 1 February 2027; test before the first release rather than deferring the risk.
- Run release on at least one Android 15/16 16 KB environment or equivalent Play pre-launch testing.
- Replace Google sample AdMob IDs with approved production App ID and banner unit ID.
- Use the final Play upload/release signing configuration; never commit private keys or passwords.
- Verify subscription product/base plan is active and test through a Play testing track.
- Verify privacy/terms/safety/support URLs work publicly and without login.
- Verify all legal links from Settings and first-use onboarding.
- Verify UMP in EEA/UK and other configured regulated regions using Google test geography before production.
- Verify ads never overlap run controls, navigation, or system gesture areas.

## Distribution-specific gates

### Japan

Because PressBench offers an in-app subscription, distribution to consumers in Japan requires the business-operator disclosures required by Japan’s Specified Commercial Transactions Act, including operator name, telephone number, and physical address through the applicable Play/Payments surfaces or a compliant linked page.

### New personal Play accounts

If the developer account is a personal account created after 13 November 2023, production access requires a closed test with at least 12 testers continuously opted in for at least 14 days, followed by the Play production-access application.

### Global privacy

The app uses a privacy-minimising baseline: local-only production records, no account/cloud backend, no sensitive permissions, non-personalized publisher ad treatment, AD_ID permission removed, UMP regional consent, public privacy policy, local data deletion, and direct subscription management.

This baseline reduces risk but does not itself certify compliance with every law in every country. Before launch, confirm whether GoodUse Studios requires an EEA representative, UK representative, local consumer/merchant disclosures, tax registrations, or other jurisdiction-specific steps based on the actual business establishment, targeting, and processing.
