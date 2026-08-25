# PressBench Android — Store Readiness Gate

**Baseline:** `1.0.0-closed-v16-native` (version code 1403)

## Implemented baseline

- Native Jetpack Compose experience with a Setup → First piece → Production → Result workflow.
- Explicit Terms acceptance and safety acknowledgement before normal use.
- No account, login, reviewer credentials or purchase wall.
- Settings links to Privacy Policy, Terms, Safety, Local Data & Deletion, Third-Party Notices and Support; Privacy choices appears when UMP requires it.
- Functional user-initiated PDF and CSV export.
- Google test banner ads after UMP permits requests; `npa=1` supplied.
- No billing dependency, paid product, purchase, subscription, restore or management controls.
- Local deletion returns the App to an empty initial state.
- Android backup and device transfer disabled with manifest settings and explicit storage-domain exclusions.

## Console review still required before submitting

- Verify the uploaded artifact is the signed version code 1403 AAB and matches the recorded SHA-256.
- Verify privacy URL and all in-App legal URLs resolve publicly without login.
- Set **Contains ads: Yes**, **In-app purchases: No**, **App access: unrestricted**, and target audience **18+**.
- Complete Data Safety using `STORE-DISCLOSURES.md`, including Google Mobile Ads data.
- Complete content rating and all other App content declarations accurately.
- Confirm listing text and localized screenshots describe only functions present in this build and mark AI-generated/edited assets where Play asks.
- Confirm release notes contain real text in every selected locale, not placeholder instructions.
- Review countries/regions and any region-specific trader, privacy-representative, consumer or tax requirements.

## Binary acceptance checks

- version code/name, package, target API and merged permissions;
- dependency inventory and absence of Play Billing;
- merged permission inventory, including the Google Mobile Ads SDK's `com.google.android.gms.permission.AD_ID` declaration, remains consistent with advertising and Data Safety disclosures;
- test AdMob IDs, UMP gating and non-personalized request signal;
- backup/data-transfer exclusions;
- network and Data Safety consistency;
- 16 KB native-library compatibility;
- release lint, unit tests, ZIP integrity and upload-key signature;
- light/dark, LTR/RTL and long-translation device smoke tests;
- first-use legal links, deletion, active-run recovery, export sharing and banner placement.

This engineering checklist materially reduces rejection risk but cannot guarantee approval; Google evaluates the submitted binary, listing, account and declarations.
