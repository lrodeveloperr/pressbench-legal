---
layout: default
title: Local Data, Backup, Export, and Deletion
permalink: /data-choices/
---

# Local Data, Backup, Export, and Deletion

> **Pre-release draft.** Final storage, deletion, backup, and purchase behaviour must be verified in the signed Android and iOS applications.

**Last updated: 12 August 2026**

PressBench has no GoodUse Studios account or operational cloud database. GoodUse Studios cannot see, recover, edit, or remotely delete setups, batches, active work, or other operational records stored in the App.

## Back up or export

Use the App’s Data and Backup functions to:

- create or restore a JSON operational backup;
- export CSV records; and
- create PDF or XLSX reports where paid access and report limits permit.

PressBench does not encrypt these files. Treat them as production records. Check the destination, contents, and access controls before relying on or sharing them.

A restore can replace current local records. The App validates the incoming file and creates a local pre-restore recovery point before replacement. Preserve a separate known-good copy before restoring or deleting important records.

## Delete all local data

Use **Delete all local data** and complete the typed confirmation shown by the App.

The operation is intended to delete local machines, setups, batches, preferences, active work, drafts, and recovery state from every PressBench storage backend. The App must block deletion while a run is active and must report any cross-backend partial failure.

If a partial-failure warning appears, do not assume deletion is complete. Retry, use the operating system’s clear-storage or delete-App controls, and reopen the App to verify that records do not return.

## What local deletion does not delete

Successful local deletion does not delete:

- files previously exported, shared, emailed, uploaded, printed, or copied;
- copies retained by recipients, workplace systems, cloud storage, trash folders, synced devices, or independent backups;
- support email held by GoodUse Studios;
- Apple or Google account, billing, or transaction records; or
- the one-time store purchase, which may remain restorable.

GoodUse Studios cannot delete copies it does not possess.

## Device and cloud backups

The intended native configuration excludes the PressBench operational database from automatic operating-system or cloud application backup. This must be verified in each final signed build.

An exported file placed in Files, Downloads, email, cloud storage, messaging, workplace storage, removable media, or another destination may still be backed up by that destination. Users must manage those copies through the relevant service.

## Imports and restoration

Only restore a backup obtained from a trusted source. A malformed or incompatible backup is rejected without replacing current data. Purchase entitlement is kept separately and is not imported from an editable JSON file.

Restoring operational data does not prove that its setup values remain current, safe, or suitable. Review restored setups and current manufacturer or supplier instructions before use.

## Support information

To request access to, correction of, or deletion of support correspondence actually held by GoodUse Studios, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Data%20Request) with the subject **“PressBench Data Request.”**

We may need to verify the requester and may retain limited information where required for accounting, fraud prevention, security, an unresolved dispute, or another legal obligation.

For more detail, read the [Privacy Policy]({{ '/privacy/' | relative_url }}).
