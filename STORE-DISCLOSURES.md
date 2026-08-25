# PressBench Android — Google Play Disclosure Worksheet

**Release target reviewed:** Android 1.0.0-closed-v14  
**Reviewed:** 25 August 2026  
**Package:** `com.goodusestudios.pressbench`  
**Source ZIP SHA-256:** `3ad63565ae2c2492eee545304cd866b435de78a6f231388ae952d35c3bac5442`

This is an exact-code worksheet, not a substitute for inspecting the final signed AAB and Play Console forms. Do not enter these answers in Play Console until the veteran review is complete and the final submitted AAB matches this baseline.

## Store model in the reviewed build

- Intended commercial model: free download for this closed-test baseline; confirm the final Play pricing setting separately.
- Advertising: no. The 320×50 area is an empty interface-inspection placeholder.
- Paid product: none. The purchase, restoration and subscription-management controls are local simulations only.
- Account/login: none.
- Developer cloud sync: none.
- Analytics/crash/attribution SDK: none.
- Export: not implemented; PDF and CSV controls display a toast only.
- Photos/camera: not implemented.
- Developer-selected intended audience: adults / professional heat-press operators; not directed to children. The App does not technically verify age.

## App content declarations

- **Privacy policy:** `https://lrodeveloperr.github.io/pressbench-legal/privacy/` after the 25 August 2026 exact-build policy set is published and publicly verified.
- **Contains ads:** No for the exact v14 package.
- **In-app purchases/subscriptions:** No for the exact v14 package.
- **App access:** All implemented functionality is available without credentials.
- **Target audience:** Select 18 and over as the developer’s intended audience decision; this is not a code-derived age gate.
- **Account deletion:** Not applicable because PressBench creates no account. Local data deletion is available under Settings.
- **Permissions:** `INTERNET`, `VIBRATE`, `WAKE_LOCK`.

## Data safety — provisional exact-build baseline

The reviewed v14 code stores machine, setup, active-run, timer, QC, completed-run and preference data locally in WebView/app storage. It contains no code that automatically sends that operational data off device and no third-party SDK that collects analytics, advertising, attribution or crash data.

Provisional finding: **no automatic publisher collection or sharing was identified in the reviewed source**. Final Data Safety answers remain unset until the signed AAB, merged manifest, dependency tree and network test are verified, including treatment of user-initiated support email under Google’s current definitions. Provider-controlled browser, email and Google Play processing must be evaluated separately under Google’s current Data Safety definitions.

## Exact dependency baseline

Direct App dependencies are AndroidX Core KTX, Activity Compose, Compose UI, UI Tooling Preview and debug-only UI Tooling. Google Mobile Ads, UMP and Play Billing are absent.

## Release blockers

1. Remove or genuinely implement simulated ads, privacy choices, billing, restoration, subscription management and PDF/CSV controls.
2. Remove the seeded production values or mark every demo card, detail and run screen unmistakably as **DEMO — NOT FOR PRODUCTION**; prevent a production run until the operator replaces or expressly confirms the values. Remove manufacturer/supplier attribution unless genuine and authorised.
3. Correct or stop marketing the current “first-pass yield” metric because the reviewed formula does not subtract rework.
4. If any simulated function is implemented, recompile the applicable legal modules and store declarations from the final code; do not reuse this no-ads/no-billing baseline.
5. Resolve or formally accept the PressBench name/trademark risk before public launch.
6. Build and inspect the final signed AAB, including its merged manifest and full dependency tree.
7. Perform network testing and verify Android backup remains disabled.
8. Verify the Target Audience and content-rating forms, plus every legal URL and in-App link.
9. Publish the matching legal pages atomically and verify them publicly. Do not replace policies for another active build with this exact-v14 baseline.
10. Capture only genuine final screenshots that show working functions.

## Localized listing control

The app has 31 base language IDs plus a selectable Traditional Chinese (`zh-Hant`) override. Every localized listing must remain within Google’s field limits and must not claim export, photos, ads, purchases, machine control, recommended settings or other absent functionality.
