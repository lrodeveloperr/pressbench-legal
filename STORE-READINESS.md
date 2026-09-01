# PressBench Android — Store Readiness Gate

**Baseline:** `1.0.0-closed-v17-native` (version code 1404)  
**Source:** `lrodeveloperr/pressbench-apk-compiler@689d5d596ac5bd2de02f30984b9867dbd92c3624`  
**Reviewed:** 1 September 2026

## Implemented baseline

- Native Jetpack Compose Setup → First piece → Production → Result workflow.
- Explicit Terms acceptance and safety acknowledgement before normal use.
- Five successfully completed and saved free runs; failed, canceled and unsaved runs do not consume the allowance.
- Google Play Billing Library 9.1.0 with product `pressbench_unlimited_monthly_android` and monthly base plan `monthly`.
- US$6.99/month US base price model with Google Play localized/geo-priced display.
- Pro gates unlimited runs, removes the banner after entitlement verification and enables PDF/CSV reports.
- Purchase acknowledgement, restore/reconciliation, subscription management route, legacy entitlement recognition and up to 72 hours of verified offline continuity.
- Production Google adaptive banner for free users after UMP permission; non-personalized signal supplied.
- No PressBench account or developer cloud database.
- Local deletion, local PDF/CSV sharing, and Android backup/device-transfer exclusions.

## Play Console checks before rollout

- Verify the uploaded artifact is the signed version code 1404 AAB and record its SHA-256.
- Confirm production AdMob identifiers, UMP message configuration and countries/regions are correct.
- Activate `pressbench_unlimited_monthly_android` and base plan `monthly`; set US$6.99 and review every Google-generated regional price.
- Test with Play licence testers: new purchase, pending state, acknowledgement, restore, renewal, cancellation, expiry, refund/revocation, legacy products and reinstall.
- Verify the purchase screen shows Play’s localized price and monthly period, benefits, renewal wording, Privacy Policy, Terms and Restore purchase.
- Verify Settings provides a working subscription-management link.
- Set **Contains ads: Yes**, **In-app purchases: Yes**, **App access: unrestricted**, and the selected adult target audience accurately.
- Recomplete Data Safety using `STORE-DISCLOSURES.md`, Google Mobile Ads 25.4.0’s current disclosure and Play Billing’s current SDK declaration.
- Confirm the public privacy policy and every in-App legal URL resolve without login.
- Complete content rating and all other App content declarations accurately.
- Ensure listing copy and screenshots distinguish free and Pro functionality and do not promise unavailable offers.
- Review countries/regions and region-specific trader, consumer, tax, privacy-representative and subscription requirements.

## Binary acceptance checks

- version code/name, package, target API 36 and merged permissions;
- `com.android.vending.BILLING`, AdMob metadata and any SDK-added advertising identifier permission;
- production versus test AdMob identifiers in the exact release artifact;
- UMP gating, privacy options and `npa=1`;
- Play Billing 9.1.0, active product/base-plan match and acknowledgement path;
- free-run monotonicity, Pro gates, expiry behavior and 72-hour offline boundary;
- backup/data-transfer exclusions and clear-text traffic disabled;
- PDF/CSV entitlement gate and user-initiated FileProvider sharing;
- 16 KB native-library compatibility, release lint, tests, bundle integrity and upload signature;
- light/dark, LTR/RTL, long-translation and supported-Android device smoke tests.

This checklist reduces rejection and consumer-disclosure risk but cannot guarantee Google Play approval.
