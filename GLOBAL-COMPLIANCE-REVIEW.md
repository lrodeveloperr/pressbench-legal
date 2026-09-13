# PressBench — Global Play & Privacy Compliance Review

**Review date:** 13 September 2026  
**Android release baseline:** `1.0.1`, version code 2  
**Source reviewed:** `lrodeveloperr/press-bench-android`

This is an engineering and store-readiness review, not a legal opinion for every jurisdiction. PressBench minimizes publisher processing: operational records remain on-device, there is no PressBench account or developer production database, Android backup/device transfer is disabled, and routine external services are Google Play Billing, the public legal site and user-selected export destinations.

## Google Play baseline

- Free users receive ten qualifying runs under the same completion-and-save rule used on iOS; no advertising SDK or ad inventory is included.
- Android PressBench Pro is a monthly Google Play subscription for unlimited runs and PDF/CSV reports. Google Play displays the current localized offer before purchase.
- Keep the public privacy policy and in-App legal links accessible without login.
- Reconfirm how Play Console expects Google Play Billing purchase history/status to be declared for the exact SDK and implementation.
- Declare **Contains ads: No**, **In-app purchases: Yes**, the actual adult target audience and unrestricted App access.
- Provide a working Google Play subscription-management route and clear recurring-benefit, billing-period and cancellation disclosures.
- Recheck target API, SDK policy status, permissions, 16 KB compatibility and the signed AAB before every release.

## Regional privacy considerations

For Canada, maintain accountability, clear purposes, meaningful consent, safeguards, access/correction, retention limits and a privacy-contact process. In the EEA and UK, confirm with qualified counsel whether an Article 27 EEA representative and/or UK representative is required for the actual establishment, targeting and monitoring facts. If required, appoint and publish the representative before distribution in that market.

For US states, Brazil, Japan, Australia, New Zealand, Switzerland, Türkiye, South Africa, South Korea, India and other markets, requirements vary with business thresholds and actual processing. Confirm applicable notices, consent/opt-out mechanisms, representatives or officers, language, security, retention and consumer disclosures. Exclude a market if a mandatory local obligation cannot be met.

## Consumer and subscription status

The Android subscription supplies recurring access to unlimited workflow usage and report generation. Google Play supplies the localized price and manages payment, renewal, cancellation and refunds. Keep benefits available throughout paid entitlement, preserve existing records after expiry, honor supported legacy purchases, and do not advertise a trial or offer unless it is active in Play Console.

The client-only entitlement implementation relies on periodic Play verification with a signed, bounded local continuity record that cannot extend its original verification window. This minimizes developer-held purchase data, but it is less resistant to delayed revocation than a production purchase-verification backend. Monitor fraud and refund risk; if a backend is later introduced, update the privacy policy, security model, Data Safety answers and retention/deletion rules before launch.

## Languages and market scope

The App is localized broadly while the legal site is currently English. Do not treat machine translation as qualified local legal review. Obtain local review where mandatory local-language consumer or privacy terms apply, or exclude the affected market until ready.

## Release rule

A worldwide distribution selection does not itself establish worldwide compliance. Re-run this review whenever PressBench changes an SDK, permission, data flow, account/cloud feature, monetization model, price, subscription benefit, report gate, entitlement system or target market.
