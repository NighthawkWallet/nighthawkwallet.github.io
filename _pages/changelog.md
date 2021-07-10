---
layout: page
title: What's New
include_in_header: true
---

# Nighthawk Wallet Design & Development '21
## Updated July 10, 2021

| Feature/Issue  | % Complete | Status |
--- | --- | ---
|Auto-shielding (receive funds on T-addrs and send to Z-addrs) | 25% | Nighthawk iOS is live with Manual Shielding for Transparent funds & Nighthawk Android Auto-Shielding for every 1 ZEC received in T-address is under final testing phase |
|ZIP-321 Add Payment URI support + Deep Link integration | 0% | URI support and Deep Link integration to be compatible with ZecPages is planned |
|ZIP-316 NU5 support + Unified Addresses | 0% | Waiting on implementation in zcashd test-net https://github.com/zcash/zips/blob/master/zip-0316.rst |
|Publish Nighthawk Wallet on the F-Droid Store | 50% | Aim to have approval for "No Anti-features" flag, removed un-necessary Google dependencies, work in progress towards integrating builds within Fdroid Server after successful continuos integration with Bitrise https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/15 |
|New User onboarding & tutorial | Planned for Milestone 3 | Tis task will be started after the UX design changes with Unified Addresses is completed https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/30 |
|Optional backup of seed words | Planned for Milestone 2 | https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/29 |
|Support language translations for top 10 languages | 10% | Evaluated several language translation services, Planned Milestone 2 https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/28 |
|Resolve 0 balance bug on Android | Done | https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/27 |
|Add option to Rescan wallet to debug issues | Done | Rescan option added under Profile for easy debugging of issues https://github.com/zcash/zcash-android-wallet/issues/223 |
|View USD value of ZEC balance  | 50% | Initial Zcash balance polling via proxy server querying Gemini Exchange on a per minute basis was completed. An updated integration to get the ZEC/USD price via lightwalletd service is being developed. https://github.com/zcash/zcash-android-wallet/issues/231 |
|Update Transaction Details Screen  | Work in Progress | https://github.com/zcash/zcash-android-wallet/issues/239 |
|Refactor Send Transaction flow on Android  | Planned for Milestone 2 | https://github.com/zcash/zcash-android-wallet/issues/245 |
|Accessibility fixes on iOS | Done | Fixed device Home Screen issue https://github.com/zcash/zcash-ios-wallet/issues/252 |
|Add in-app message to notify users of any known issues with the app or the network | Done |  Updated Banner with Network & Auto-shielding statushttps://github.com/nighthawk-apps/nighthawk-wallet-android/issues/31|
|Integrate Flexa Spend SDK | 5% | Initial contact and Nighthawk requirements to not initialize the library till the user opts in shared with Flexa team, waiting on the availability of the release to start this work (target Milestone 2/3) https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/32 |
|Add exchange support  | 5% | Evaluated integration with MoonPay & Transak(limited to T-addresses), and looking forward for Zcash Thorchain Integration for Native Swap integration within Nightawk https://github.com/nighthawk-apps/nighthawk-wallet-android/issues/33 |
|Finish & Publish "We Accept Zcash" on App Store  | 0% | https://github.com/zcash-hackworks/we-accept-zcash-ios |
|UX Group Study | Planned October 2021 | Design Phase will begin following NU5 |
|Redesign App Theme and elements | 5% | Logo updated, Day/Night theme planned in Milestone 2 |

<br>

# Changelog

## **Version 1.0.19 *(2021-05-13)**
- Hotfix: Remove un-used flags during wallet creation. 

## **Version 1.0.18 *(2021-05-08)**
- Add the ability to rescan or wipe the wallet for troubleshooting.
- Fix issue when syncing transactions after sending MAX balance out of wallet.
- Update ECC dependencies.

## **Version 1.0.17 *(2021-03-31)**
- Switch price endpoint to api.lightwalletd.com

## **Version 1.0.16 *(2021-03-24)**
- Better handling around unsatisfied link errors.

## **Version 1.0.15 *(2021-03-21)**
- Fix block rescan error.

## **Version 1.0.14 *(2021-03-17)**
- Connect to lightwalletd.com service funded by ZOMG.
- Remove Google Services dependency.
- Support QR code scan on ZecPages.

## **Version 1.0.13 (2021-01-24)**
- Fix crash in magicsnakeloader.
- Handle NumberFormatException.
- Add donation address under Settings.

## **Version 1.0.12 (2021-01-20)**
- Fix crash when restoring wallet.

## **Version 1.0.11 (2021-01-18)**
- Add price query via Nighthawk Server Cached Proxy.
- Update dependencies & Zcash-SDK.

## **Version 1.0.10 (2021-01-01)**
- Fix: Use LockBox Server Settings.
- Update dependencies for material and lottie libs.

## **Version 1.0.9 (2020-12-20)**
- New: Upgrade to the latest Zcash SDK.
- New: Implement ZIP-313, reducing the default fee from 10,000 to 1,000 zats.
- New: Adds authentication prior to viewing backup seed words.
- Fix: Repaired the upgrade flow, which could not reorg because of missing birthday height
- Fix: Repaired create wallet flow which was being covered by the loading screen
- Fix: Authentication bugs on older devices that were preventing sends and mishandling cancels.
- Fix: Users can now upgrade from seed-only prior versions without crashing or needing to restore.
- Fix: Improved internal metrics for troubleshooting issues.
- Fix: Correct race condition when launching the app
- Fix: Display loading screen while waiting for app to initialize
- Add translations for Spanish, Italian, Korea, Russian and Chinese

## **Version 1.0.8 (2020-11-15)**
- Enable deshielding ZEC transaction z -> t
- Update dependencies and gradle build setup
- Simplify Send transaction flow
- Fix importing of wallets with birthday heights after 1,000,000 blocks
- Minor UI Niceties

## **Version 1.0.7 (2020-08-29)**
- Switch default lightwalletd server to Nighthawk's own no-Logs, non-US based server
- Theming & copy updates
- Update dependencies
- Fix MaterialButton styling

## **Version 1.0.6 (2020-08-24)**
- Update to latest librustzcash SDK lib & android dependencies
- Fix New Wallet creation
- Fix SideShift affiliate url
- Fix Donate to Nighthawk copy address
- Add Biometric support
- Add shortcut for auto-fill amount for memo
- Improve compatibility with memo reply-to formats
- Support precise birthday heights for faster restore
- Switch to Reply-To standard for memos

## **Version 1.0.5 (2020-08-01)**
- Revamp Wallet UI, add Zash info link
- Update donation address, add SideShift.ai integration
- Default to ZecWallet server, Thanks @adityapk!
- Upgrade NDK version, Strigify resources and optimize layouts.

## **Version 1.0.4 (2020-07-22)**
- Fix a bug in resolving transaction history

Version 1.0.3 (2020-07-20)**
- New Settings screen with the ability to point to a lighthttpd server of user's choice.
- Switch to "Reply-To" from "sent-from" because the former underscores the idea that the given address is not necessarily the address that originated the transaction.
- Update dependencies and secure the lighthttpd setting via EncryptedSharedPreferences
- Add Donation address

## **Version 1.0.2 (2020-07-09)**
- Remove Feedback Module, Crashlytics & Mixpanel libs
- Fix SSL handshake failure
- Fix for bad QR scan & Navigation after sending ZEC.

## **Version 1.0.1 (2020-07-01)**
- Resolved a critical bug where an EU locale or alternative keyboards defaults to , for decimal on the Send screen and the mobile SDK ignores the denominator on the input screen
- Added further instances of Nighthawk branding (h/t @imichaelmiers)
- Fixes the cursor position resetting to 0 when there's a space on either side of the address field (h/t @CrystalPony)
- Updates dependencies

## **Version 1.0.0 (2020-06-16)**
- Repackage to Nighthawk Wallet
- Removed Analytics Reporting
- Changed package naming & logo
- Removed Send Feedback
- Block sending tx to t addr

## **Version 1.0.0-alpha23 (2020-02-21)**
- Fix: reorg improvements, squashing critical bugs that disabled wallets
- New: extend analytics to include taps, screen views, and send flow.
- New: add crash reporting via Crashlytics.
- New: expose user logs and developer logs as files.
- New: improve feature for creating checkpoints.
- New: added DB schemas to the repository for tracking.
- Fix: numerous bug fixes, test fixes and cleanup.
- New: improved error handling and user experience

## **Version 1.0.0-alpha17 (2020-02-07)**
- New: implemented wallet import
- New: display the memo when tapping outbound transactions
- Fix: removed the sad zebra and softened wording for sending z->t
- Fix: removed restriction on smallest sendable ZEC amount
- Fix: removed "fund now"
- New: turned on developer logging to help with troubleshooting
- New: improved wallet details ability to handle small amounts of ZEC
- New: added ability to clear the memo
- Fix: changed "SEND WITHOUT MEMO" to "OMIT MEMO"
- Fix: corrected wording when the address is included in the memo
- New: display the approximate wallet birthday with the backup words
- New: improved crash reporting
- Fix: fixed bug when returning from the background
- New: added logging for failed transactions
- New: added logic to verify setup and offer explanation when the wallet is corrupted
- New: refactored and improved wallet initialization
- New: added ability to contribute 'plugins' to the SDK
- New: added tons more checkpoints to reduce startup/import time
- New: exposed logic to derive addresses directly from seeds
- Fix: fixed several crashes

## **Version 1.0.0-alpha11 (2020-01-15)**
- Initial ECC release

## **Version 1.0.0-alpha03 (2019-12-18)**
- Initial internal wallet team release
