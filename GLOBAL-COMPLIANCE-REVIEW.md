# PressBench — Global Play & Privacy Compliance Review

**Review date:** 25 August 2026
**Release baseline:** Android `1.0.0-closed-v16-native`, version code 1403

This is an engineering/store-readiness review, not legal advice for every jurisdiction. PressBench minimizes publisher processing: operational records remain on-device, there is no PressBench account or cloud database, Android backup/device transfer is disabled, and routine external services are limited to Google Mobile Ads/UMP, the public legal site and user-chosen external apps.

## Google Play baseline

- Keep the public privacy policy and in-App legal links accessible without login.
- Declare Google Mobile Ads data in Data Safety even though PressBench production records remain local.
- Declare **Contains ads: Yes**, **In-app purchases: No**, adult target audience and unrestricted App access.
- The closed-test build has no Play Billing dependency or purchase/subscription UI.
- Use only official Google test ad identifiers in testing. Do not publish a production release with test IDs.
- Request ads only after UMP permits it, expose privacy options when required, and keep the `npa=1` signal.
- Recheck target API, SDK policy status, permissions and 16 KB compatibility from the exact signed AAB before every release.

## Regional privacy considerations

For Canada, maintain transparency, appropriate purposes/consent, safeguards, retention limits and a rights/contact process. In the EEA and UK, the principal risk is advertising consent: configure applicable Google-certified consent messaging and confirm with qualified counsel whether an Article 27 EEA representative and/or UK representative is required for the actual establishment, targeting and monitoring facts. If required, appoint and publish the representative before distribution in that market.

For US states, Brazil, Japan, Australia, New Zealand, Switzerland, Türkiye, South Africa, South Korea, India and other markets, requirements vary with business thresholds and actual processing. Confirm applicable notices, consent/opt-out mechanisms, representatives/officers, language, security, retention and consumer disclosures. Temporarily exclude a market if a mandatory local obligation cannot be confirmed.

## Consumer and commercial status

This build is free, shows only Google test ads and offers no purchase or subscription. A future paid ad-free option requires a separate billing implementation, Play product/base plan, localized Play price, entitlement and restoration lifecycle, cancellation access, updated legal/store disclosures and regional merchant/tax checks. An internal planning price is not a public offer.

## Languages and market scope

The App and listing may be localized while this legal site is English. Do not treat machine translation as legally reviewed local terms. Obtain qualified local review where local-language legal documents are mandatory or exclude the affected market until ready.

## Release rule

A global distribution selection does not prove global compliance. Re-run this review whenever the App adds or changes an SDK, permission, data flow, account/cloud feature, ad format, purchase, price or target market.
