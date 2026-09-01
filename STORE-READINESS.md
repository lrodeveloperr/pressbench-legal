# PressBench Android — Store Readiness Gate

**Baseline:** `1.0.0-closed-v18-native` (version code 1405)  
**Source:** `lrodeveloperr/pressbench-apk-compiler@92ba7dd7a4beab7d9294d044a8d2fc10d1f6b499`  
**Reviewed:** 1 September 2026

## Implemented baseline

- Native Jetpack Compose Setup → First piece → Production → Result workflow.
- Explicit Terms acceptance and safety acknowledgement before normal use.
- Five successfully completed and saved free runs; failed, canceled and unsaved runs do not consume the allowance.
- Google Play Billing Library 9.1.0 with product `pressbench_unlimited_monthly_android` and monthly base plan `monthly`.
- US$6.99/month US base price model with Google Play localized/geo-priced display.
- Pro gates unlimited runs and PDF/CSV reports after entitlement verification.
- Purchase acknowledgement, restore/reconciliation, subscription management route, legacy entitlement recognition and up to 72 hours of verified offline continuity.
- No advertising SDK or ad inventory in either tier.
- No PressBench account or developer cloud database.
- Local deletion, local PDF/CSV sharing, and Android backup/device-transfer exclusions.

## Play Console checks before rollout

- Verify the uploaded artifact is the signed version code 1405 AAB and record its SHA-256.
- Activate `pressbench_unlimited_monthly_android` and base plan `monthly`; set US$6.99 and review every Google-generated regional price.
- Test with Play licence testers: new purchase, pending state, acknowledgement, restore, renewal, cancellation, expiry, refund/revocation, legacy products and reinstall.
- Verify the purchase screen shows Play’s localized price and monthly period, benefits, renewal wording, Privacy Policy, Terms and Restore purchase.
- Verify Settings provides a working subscription-management link.
- Set **Contains ads: No**, **In-app purchases: Yes**, **App access: unrestricted**, and the selected adult target audience accurately.
- Recomplete Data Safety using `STORE-DISCLOSURES.md` and Play Billing’s current SDK declaration.
- Confirm the public privacy policy and every in-App legal URL resolve without login.
- Complete content rating and all other App content declarations accurately.
- Ensure listing copy and screenshots distinguish free and Pro functionality and do not promise unavailable offers.
- Review countries/regions and region-specific trader, consumer, tax, privacy-representative and subscription requirements.

## Binary acceptance checks

- version code/name, package, target API 36 and merged permissions;
- `com.android.vending.BILLING`, with no AdMob metadata, advertising identifier permission or Google Mobile Ads/UMP components;
- Play Billing 9.1.0, active product/base-plan match and acknowledgement path;
- free-run monotonicity, Pro gates, expiry behavior and 72-hour offline boundary;
- backup/data-transfer exclusions and clear-text traffic disabled;
- PDF/CSV entitlement gate and user-initiated FileProvider sharing;
- 16 KB native-library compatibility, release lint, tests, bundle integrity and upload signature;
- light/dark, LTR/RTL, long-translation and supported-Android device smoke tests.

This checklist reduces rejection and consumer-disclosure risk but cannot guarantee Google Play approval.
