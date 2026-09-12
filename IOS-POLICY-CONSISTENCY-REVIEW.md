# PressBench iOS — Policy Consistency Review

**Review date:** 12 September 2026  
**Source reviewed:** `lrodeveloperr/Pressbench-iphone@db7c7a71f2275ee1337407b6e62fdcad5ced660d`  
**Bundle identifier:** `com.goodusestudios.pressbench`

## Confirmed implementation baseline

- Ten qualifying runs are free. A run uses one allowance only after it is successfully committed and saved and records at least one processed item or a first-piece attempt. Starting, leaving or discarding a run before save, and a failed save or commit, do not count. A saved run counts even if its recorded quality outcome is unsuccessful.
- PressBench Pro is offered through the monthly auto-renewable product `pressbench_unlimited_monthly_ios`, configured with a US reference price of US$9.99 and Apple-supplied storefront pricing shown by StoreKit.
- The annual product is not loaded, displayed or offered. `pressbench_unlimited_annual_ios` remains recognized only for continuity of a previously acquired, verified entitlement until its StoreKit expiration date.
- Pro unlocks unlimited runs and locally generated PDF/XLSX reports while the verified entitlement is active. Existing records remain readable without Pro.
- Purchases, restoration and entitlement updates use StoreKit 2. Payment-card data is not handled by the App. Product and transaction identifiers, purchase and expiration dates and verification state are processed in memory; entitlement is excluded from operational persistence and reconstructed from StoreKit at launch.
- No account or sign-in is required. No developer cloud database, advertising SDK, analytics SDK, crash-reporting SDK, attribution SDK or tracking SDK is included.
- Operational data is stored in the App’s private local storage and may be included in an Apple-managed device backup when the user enables that service.
- Optional manual backup and restore use Apple’s Files exporter/importer. Backup files contain machines, setups, completed runs, selected portable settings and up to ten qualifying free-run batch identifiers; they exclude active-run state and App Store entitlement and are not encrypted by PressBench.
- PDF/XLSX reports are generated locally and leave the App only through a user-initiated system share flow.
- Timer notifications are optional and scheduled locally. The body contains the current stage label, which may be operator-entered, and is not sent to GoodUse Studios.
- Delete Local Data is unavailable while a run is active. When available and confirmed, it clears operational records, stored session and draft state, preferences, the pending timer notification and the local backup-status display. It does not reset the monotonic usage ledger, cancel or alter the Apple-managed subscription, or delete previously exported files or Apple-managed backups.
- The App does not request location, contacts, calendars, photos, camera, microphone or health-data access.
- The privacy manifest declares no tracking and no collected data types; UserDefaults is declared for App functionality.

## Public-document reconciliation

The following files were reconciled to that baseline:

- `docs/privacy.md`
- `docs/terms.md`
- `docs/subscriptions.md`
- `docs/data-choices.md`
- `docs/support.md`
- `docs/index.md`
- `docs/accessibility.md`
- `docs/third-party-notices.md`

Android-specific disclosures were preserved and were not re-certified as part of this iOS review.

## Result

After correction and re-review, the public iOS policy statements are consistent with the identified source commit for the data lifecycle, permissions, backup/export behavior, deletion behavior, monetization, entitlement handling, advertising/tracking status and safety boundary. The source establishes the intended US$9.99 reference price and monthly product, but the active App Store Connect price, product duration and regional availability require separate verification in App Store Connect. This is a code-to-policy consistency review, not a legal opinion or a guarantee of App Store approval.
