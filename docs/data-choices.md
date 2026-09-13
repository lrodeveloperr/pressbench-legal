---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 13 September 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete operational records stored locally, in Apple-managed backups, or in backup files you export to a destination you choose.

## Delete local PressBench data

On iOS, tap the gear icon to open **Settings**, then choose **Delete Local Data** and confirm. This action is unavailable while a run is active. When available, it clears supported operational records, stored session and draft state and preferences. It preserves the monotonic count used to enforce the ten-free-run allowance; StoreKit remains the authority for subscription access. It clears the local last-backup status, but it does not delete backup files previously exported to Files.

On Android, the in-App **Delete Local Data** action clears operational records and preferences held in private App storage, including the headless engine’s private database and durable local storage. It intentionally preserves the separately stored ten-run usage counter and signed, time-limited entitlement-verification record. Clearing all Android App storage or uninstalling removes all App-local storage, including those counters. Android cloud backup and device-to-device transfer are disabled; a qualifying purchase can be restored from Google Play.

## Optional backup files on iOS

No account or sign-in is required. Tap the gear icon to open **Settings**, then use **Local Data & Backups**:

- **Create backup** opens Apple’s Files interface so you can save a PressBench backup to iCloud Drive, On My iPhone or another available Files provider.
- **Import backup** lets you select a compatible file, validates it and shows a summary before replacing local operational data.
- Restore never imports or changes App Store purchase entitlement.
- Restore merges valid qualifying free-run identifiers already recorded on the device with those in the backup and qualifying restored runs, up to ten; it never lowers recorded usage.
- **Delete Local Data** does not delete exported backup files. Delete those copies in Files or with the selected provider.

A backup may contain machines, setups, completed runs, selected portable settings and up to ten qualifying free-run batch identifiers. It excludes active-run state and App Store entitlement. The file is not encrypted by PressBench, so protect its destination and sharing permissions. GoodUse Studios does not receive a copy.

## Reports and exports

Reports are created locally and exported only when you choose a destination through the platform share or document interface. On Android, the App writes only to the document destination you select. Android Pro supports PDF/CSV and iOS Pro supports PDF/XLSX. Copies saved or shared elsewhere are controlled by the destination and are not deleted by **Delete Local Data**.

## Purchases

On iOS, free users receive ten qualifying runs under the rule described above. PressBench Pro is a monthly auto-renewable App Store subscription that provides unlimited runs and PDF/XLSX reports while active. Apple displays the current localized price before purchase in each storefront. Users can [manage or cancel in their Apple Account subscription settings](https://apps.apple.com/account/subscriptions) and can use **Restore purchase** in PressBench. A previously acquired, verified annual entitlement may remain valid until its StoreKit expiration date, but the annual product is not offered for sale to new customers. Existing records remain readable after expiry, and the iOS App displays no ads.

On Android, free users receive ten qualifying runs under the same completion-and-save rule used on iOS. Android PressBench Pro is a monthly auto-renewable Google Play subscription that unlocks unlimited runs and PDF/CSV reports while active and verified. The Android App contains no advertising SDK and displays no ads. Google Play displays the current localized offer before purchase. Users can manage or cancel through Google Play subscription settings and use **Restore purchase** in PressBench. Canceling does not delete existing records.

## Support email

For requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**.
