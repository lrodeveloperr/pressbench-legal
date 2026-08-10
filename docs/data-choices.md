---
layout: default
title: Local Data, Backup, Export, and Deletion
permalink: /data-choices/
---

# Local Data, Backup, Export, and Deletion

> **Pre-release draft.** Final deletion, backup, and purchase behaviour must be verified in the signed Android and iOS builds.

**Last updated: 10 August 2026**

PressBench has no developer account or cloud database. GoodUse Studios cannot see, recover, edit, or remotely delete production records stored in the App.

## Export or back up first

In PressBench, open **Data Management**.

- Use **Backup & restore** to save or share a JSON database backup.
- Use **Export CSV** for a spreadsheet-ready copy of production settings and batch records.
- Use the Analytics and reporting area to create PDF or XLSX reports where available under the current plan.

Treat every export as production data. Check the destination and file contents before relying on it. A JSON backup may replace current local records when restored, so preserve a known-good copy separately.

## Delete all local data

In the App:

1. Open the navigation menu.
2. Select **Data Management**.
3. In **Local data reset**, choose **Delete all local data**.
4. Complete the typed confirmation shown by the App.

The audited App clears the active local store and attempts to retire any alternate local storage backend. If the App reports that alternate storage could not be retired, an older local copy may remain recoverable: retry the deletion or clear the App’s storage through the operating system, then reopen the App and verify that no records return. Do not treat the in-App deletion as complete while that warning remains.

Successful local deletion does not delete copies previously exported, shared, emailed, uploaded, printed, or included in an operating-system, device, cloud, or workplace backup.

Clearing the App’s storage in device settings or uninstalling the App may also remove local records. These actions do not cancel an Android subscription. The iOS Pro unlock is a one-time purchase and has no renewal to cancel.

## Delete exported copies

Delete exported files from every location to which they were saved or shared, including Downloads, Files, email, messages, shared drives, cloud-storage folders, removable media, print queues, and recipients’ systems. GoodUse Studios cannot remove those copies.

## Device backups

Android, iOS, a device manufacturer, or a workplace management system may back up App data independently. Review the relevant device or account backup settings and remove old backups where appropriate. Restoration of a device backup may restore an older App database.

## Store and support data

Apple or Google controls store account, billing, and purchase history. Use the applicable platform controls for those records. To request access to or deletion of support email held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **“PressBench Data Request.”** We may need enough information to locate the correspondence and verify that the requester is authorised.

For more detail, read the [Privacy Policy]({{ '/privacy/' | relative_url }}).
