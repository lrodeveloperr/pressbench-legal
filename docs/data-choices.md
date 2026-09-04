---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 4 September 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete operational records stored locally, in Apple-managed backups, or in backup files you export to a destination you choose.

## Delete local PressBench data

On iOS, open **More → Settings → Maintenance → Delete Local Data** and confirm. This clears supported operational records, active-run state and preferences and returns the App to onboarding. It intentionally preserves verified StoreKit entitlement state and the monotonic count used to enforce the five-free-run allowance. It clears the local last-backup status, but it does not delete backup files previously exported to Files.

On Android, the in-App **Delete Local Data** action clears operational records and preferences held in DataStore. It intentionally preserves the separately stored five-run usage counter and recent paid-entitlement verification time. Clearing all Android App storage or uninstalling removes all App-local storage, including those counters. Android cloud backup and device-to-device transfer are disabled; a qualifying purchase can be restored from Google Play.

## Optional backup files on iOS

No account or sign-in is required. In **More → Settings → Local Data & Backups**:

- **Create backup** opens Apple’s Files interface so you can save a PressBench backup to iCloud Drive, On My iPhone or another available Files provider.
- **Import backup** lets you select a compatible file, validates it and shows a summary before replacing local operational data.
- Restore never imports or changes App Store purchase entitlement.
- Restore never lowers the monotonic five-free-run usage count. The App keeps the highest of the current secure count, the count carried by the backup and the number of completed runs in the restored data.
- **Delete Local Data** does not delete exported backup files. Delete those copies in Files or with the selected provider.

A backup may contain machines, setups, completed runs, settings and the free-run usage count. It excludes active-run state and App Store entitlement. The file is not encrypted by PressBench, so protect its destination and sharing permissions. GoodUse Studios does not receive a copy.

## Reports and exports

Reports are created locally and shared only when you choose a destination through the platform share sheet. Android Pro supports PDF/CSV and iOS Pro supports PDF/XLSX. Copies saved or shared elsewhere are controlled by the destination and are not deleted by **Delete Local Data**.

## Purchases

On iOS, free users may save five successfully completed runs. iOS PressBench Pro is a monthly auto-renewable subscription configured at US$6.99 per month in the US storefront, with regional prices supplied by Apple. It unlocks unlimited runs and PDF/XLSX reports while active. The iOS App displays no ads.

On Android, free users may save five successfully completed runs. Android PressBench Pro is a monthly auto-renewable Google Play subscription that unlocks unlimited runs and PDF/CSV reports while active and verified. The Android App contains no advertising SDK and displays no ads. The US base price is US$6.99 per month; Google Play supplies regional prices. Users can manage or cancel through Google Play subscription settings and use **Restore purchase** in PressBench. Canceling does not delete existing records.

## Support email

For requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**.
