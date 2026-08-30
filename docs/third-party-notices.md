---
layout: default
title: Third-Party Software Notices
nav_title: Notices
permalink: /third-party-notices/
---

# Third-Party Software Notices

**Release baselines: PressBench Android 1.0.0-closed-v16-native and PressBench iOS 0.22.0 TestFlight profile, 30 August 2026**

PressBench includes third-party software. Each component remains owned by its respective rights holder and is governed by its applicable licence and service terms. Nothing in the PressBench Terms limits rights granted by an applicable open-source licence.

The reviewed Android build directly declares dependencies on:

- AndroidX Core KTX;
- AndroidX Activity Compose;
- AndroidX Lifecycle;
- AndroidX DataStore;
- Jetpack Compose UI;
- Material 3 and Material Icons;
- Google Mobile Ads SDK 25.4.0;
- Google User Messaging Platform SDK 4.0.0;
- JUnit for unit tests; and
- Jetpack Compose UI Tooling in debug builds.

These AndroidX components are generally provided under the Apache License 2.0. Kotlin, the Android Gradle plugin, the Compose compiler/plugin and transitive build/runtime components remain subject to their respective licences and terms.

The reviewed Android build does **not** directly declare Google Play Billing or AndroidX Navigation. Google Mobile Ads and UMP are subject to Google's applicable SDK and service terms in addition to any included software licences.
The iOS TestFlight profile directly uses Apple StoreKit 2, AuthenticationServices, iCloud key-value storage, Google Mobile Ads SDK 13.9.0 and Google UMP SDK 3.1.0 through Google’s Swift Package Manager distributions. Apple frameworks and services are governed by Apple’s platform terms. The Google SDKs are subject to Google’s applicable SDK and service terms and include transitive software and privacy manifests.


The exact transitive inventory can change when dependencies are updated. Release engineering should retain the dependency report and build files for each published version and regenerate these notices when a dependency or version changes.

For a licensing question, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Open%20Source) with the subject **PressBench Open Source**.
