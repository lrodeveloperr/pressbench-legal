---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 28 August 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete the machines, setups, runs, quality-control records and preferences stored in the App's private local storage or in the user's optional private iCloud backup.

## Delete local PressBench data

Open **Settings → Delete Local Data** and confirm. This clears PressBench's locally stored records, active-run state and preferences and returns the App to an empty initial state. You can also clear the App's storage in Android settings or uninstall it.

The Android build disables Android backup and explicitly excludes every supported storage domain from cloud backup and device-to-device transfer. These controls reduce unintended transfer, but users should still secure their device.

On iOS, **Delete Local Data** also turns off automatic PressBench backup so an existing iCloud backup is not overwritten by the newly empty local state. It does not itself delete that iCloud backup.

## Optional Apple and iCloud backup on iOS

The iOS App remains fully usable without signing in. If you choose Sign in with Apple, PressBench stores the Apple authorization identifier in the device Keychain and can automatically back up machines, setups, completed runs and settings to the App's private iCloud container. GoodUse Studios does not receive the identifier or backup.

In **Settings → Apple & iCloud Backup**, you can:

- create a backup immediately;
- restore from iCloud after confirming that local operational data will be replaced;
- turn off automatic backup while retaining the existing iCloud copy; or
- permanently delete the iCloud backup without deleting data on the device.

The backup excludes App Store purchase entitlement and active-run session state. Availability depends on the device's Apple and iCloud configuration.

## Reports and exports

When you choose an export, PressBench creates it locally and opens the platform's system share sheet. Android supports PDF/CSV and iOS supports PDF/XLSX. Nothing is uploaded automatically. A copy that you deliberately save or share is controlled by the chosen destination and is not deleted by **Delete Local Data**.

## Advertising and purchases

The closed-test build uses Google Mobile Ads and UMP with Google's official test identifiers. Deleting local data resets App preferences, including applicable consent state held by the App; it does not delete information independently handled by Google or the device platform.

The build has no Google Play Billing dependency, paid product, purchase, subscription, restore-purchase control or subscription-management control. There is therefore no PressBench subscription to cancel.

## Support email

For access, correction or deletion requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**. We may request enough information to locate the correspondence and verify authority.

For more detail, see the [Privacy Policy]({{ '/privacy/' | relative_url }}).
