---
layout: default
title: Local Data and Deletion
nav_title: Data
permalink: /data-choices/
---

# Local Data and Deletion

**Last updated: 25 August 2026**

PressBench has no developer cloud account or remote production database. GoodUse Studios cannot see, recover, edit or remotely delete the machines, setups, runs, quality-control records and preferences stored in the App's private local storage.

## Delete local PressBench data

Open **Settings → Delete Local Data** and confirm. This clears PressBench's locally stored records, active-run state and preferences and returns the App to an empty initial state. You can also clear the App's storage in Android settings or uninstall it.

The reviewed build disables Android backup and also explicitly excludes every supported storage domain from cloud backup and device-to-device transfer. These controls reduce unintended transfer, but users should still secure their device.

## Reports and exports

When you choose PDF or CSV, PressBench creates the report in its cache and opens Android's system share sheet. Nothing is uploaded automatically. A copy that you deliberately save or share is controlled by the chosen destination and is not deleted by **Delete Local Data**.

## Advertising and purchases

The closed-test build uses Google Mobile Ads and UMP with Google's official test identifiers. Deleting local data resets App preferences, including applicable consent state held by the App; it does not delete information independently handled by Google or the device platform.

The build has no Google Play Billing dependency, paid product, purchase, subscription, restore-purchase control or subscription-management control. There is therefore no PressBench subscription to cancel.

## Support email

For access, correction or deletion requests concerning support correspondence held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **PressBench Data Request**. We may request enough information to locate the correspondence and verify authority.

For more detail, see the [Privacy Policy]({{ '/privacy/' | relative_url }}).
