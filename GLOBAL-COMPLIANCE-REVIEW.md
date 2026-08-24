# PressBench — Global Play & Privacy Compliance Review

**Review date:** 24 August 2026  
**Release baseline:** Android 1.0.0 / package `com.goodusestudios.pressbench`

This is an engineering/store-readiness review, not a legal opinion for 175 jurisdictions. PressBench intentionally minimizes direct publisher processing: production data stays on-device, there is no PressBench account/cloud database, sensitive Android permissions are not requested, and the only routine external services are Google Mobile Ads/UMP and Google Play Billing.

## Google Play baseline

The Android release must keep these declarations synchronized with the signed AAB:

- Privacy policy: public HTTPS/HTML URL, accessible without login, and linked in-app.
- Data safety: include data transmitted by Google Mobile Ads and Play Billing; do not declare “no data collected/shared” merely because production records are local.
- Contains ads: **Yes**.
- Target audience: **18+ / adults** only, if that matches the store listing and marketing.
- App access: no reviewer credentials required.
- Content rating: complete IARC questionnaire accurately.
- Subscription: `remove_ads_monthly`, auto-renewing monthly; only recurring benefit is removal of the banner while active; local price from Google Play; cancellation/management link in Settings.
- Ads: persistent banner only; no interstitial/app-open baseline; never position ads to cause accidental clicks or impair run controls.
- Target API: 36 for the 31 August 2026 Play requirement.
- 16 KB: test the signed bundle and native SDKs now. Google currently states that API 35+ apps must support 16 KB page sizes for Play updates from 1 February 2027.
- SDK responsibility: re-check the exact versions of Google Mobile Ads, UMP, Billing and all transitive SDKs before every release.

## Privacy baseline by region

### Canada

PIPEDA and any applicable provincial laws require transparency, appropriate purposes/consent, safeguards, retention limits, access/correction mechanisms, and accountability for service providers. PressBench’s policy identifies the operator/privacy contact, local-only production data, Google service processing, retention, security, and user controls.

### EEA

If EU GDPR/ePrivacy rules apply, the principal PressBench risk is advertising/consent rather than the local production database. Google UMP must be configured with the required certified CMP message(s), ads must not be requested before `canRequestAds`, and the Privacy Options entry point must be shown when UMP says it is required. Confirm with counsel whether Article 27 requires an EEA representative for the actual GoodUse Studios processing model; if yes, publish the representative’s contact details before enabling EEA distribution.

### United Kingdom

Apply the same discipline under UK GDPR/PECR and Google’s UK consent requirements. Confirm whether a UK representative is required for the actual processing/targeting model and publish the details before UK distribution if so.

### United States

State privacy laws apply based on state, activity and statutory thresholds. Do not assume CCPA/CPRA or another state law applies or does not apply without checking the business thresholds and advertising practices. Configure Google Privacy & Messaging/UMP for applicable US-state messages, maintain the global privacy notice, and honor any legally required opt-out/rights route for data GoodUse Studios actually controls.

### Brazil

LGPD can apply to processing connected with individuals in Brazil. Maintain clear purposes, lawful processing, security, retention/deletion, and rights/contact information. Confirm any local representative/officer obligations that apply to the actual business size and processing model.

### Japan

APPI privacy principles may apply to personal information handled in Japan. Separately, because PressBench sells an in-app subscription, Google Play notes that Japan’s Specified Commercial Transactions Act can require the business operator’s name, physical address and telephone number to be displayed through the required Play/Payments surface or compliant disclosure page.

### Australia / New Zealand / Switzerland / Türkiye / South Africa / South Korea / India and other markets

These markets have privacy/consumer regimes that can impose notice, security, rights, retention, transfer, local-language, representative/officer, or merchant-disclosure duties depending on thresholds and the actual processing. The PressBench technical baseline is designed to minimize exposure, but it is not a substitute for jurisdiction-specific legal advice. If a local obligation cannot be confirmed before launch, exclude that market temporarily rather than making a false compliance claim.

## Consumer / merchant disclosures

Because PressBench monetizes through a Play subscription, the Google Payments profile/merchant information must be accurate. Google states that monetizing developer accounts display the full legal address on Google Play. Keep the developer/merchant identity consistent with the Terms and Privacy Policy.

For the EEA, complete Play’s tax/compliance classification for the subscription (Digital Content vs Service; Google says “Service” may be selected if in doubt, but the developer remains responsible for the classification). Complete any trader/consumer information Play requests.

For Japan, verify the required operator name, public address and telephone number before enabling paid distribution.

## Languages

The app UI is localized, but the legal site is currently English. Store policy does not by itself turn machine-translated legal text into legally reliable local terms. Before relying on translated Terms/Privacy as a contract or statutory notice in a jurisdiction that requires local-language documents (for example, potentially Quebec/French consumer contexts), obtain a legally reviewed translation or exclude that jurisdiction until ready.

## Release rule

A “global” checkbox in Play Console does not prove compliance with every law. Ship only to markets for which the Play account/merchant details, privacy/consent configuration, local-language requirements, representatives (if required), taxes, and paid-product disclosures have been completed. Re-run this review whenever the app adds a new SDK, permission, data flow, account/cloud feature, ad format, or paid feature.
