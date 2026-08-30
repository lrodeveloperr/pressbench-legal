---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 30 August 2026**

PressBench has no GoodUse Studios cloud account or developer-controlled production database. GoodUse Studios cannot see, recover, edit or remotely delete the machines, setups, runs, quality-control records and preferences stored in the App's private local storage, in an Apple-managed device backup or transfer, or in the user's optional private iCloud key-value backup.

PressBench does not create a GoodUse Studios or developer-operated user account, so there is no PressBench account to delete. Optional Sign in with Apple is used only to enable the App's private Apple backup controls. The effects of **Sign Out** and **Delete Local Data**, including what they do not delete, are described below.

## Delete local PressBench data

On iOS, open **More → Settings → Maintenance → Delete Local Data** and confirm. This clears supported PressBench operational records, active-run state and supported preferences and returns the App to onboarding. It intentionally preserves verified StoreKit entitlement state and the monotonic count used to enforce the five-free-run allowance. On Android, use the corresponding in-App action, clear the App's storage in Android settings or uninstall it.

The Android build disables Android backup and explicitly excludes every supported storage domain from cloud backup and device-to-device transfer. These controls reduce unintended transfer, but users should still secure their device.

On iOS, **More → Settings → Maintenance → Delete Local Data** removes the local Apple backup sign-in link and local last-backup status. It does not delete the existing iCloud backup value.

## Optional Apple and iCloud backup on iOS

The iOS App remains fully usable without signing in. If you choose Sign in with Apple, PressBench stores the Apple authorization identifier in local UserDefaults and attempts an initial backup of machines, setups, completed runs and settings to the App's private iCloud key-value store. The backup envelope includes that identifier as an owner check. The identifier and backup are not transmitted to a GoodUse Studios server. The current App does not continuously or automatically back up after every change.

Separately, Apple may include the App's local storage and preferences in an Apple-managed device backup or device transfer under the user's Apple and iCloud settings. PressBench does not control those system copies, and GoodUse Studios does not receive them.

In **Settings → Local Data & Backups**, you can:

- choose **Back Up Now**;
- restore from iCloud after confirming that local operational data will be replaced;
- choose **Sign Out** to remove the local Apple authorization link and local last-backup status.

The backup excludes App Store purchase entitlement and active-run session state. **Sign Out** does not delete the existing iCloud value. The current App has no in-app **Delete iCloud Backup** control. Apple may provide device or account controls for iCloud data; their availability and behaviour are controlled by Apple. Availability also depends on the device's Apple and iCloud configuration.

## Reports and exports

When you choose an export, PressBench creates it locally and opens the platform's system share sheet. Android supports PDF/CSV and iOS supports PDF/XLSX. Nothing is uploaded automatically. A copy that you deliberately save or share is controlled by the chosen destination and is not deleted by **Delete Local Data**.

## Advertising and purchases

The Android closed-test profile uses Google Mobile Ads and UMP with Google's official test identifiers. The iOS profile uses PressBench’s production AdMob identifiers, requests current consent information and sends a production ad request only when UMP reports that ads may be requested. Deleting local data resets supported App preferences; it does not delete information independently handled by Google or the device platform.

The Android build has no Google Play Billing dependency or paid product. On iOS, PressBench Pro is a monthly auto-renewable subscription handled by Apple. Users can manage or cancel it through Apple subscription settings and use **Restore purchase** on the PressBench Pro paywall. Canceling the subscription does not delete local operational records.

## Support email

For access, correction or deletion requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**. We may request enough information to locate the correspondence and verify authority.

For more detail, see the [Privacy Policy]({{ '/privacy/' | relative_url }}).
