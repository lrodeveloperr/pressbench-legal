# PressBench — Pre-release Legal, Safety, Privacy, and Support Drafts

Pre-release legal and support drafts for **PressBench**, a local-first heat-press setup, run, batch-record, analytics, and export utility. These files are private working drafts and are not yet the effective public policies.

- Provider: **Lateef Razaq-Oyetola carrying on business as GoodUse Studios**, Ontario, Canada
- Support and privacy contact: [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Support)
- Logic baseline: **PressBench v0.21.2**, reviewed 12 August 2026
- Free Tier: **3 saved setups and 10 saved batches**
- Paid model: **one-time US$4.99 base-price, geopriced non-consumable unlock on both iOS and Android**
- Advertising and subscriptions: **none**

## Consumer-facing drafts

- [Privacy Policy](docs/privacy.md)
- [Terms of Use](docs/terms.md)
- [Purchases, Paid Access, and Refunds](docs/purchases.md)
- [Support](docs/support.md)
- [Heat-Press Safety Notice](docs/safety.md)
- [Local Data, Backup, Export, and Deletion](docs/data-choices.md)
- [Accessibility Statement](docs/accessibility.md)
- [Third-Party Software Notices](docs/third-party-notices.md)

## Internal release materials

- [Legal and Store Alignment Audit](LEGAL-ALIGNMENT-AUDIT.md)
- [Store Disclosures Worksheet](STORE-DISCLOSURES.md)
- [Pricing Review](PRICING-REVIEW.md)

## Architecture reflected in the drafts

The audited logic requires no account, GoodUse Studios cloud database, advertising, analytics SDK, tracking SDK, remote push token, or equipment connection. Operational records remain on the device. Notifications are optional and generic. Manual JSON, CSV, PDF, and XLSX files are not encrypted by PressBench. Store services may process purchase and entitlement information; voluntary support email is received by GoodUse Studios.

## Release condition

This private repository cannot itself serve as the public privacy-policy URL required by Apple and Google. Before release:

1. verify the final signed Android and iOS applications, native wrappers, SDKs, permissions, entitlements, privacy manifests, backup exclusions, notifications, runtime traffic, and purchase lifecycle;
2. confirm the exact store products, geographic prices, tax settings, trader details, and refund behaviour;
3. publish approved policies at stable public URLs accessible without authentication;
4. provide working in-App links and versioned legal presentation;
5. complete all required store privacy and consumer disclosures;
6. provide required translations before offering the App in the relevant storefront; and
7. replace draft dates with effective dates only after approval.

If the final build adds a server, account, analytics, crash reporting, advertising, remote push, cloud synchronization, equipment connectivity, or a different payment model, re-audit the policies before publication.

Copyright © 2026 Lateef Razaq-Oyetola carrying on business as GoodUse Studios. All rights reserved, except for third-party components governed by their own licences.
