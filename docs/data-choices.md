---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 31 August 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete operational records stored locally, in Apple-managed backups, or in the user’s optional private iCloud backup.

## Delete local PressBench data

On iOS, open **More → Settings → Maintenance → Delete Local Data** and confirm. This clears supported operational records, active-run state and preferences and returns the App to onboarding. It intentionally preserves verified StoreKit entitlement state and the monotonic count used to enforce the five-free-run allowance. It also removes the local Apple backup sign-in link and local last-backup status, but it does not delete the private iCloud backup.

On Android, use the corresponding in-App action, clear App storage or uninstall. The reviewed Android profile disables Android backup and device-to-device transfer.

## Optional Apple and iCloud backup on iOS

The iOS App remains usable without signing in. Optional Sign in with Apple enables **Back Up Now**, **Restore**, **Sign Out** and **Delete iCloud Backup** in **More → Settings → Local Data & Backups**.

- **Back Up Now** replaces the current private PressBench iCloud key-value backup.
- **Restore** replaces local operational records after confirmation.
- **Delete iCloud Backup** removes the current PressBench value from the App’s private iCloud key-value store; it does not delete local records or Apple-managed device backups.
- **Sign Out** removes the local Apple authorization link and local backup status; it does not delete the private iCloud backup.

The backup may contain the stable Apple authorization identifier as an owner check plus machines, setups, completed runs and settings. It excludes App Store entitlement and active-run session state. GoodUse Studios does not receive a copy.

## Reports and exports

Reports are created locally and shared only when you choose a destination through the platform share sheet. Android supports PDF/CSV and iOS Pro supports PDF/XLSX. Copies saved or shared elsewhere are controlled by the destination and are not deleted by **Delete Local Data** or **Delete iCloud Backup**.

## Purchases

On iOS, free users may save five successfully completed runs. PressBench Pro is a monthly auto-renewable subscription that unlocks unlimited runs and PDF/XLSX reports. Neither tier displays ads. Users can manage or cancel through Apple subscription settings and use **Restore purchase** in PressBench. Canceling does not delete existing records.

The reviewed Android closed-test profile has no Google Play Billing dependency or paid product. Its test-ad data handling is described in the [Privacy Policy]({{ '/privacy/' | relative_url }}).

## Support email

For requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**.
