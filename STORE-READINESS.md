# PressBench Android 1.0.0 — Store Readiness Gate

**Status:** code/legal baseline prepared; blocked on owner-supplied release credentials, public legal hosting, final AAB inspection, and Play Console declarations.

## First-use flow

1. Welcome: one-screen explanation of Setup → First piece → Production → Result.
2. Safety, Terms & Privacy: links to Privacy Policy, Terms, and Safety Notice; explicit Terms acceptance and Safety acknowledgement.
3. After acceptance, Google UMP is initialized. A Google consent form appears only when Google reports that one is required.
4. No account, login, permissions carousel, marketing carousel, or forced purchase screen.

## In-App legal/privacy wiring

Settings contains:

- Privacy choices (only when Google UMP requires an entry point);
- Privacy Policy;
- Remove ads;
- Manage subscription for active subscribers;
- Restore Purchases;
- Terms of Use;
- Safety Notice;
- Local Data & Deletion;
- Third-Party Notices;
- Support; and
- Delete Local Data.

## Owner-supplied items still required

- Public legal URL: enable a publicly reachable GitHub Pages site for `pressbench-legal` (the repository itself does not have to be public if the account supports public Pages from a private repository), or provide another public HTTPS host.
- Production AdMob App ID.
- Production AdMob banner ad-unit ID.
- Confirm Google Play subscription product ID `remove_ads_monthly`, activate a monthly base plan, and choose/store prices. Do not configure a trial unless desired and disclosed.
- Play release/upload signing credentials must be configured privately in the build environment; do not send private keys/passwords in chat or commit them.
- Confirm developer account type and creation date to determine the 12-testers/14-days gate.
- Confirm the Play developer display name and whether GoodUse Studios is the public merchant/developer name.
- Confirm `lrodeveloperr@gmail.com` remains the public support/privacy address.
- For paid distribution in Japan: provide/verify the business operator’s public physical address and telephone number in the Google Payments/Play surfaces required for the account.
- Confirm intended target audience is 18+ only.
- If distributing throughout the EEA/UK, obtain legal advice on whether an Article 27 EU representative and/or UK representative is required for the actual processing/targeting model and provide representative contact details if applicable.
- Supply/confirm store assets after the final native build: icon, 1024×500 feature graphic, phone screenshots, localized store title/short description/full description.

## Final binary-only checks

Do not mark the release complete until the signed AAB is available and these are verified from that artifact:

- manifest and merged permissions;
- SDK/dependency inventory;
- no Advertising ID permission;
- network traffic matches disclosures;
- real AdMob IDs, UMP behaviour, and non-personalized publisher setting;
- Play Billing purchase, restore, cancellation link, lapse/refund states;
- 16 KB page-size compatibility (test now; Google currently makes this a release-blocking update requirement for API 35+ apps from 1 February 2027);
- target API 36;
- crash-free launch in light/dark, LTR/RTL, and representative long-translation locales;
- first-use links open publicly;
- deletion clears local production data;
- active-run recovery after process death;
- banner never covers or crowds controls;
- Play Data safety answers match the final SDK behaviour.
