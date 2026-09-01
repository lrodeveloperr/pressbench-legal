---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 1 September 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete operational records stored locally, in Apple-managed backups, or in the user’s optional private iCloud backup.

## Delete local PressBench data

On iOS, open **More → Settings → Maintenance → Delete Local Data** and confirm. This clears supported operational records, active-run state and preferences and returns the App to onboarding. It intentionally preserves verified StoreKit entitlement state and the monotonic count used to enforce the five-free-run allowance. It also removes the local Apple backup sign-in link and local last-backup status, but it does not delete the private iCloud backup.

On Android, the in-App **Delete Local Data** action clears operational records and preferences held in DataStore. It intentionally preserves the separately stored five-run usage counter and recent paid-entitlement verification time. Clearing all Android App storage or uninstalling removes all App-local storage, including those counters. Android cloud backup and device-to-device transfer are disabled; a qualifying purchase can be restored from Google Play.

## Optional Apple and iCloud backup on iOS

The iOS App remains usable without signing in. Optional Sign in with Apple enables **Back Up Now**, **Restore**, **Sign Out** and **Delete iCloud Backup** in **More → Settings → Local Data & Backups**.

- **Back Up Now** replaces the current private PressBench iCloud key-value backup.
- **Restore** replaces local operational records after confirmation.
- **Delete iCloud Backup** removes the current PressBench value from the App’s private iCloud key-value store; it does not delete local records or Apple-managed device backups.
- **Sign Out** removes the local Apple authorization link and local backup status; it does not delete the private iCloud backup.

The backup may contain the stable Apple authorization identifier as an owner check plus machines, setups, completed runs and settings. It excludes App Store entitlement and active-run session state. GoodUse Studios does not receive a copy.

## Reports and exports

Reports are created locally and shared only when you choose a destination through the platform share sheet. Android Pro supports PDF/CSV and iOS Pro supports PDF/XLSX. Copies saved or shared elsewhere are controlled by the destination and are not deleted by **Delete Local Data** or **Delete iCloud Backup**.

## Purchases

On iOS, free users may save five successfully completed runs. iOS PressBench Pro is a monthly auto-renewable subscription that unlocks unlimited runs and PDF/XLSX reports. The iOS App displays no ads.

On Android, free users may save five successfully completed runs and may see a bottom Google banner. Android PressBench Pro is a monthly auto-renewable Google Play subscription that unlocks unlimited runs, removes the banner and enables PDF/CSV reports while active and verified. The US base price is US$6.99 per month; Google Play supplies regional prices. Users can manage or cancel through Google Play subscription settings and use **Restore purchase** in PressBench. Canceling does not delete existing records.

## Support email

For requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**.
