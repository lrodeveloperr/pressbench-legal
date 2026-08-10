# PressBench Legal and Store Alignment Audit

**Audited artifact:** PressBench source v0.17.1  
**Audit date:** 10 August 2026  
**Provider:** Lateef Razaq-Oyetola carrying on business as GoodUse Studios, Ontario, Canada

## Conclusion

The local-first privacy and safety posture is strong, but the supplied artifact is **not yet commercially or legally release-ready**. The platform model is now confirmed—one-time Pro unlock that does not expire merely with time on iOS, auto-renewing Pro subscription on Android, and no ads—but the source implements only an unfinished Android-oriented entitlement bridge. The Android subscription currently unlocks a static offline creation ceiling and report exports without demonstrated recurring value. The policy set is a pre-release draft and must not be treated as proof that a native binary or store listing complies.

## Confirmed product facts

- Free Tier may add a setting while fewer than 3 operator-created settings are currently stored and add a batch while fewer than 5 batches are currently stored; deleting one reopens a slot. JSON backup and CSV export remain available.
- Pro is intended to permit creation of up to 1,000 operator-created settings and 1,000 batch records; PDF and XLSX report exports are gated by verified Pro.
- Local fields can contain job/customer labels, suppliers, SKUs, lots, material and design details, operating settings, outcomes, issues, corrections, timestamps, and notes.
- User-directed exports: JSON, CSV, XLSX, and PDF.
- Source claims: no account, cloud database, analytics SDK, or network permission.
- No advertising or tracking integration was identified in the supplied source.
- Purchase entitlement is deliberately excluded from editable backups.
- The App records operator input and does not inspect or control machinery or determine safe settings.

## Release blockers

### P0 — Remove actionable generic starter setpoints

The source says the App does not recommend safe or correct settings, yet it auto-installs “Factory Presets” containing generic actionable values, including 315°F for 15 seconds at medium pressure and 285°F for 10 seconds at medium pressure. A title saying “Verify Manufacturer” does not cure that product contradiction. Remove the operational values and rename the templates as blank starter examples before release; do not rely on a disclaimer to close this blocker.

### P0 — Implement the confirmed model and compliant Android recurring value

The source contains Subscribe and Restore Purchase language but no price, period, product ID, trial, or completed purchase service. Its own error copy says a verified store purchase service is unavailable in the web build.

Google Play requires subscriptions to provide sustained or recurring value. A static local creation-limit and report-export unlock is much closer to a one-time product.

**Confirmed model:** iOS uses a one-time non-consumable Pro unlock that does not expire merely with time and has no subscription; Android uses an auto-renewing Pro subscription; neither platform uses ads. The Android release must define and implement genuine sustained or recurring value with exact billing terms. If that recurring value is not added, the Android subscription remains exposed to rejection and should be changed to a one-time product before submission.

### P0 — Implement and test the native purchase layer

Implement store product configuration, secure entitlement verification, restoration, pending purchase handling, cancellation/lapse behaviour, billing retry or grace states, refund/revocation handling, offline caching, and the no-data-loss rule. Test every state with store sandbox/test accounts.

### P0 — Put exact purchase facts before confirmation

The final iOS purchase screen must show the local one-time price, the fact that Pro does not expire merely with time, included features, restoration, and working Privacy and Terms links, with no subscription wording. The Android paywall must show the actual local price, currency, billing period, automatic renewal, recurring value, included features, cancellation method, expiry behaviour, and working Privacy and Terms links. Policies hosted elsewhere do not cure an incomplete paywall.

The current “Manage plan” control only reopens the subscribe/restore paywall; it has no manage or cancel route. Add a working platform management action for active subscribers or relabel the control until that action exists.

### P0 — Verify the final binaries

The attachment is HTML/JavaScript source, not a signed AAB or iOS archive. Before store declarations, inspect the final dependency graph, Android manifest, iOS entitlements and privacy manifest, backup settings, SDK behaviour, network traffic, and purchase integration.

### P0 — Add in-App legal access and assent

The audited interface exposes safety copy and data controls but no confirmed working links to Privacy, Terms, Purchases, Support, Data Choices, or third-party notices. Add accessible links in Data Management or About and from every purchase screen. Present the effective Terms and Privacy notice conspicuously in the release flow and record versioned affirmative acceptance where required. A Google Play subscription build must also provide an in-App link to an easy online management and cancellation method. Keep Safety available from the production-run flow.

### P0 — Implement the iOS non-consumable offer

The source UI is Android-subscription-oriented. The iOS build must replace Subscribe and Android-plan wording with a one-time non-consumable Pro purchase, non-expiring-with-time entitlement copy, and Restore Purchase. It must never display automatic-renewal or subscription-management language. Ensure store listing, code, and policies say the same thing.

### P0 — Make the paid creation ceiling truthful and enforce it everywhere

Free/Pro limits govern current stored counts and new-record creation, not lifetime creation or total storage. Deleting a record below its Free threshold reopens a slot. Restore can load as many as 1,000 settings and 1,000 batches without Pro; at or above a Free threshold, those records remain stored, viewable, editable or correctable, JSON-backupable, and CSV-exportable, while a new record of that type and PDF/XLSX report export remain blocked. Preserve and describe that no-data-loss rule.

Canonical starters are excluded from the displayed user-created count, but the hard recipe ceiling counts every row. With five starters installed, a default database can block creation at 995 operator-created settings while the UI shows `995 / 1000`. Make the physical ceiling exclude canonical starters or increase the raw ceiling accordingly. IndexedDB and normal UI creation paths otherwise check the intended record limit, but several compatibility-storage mutation and replacement methods do not independently enforce it. Centralise the invariant across every store backend, import, replacement, demo, batch, and setting mutation. Disclose or remove the separate 8 MB primary-store, 2 MB compatibility-store, and 1 MB per-record limits; otherwise paid users may be blocked far below the numerical ceiling despite available device storage.

## High-priority alignment items

### P1 — Correct absolute offline wording

“No network permission” and similar absolute claims can conflict with store billing, store licensing, user-opened legal pages, platform diagnostics, or enabled device backups. Use the accurate claim: **PressBench does not transmit production records to GoodUse Studios; user-directed exports and operating-system, device, cloud, or workplace backups may move copies.**

### P1 — Define expiry behaviour

The current runtime does not delete existing or restored records when entitlement is inactive. Those records remain stored, viewable, editable or correctable, JSON-backupable, and CSV-exportable; PDF/XLSX report generation is blocked. A new record of a type is blocked while its current stored count is at or above the applicable Free threshold; deleting records below that threshold reopens a slot. Verify that the final native wrappers preserve this behaviour for Android expiry, cancellation, billing failure, grace or hold states, and for refund, revocation, pending purchase, and offline verification on either platform. Test users already above both Free Tier limits.

### P1 — Complete third-party notices

The source embeds ExcelJS, JSZip, jsPDF, pako, browser buffer utilities, and modified Noto subsets. Preserve all embedded notices and generate a complete notice/SBOM file from the final locked dependencies. The current public notice is a human-readable summary, not a substitute for binary-level licence compliance.

### P1 — Correct misleading runtime labels

The dashboard says “Repeat a validated production setup,” but the repeat-last logic accepts a complete failure, rework, partial, Draft, or Trial record without requiring a successful or Verified result. Change this to **“Repeat a recorded setup”** and reserve “Verified” or “validated” for the documented evidence rule.

User-facing onboarding and backup text also drift between “PressBench” and the legacy name “Press Bench Log.” Keep the technical schema identifier if required, but make all visible product copy consistently say “PressBench.”

### P1 — Privacy and support operations

Keep a documented process for support-email access/deletion requests and delete resolved support correspondence on the stated schedule unless an exception applies. Do not ask users to email unredacted backups or production reports.

### P1 — Make delete-all verifiable across storage backends

Delete-all clears the active store and attempts to retire the alternate backend, but an alternate-backend failure can leave an older recovery copy and only display a warning. Make deletion clear and verify every local backend, or provide a reliable retry and verification flow. Keep the Data Choices page's warning until the final implementation proves atomic deletion.

### P1 — Market and language gate

Do not distribute into a jurisdiction until the effective policies and purchase disclosures meet its language and consumer-information rules. If Québec is included, obtain Québec-specific review of the French-first consumer-contract requirements before release. If any EU/EEA market is included, complete the privacy-controller, lawful-basis, international-transfer, consumer, and Digital Services Act trader disclosures before release.

The source contains dormant, currently unsupported locale strings that describe record capacity as “unlimited,” while the domain ceiling is 1,000 per record type. Keep those locales disabled until every pricing and capacity string is corrected and regression-tested.

## Store declaration judgment

If the final native apps preserve the audited local-only configuration and use only platform purchase services, Apple’s “Data Not Collected” response and Google Play’s no developer collection/sharing position may be supportable. This is a provisional inference, not a final declaration; platform definitions require evaluating all integrated code and final runtime behaviour.

## Primary official references

- [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/) — subscriptions must provide ongoing value; purchase terms must be clear.
- [Apple App Privacy management](https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy/) — privacy URL and accurate disclosures are required.
- [Apple Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)
- [Google Play Subscriptions policy](https://support.google.com/googleplay/android-developer/answer/9900533) — subscriptions require sustained or recurring value and clear terms.
- [Google Play Data safety guidance](https://support.google.com/googleplay/android-developer/answer/10787469)
- [Google Play Payments policy](https://support.google.com/googleplay/android-developer/answer/9858738)
- [Google Play subscription cancellation](https://support.google.com/googleplay/answer/7018481) — uninstalling does not cancel.
- [Google Play order management and refunds](https://support.google.com/googleplay/android-developer/answer/2741495) — eligible Play Console users can issue full or partial refunds.
- [Office of the Privacy Commissioner of Canada mobile-app guidance](https://www.priv.gc.ca/en/privacy-topics/ai-technology-and-innovation/mobile-and-digital-devices/mobile-apps/gd_app_201210/)
- [Québec Charter of the French language, section 55](https://www.legisquebec.gouv.qc.ca/en/document/cs/C-11?langCont=en#se:55)

## Final approval gate

Do not make the consumer pages effective or submit to either store until every P0 item is closed, the chosen pricing model is reflected byte-for-byte in the native builds, and the public URLs are live and tested without login.
