# PressBench Store Disclosures — Provisional Release Worksheet

**Source baseline:** v0.17.1, reviewed 10 August 2026.  
**Status:** Provisional until the final signed Android App Bundle and iOS archive are inspected.

## Intended public URLs

The intended GitHub Pages URLs are:

- Privacy: `https://lrodeveloperr.github.io/pressbench-legal/privacy/`
- Terms: `https://lrodeveloperr.github.io/pressbench-legal/terms/`
- Purchases: `https://lrodeveloperr.github.io/pressbench-legal/subscriptions/`
- Support: `https://lrodeveloperr.github.io/pressbench-legal/support/`
- Data choices: `https://lrodeveloperr.github.io/pressbench-legal/data-choices/`
- Safety: `https://lrodeveloperr.github.io/pressbench-legal/safety/`

These URLs are not approved store URLs until GitHub Pages is enabled, the pre-release banners are removed after final approval, and every route is verified without authentication.

## Apple App Privacy

Provisional answer for the audited local-only configuration:

- **Data collection:** “No, we do not collect data from this app.”
- **Tracking:** No.
- **Privacy Policy URL:** required; use the public Privacy URL above.
- **User Privacy Choices URL:** use the Data Choices URL above.

Use this answer only if the final iOS archive contains no analytics, advertising, crash-reporting, remote configuration, cloud sync, account, developer server, or other SDK that transmits accessible data off-device. StoreKit/App Store processing and any Apple-provided diagnostics must be reviewed in the final binary and App Store Connect configuration.

## Google Play Data safety

Provisional answer for the audited local-only configuration:

- No account creation.
- No production data collected by or shared with GoodUse Studios.
- No advertising or tracking.
- No developer analytics or crash-reporting SDK.
- Local records and user-directed exports are not developer collection merely because they exist on the device; review any Android backup configuration separately.
- Google Play may process purchases under its own service terms.

Do not submit “no data collected or shared” until the final AAB manifest, SDK list, network-security configuration, Android backup rules, and runtime traffic are verified. If any library transmits device, diagnostics, purchase, or usage data to a developer or third party, disclose the relevant data type, purpose, retention, and sharing status.

The App has no account, so Google’s in-App account-deletion requirement should not apply. The Data Choices page still provides a public explanation of local deletion.

## Permissions and platform features

The audited source does not require location, camera, microphone, contacts, Bluetooth, health, advertising ID, or broad shared-storage permission. Haptic and audio cues are outputs. Backup import, file save, and sharing should use user-initiated system pickers or share sheets.

Verify the final manifests and entitlements. Remove any permission or capability that is not essential.

## Monetisation declarations

Confirmed commercial structure:

- Android: limited Free Tier followed by an auto-renewing Pro subscription.
- iOS: limited Free Tier followed by a one-time non-consumable Pro unlock that does not expire merely with time and has no recurring charge.
- No ads.
- No trial unless one is deliberately configured and disclosed.

The Android paywall and store metadata must state the exact local price, billing period, automatic renewal, ongoing subscription value, cancellation method, and links to Privacy and Terms. The current static creation-ceiling and export unlock is exposed to Google Play’s recurring-value rule. The iOS purchase flow must contain no subscription or renewal wording.

Free/Pro limits govern current stored counts and new record creation rather than lifetime creation or total local storage. Deleting a record below its Free threshold reopens a slot. At or above a threshold, existing, restored, or lapsed records remain stored, viewable, editable or correctable, JSON-backupable, and CSV-exportable; a new record of that type and PDF/XLSX report generation remain gated. Store copy and the purchase screen must state that split exactly unless the released code is deliberately changed and re-audited. The iOS purchase has no recurring charge and does not expire merely with time; record and storage limits still apply.

## Store-listing factual claims

Permitted only if the final binary matches:

- local-first production settings and batch records;
- no login or cloud account;
- no ads or tracking;
- no developer analytics SDK;
- user-directed JSON, CSV, XLSX, and PDF exports;
- app does not control machinery or determine safe settings; and
- operator must verify current manufacturer instructions.

Avoid absolute claims such as “zero network activity” or “records never leave the device.” Prefer: **“PressBench does not transmit production records to GoodUse Studios. Your exports and any enabled operating-system, device, cloud, or workplace backups may move copies.”**

## Category, audience, and content

- Likely primary category: Business or Productivity.
- Intended audience: adult heat-press operators and production teams.
- Not directed to children.
- No user-to-user communication or uploaded user-generated content in the audited configuration.
- No medical, financial, government, or professional certification function.
- Safety disclaimer must be visible in-App before the first production run and remain accessible thereafter.

Store age-rating answers must be completed from the final questionnaire; do not use the legal adult-audience statement as a substitute for accurate content-rating answers.

## Final submission gate

Confirm the following from the signed binaries, not from this HTML source:

1. SDK inventory and third-party privacy practices.
2. Android permissions, data backup rules, and runtime traffic.
3. iOS entitlements, privacy manifest, required-reason APIs, and runtime traffic.
4. Product identifiers, price, period, entitlement restoration, and failure states.
5. Working in-App links to Privacy, Terms, Purchases, Support, Data Choices, and Safety.
6. Versioned Terms/Privacy presentation and any required assent; easy in-App subscription cancellation access where applicable.
7. Generic starter templates contain no unsafe actionable setpoints, and “validated” is used only where the verification rule actually passes.
8. The 1,000 operator-created-setting ceiling counts canonical starters separately, every storage path enforces the intended invariants, and the 8 MB / 2 MB / 1 MB internal data limits are either disclosed or removed.
9. iOS contains only the confirmed one-time non-consumable offer; Android contains only the confirmed auto-renewing subscription offer; neither build contains ads.
10. Delete-all clears and verifies every local storage backend, including failure and retry states.
11. Store declarations match the exact released version.
