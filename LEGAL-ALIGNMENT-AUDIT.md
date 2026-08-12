# PressBench Legal and Store Alignment Audit

**Audited logic:** PressBench v0.21.2 dated 12 August 2026  
**Audit date:** 12 August 2026  
**Provider:** Lateef Razaq-Oyetola carrying on business as GoodUse Studios, Ontario, Canada  
**Status:** Conditional pre-release pass for the logic; final native applications and store configuration remain unapproved.

## 1. Bottom line

The v0.21.2 logic materially improves the legal posture and closes the central defects identified in the earlier v0.17.1 review:

- starter templates contain structure rather than generic operating setpoints;
- the App distinguishes “Source checked” from “Proven on this setup” and does not present either as certification;
- both platforms use one-time, non-consumable purchases rather than an Android subscription;
- the Free Tier is 3 saved setups and 10 saved batches;
- the US price anchor is US$4.99 on both platforms with store geographic pricing;
- current Terms, safety acknowledgement, privacy-notice presentation, and temperature-unit confirmation are required before new operational work;
- existing records, deletion, correction, JSON backup, and CSV export remain available under the defined continuity rules;
- operational records remain local;
- manual exports are explicitly unencrypted;
- optional notifications are generic and use no remote push token;
- active and reserved work is protected from entitlement changes;
- restore requires a validated target and a durable pre-restore recovery point; and
- delete-all coordinates both local storage backends and reports partial failure.

The consumer policy set is now aligned to those facts. It must remain marked as a draft until the native wrappers, store products, public URLs, translations, and final binaries are verified.

## 2. Confirmed logic facts

### Product and access

- Free Tier: 3 saved setups and 10 saved batches.
- iOS product: pressbench_unlimited_lifetime_ios.
- Android product: pressbench_unlimited_lifetime_android.
- Both products: one-time, non-consumable; no renewal or subscription.
- US base-price anchor: US$4.99; store geographic pricing enabled.
- Paid physical ceilings: 1,000 saved setups and 1,000 saved batches.
- Premium reports and advanced analytics require paid access.
- JSON backup and CSV export remain available without paid access.

### Privacy architecture

- No PressBench account.
- No GoodUse Studios operational cloud or synchronization.
- No advertising, tracking SDK, analytics SDK, or remote push token required by the logic.
- Routine network boundary is limited to store entitlement.
- Operational database is required to be excluded from automatic operating-system backup.
- Manual JSON backup is not encrypted.
- Notification content is generic and excludes job references.
- No equipment connection, control, or measurement.

### Safety and evidence

- Structural starters contain no numerical operating values.
- A run uses a frozen setup snapshot and explicit current-instruction acknowledgement.
- “Source checked” and “Proven” are independent local evidence descriptions.
- Operational edits reset proof.
- App timing is a convenience aid, not a safety alarm.
- Historical batches preserve the values actually recorded.

## 3. Consumer-document assessment

The updated drafts cover:

- privacy and local-data handling;
- Terms of Use and licence;
- one-time purchase, restoration, and refund rules;
- heat-press safety;
- support and privacy requests;
- local backup, export, restore, and deletion;
- accessibility positioning; and
- third-party software notices.

The policy correctly says that users may place personal information in local fields while GoodUse Studios does not receive those operational records. It separately discloses support email, store records, website hosting, recipients, legal grounds, retention, international processing, and rights.

The purchase policy does not call the product uncapped or promise perpetual support. Store product identifiers containing “unlimited_lifetime” must not be displayed as consumer claims.

## 4. Remaining release blockers

### P0 — Final native privacy and security inspection

Inspect each signed Android App Bundle and iOS archive for:

- exact SDK and dependency inventory;
- runtime network destinations and payloads;
- advertising, analytics, diagnostics, crash reporting, remote configuration, or telemetry;
- Android permissions, backup rules, data-extraction rules, Billing integration, and notification behaviour;
- iOS entitlements, privacy manifest, required-reason APIs, StoreKit integration, backup exclusion, and notifications;
- App database and export-file locations;
- legal links and assent behaviour; and
- deletion across every storage backend.

“No data collected” store answers are conditional on this inspection.

### P0 — Store product verification

Confirm:

- both product identifiers exist and have the correct one-time product type;
- the US base price is US$4.99 and geographic storefront prices are configured;
- the paywall says one time and includes no subscription, renewal, or cancellation wording;
- purchase, pending, restored, refunded, revoked, wrong-product, wrong-account, offline, and response-loss states;
- Google Play purchases are acknowledged within Google’s required period;
- StoreKit 2 current entitlements and transaction updates process refunds and revocations;
- a temporary offline state does not revoke a verified entitlement; and
- a refund or revocation never deletes operational records.

If the products have not yet been created, consider less absolute identifiers such as pressbench_pro_onetime_ios and pressbench_pro_onetime_android. Existing product identifiers may be difficult or impossible to rename after store creation.

### P0 — Public legal URLs

The repository is intentionally private and therefore cannot serve as the store privacy-policy or support URL.

Before submission:

- publish approved consumer policies at stable HTTPS URLs accessible without authentication;
- ensure the Google privacy URL is active, public, non-geofenced, non-editable, and not a PDF;
- add an easily accessible Privacy link inside both applications;
- add working Terms, Purchases, Support, Data Choices, Safety, and third-party-notice links;
- verify every route on a clean device and unsigned-in browser; and
- keep the private audit and internal release notes out of the public policy site.

### P0 — Legal version alignment

The logic currently uses APP-018-TERMS-v2, APP-018-SAFETY-v2, and APP-018-PRIVACY-v2. The updated drafts materially change pricing and privacy wording. Before release, assign final effective versions—normally v3—and ensure the native applications present and record the matching versions.

Privacy-policy presentation is notice, not blanket consent. Terms and safety acknowledgement remain separate. Any future processing that legally requires consent needs its own informed choice.

### P0 — Trader and contact facts

Confirm before publication:

1. full business mailing address and postal code;
2. public business telephone number where required;
3. exact legal/trader name in Apple and Google;
4. bundle and package identifiers;
5. support-email provider and account safeguards;
6. whether the 24-month support-retention schedule will be operationally followed;
7. Apple/Google family-sharing settings;
8. store tax categories; and
9. countries and languages included at launch.

### P0 — Language and market gate

Do not enable a storefront until the effective policies, purchase disclosures, safety text, and required consumer information are available in the language and form required there.

For Québec, provide the French version of predetermined consumer terms before a user expressly chooses another language and complete a Québec distance-contract review.

For EU distribution, complete Digital Services Act trader verification and publish required trader contact information. Preserve mandatory digital-content conformity, update, remedy, and withdrawal-law disclosures applicable to the specific store transaction.

Assess whether an EU or UK representative is required for any personal information GoodUse Studios actually receives. The operational database itself remains on-device and is not received by GoodUse Studios.

### P1 — Third-party licensing

The v0.21.2 logic-only file does not establish the dependencies used in the final native applications. Generate a software bill of materials and exact third-party notice file from each locked release build. Confirm whether earlier web-runtime components such as ExcelJS, JSZip, jsPDF, pako, buffer utilities, and modified Noto fonts remain before naming them publicly.

### P1 — Accessibility claims

Keep the accessibility page as an objective and feedback channel until the native applications and exports have been tested. Do not claim WCAG or platform-standard conformance without evidence.

### P1 — Support operations

Implement a support procedure that:

- restricts account access;
- avoids requesting operational backups or unnecessary personal information;
- records and fulfils applicable access, correction, and deletion requests;
- applies the stated retention schedule;
- preserves records only where a documented exception applies; and
- escalates suspected privacy or security incidents.

## 5. Store privacy judgment

### Apple

A provisional “Data Not Collected” answer is supportable only if the final application and integrated third parties do not transmit accessible data off-device. Apple states that information processed only on-device is not collected for its App Privacy disclosure framework.

### Google Play

A provisional “No data collected” and “No data shared” answer is supportable only after final AAB, SDK, manifest, backup, and runtime-traffic verification. A privacy policy and Data Safety form are still required even for an app reporting no collection.

The App has no account creation, so the online account-deletion requirement should not apply. Local-data deletion must still remain functional and documented.

## 6. Primary sources

- [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- [Apple App Privacy Details](https://developer.apple.com/app-store/app-privacy-details/)
- [Apple App Store privacy management](https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy/)
- [Apple EU Digital Services Act trader requirements](https://developer.apple.com/help/app-store-connect/manage-compliance-information/manage-european-union-digital-services-act-trader-requirements/)
- [Apple StoreKit Transaction documentation](https://developer.apple.com/documentation/storekit/transaction)
- [Google Play Data Safety guidance](https://support.google.com/googleplay/android-developer/answer/10787469)
- [Google Play one-time purchase lifecycle](https://developer.android.com/google/play/billing/lifecycle/one-time)
- [Google Play refund process](https://support.google.com/googleplay/answer/2479637)
- [PIPEDA](https://laws-lois.justice.gc.ca/eng/acts/p-8.6/FullText.html)
- [Office of the Privacy Commissioner of Canada mobile-app guidance](https://www.priv.gc.ca/en/privacy-topics/ai-technology-and-innovation/mobile-and-digital-devices/mobile-apps/gd_app_201210/)
- [EU General Data Protection Regulation](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [EU Digital Content Directive](https://eur-lex.europa.eu/eli/dir/2019/770/oj/eng)
- [Québec Charter of the French Language, section 55](https://www.legisquebec.gouv.qc.ca/en/version/cs/C-11?code=se%3A55&langCont=en)
- [Québec Consumer Protection Act](https://www.legisquebec.gouv.qc.ca/en/document/cs/P-40.1)
- [Competition Act, section 52](https://laws-lois.justice.gc.ca/eng/acts/c-34/section-52.html)

## 7. Approval status

**Logic-level legal status:** conditional pass.  
**Consumer-policy status:** aligned pre-release drafts.  
**Store-submission status:** not approved until every P0 gate above is closed.  
**Worldwide-compliance claim:** not made; launch remains jurisdiction- and release-specific.
