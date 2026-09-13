# PressBench Android — Store Readiness Gate

**Baseline:** `1.0.1` (version code 2)  
**Source:** `lrodeveloperr/press-bench-android`  
**Reviewed:** 13 September 2026

## Implemented baseline

- Native Jetpack Compose Setup → First piece → Production → Result workflow.
- Explicit Terms acceptance and safety acknowledgement before normal use.
- Ten qualifying free runs under the same completion-and-save rule used on iOS; failed, canceled and unsaved runs do not consume the allowance.
- Google Play Billing Library 9.1.0 with product `pressbench_unlimited_monthly_android` and monthly base plan `monthly`.
- Google Play-localized monthly offer displayed dynamically; no amount embedded in the App or public policies.
- Pro gates unlimited runs and PDF/CSV reports after entitlement verification.
- Purchase acknowledgement, restore/reconciliation, subscription management route, existing annual-entitlement recognition and signed 30-day offline continuity.
- No advertising SDK or ad inventory in either tier.
- No PressBench account or developer cloud database.
- Local deletion, local PDF/CSV sharing, and Android backup/device-transfer exclusions.

## Play Console checks before rollout

- Verify the uploaded artifact is the signed version code 2 AAB and record its SHA-256.
- Activate `pressbench_unlimited_monthly_android` and base plan `monthly`; keep top-end markets at iOS parity and reduce only lower-price markets by roughly one Play pricing tier, then review every localized amount.
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
- free-run monotonicity, Pro gates, expiry behavior and signed 30-day offline boundary;
- backup/data-transfer exclusions and clear-text traffic disabled;
- PDF/CSV entitlement gate and user-initiated export through Android’s system document interface;
- 16 KB native-library compatibility, release lint, tests, bundle integrity and upload signature;
- light/dark, LTR/RTL, long-translation and supported-Android device smoke tests.

This checklist reduces rejection and consumer-disclosure risk but cannot guarantee Google Play approval.
