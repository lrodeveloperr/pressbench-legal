---
layout: default
title: Third-Party Software Notices
nav_title: Notices
permalink: /third-party-notices/
---

# Third-Party Software Notices

**Release baseline: PressBench Android 1.0.0-closed-v14, 25 August 2026**

PressBench includes third-party software. Each component remains owned by its respective rights holder and is governed by its applicable licence and service terms. Nothing in the PressBench Terms limits rights granted by an applicable open-source licence.

The reviewed Android build directly declares dependencies on:

- AndroidX Core KTX;
- AndroidX Activity Compose;
- Jetpack Compose UI;
- Jetpack Compose UI Tooling Preview; and
- Jetpack Compose UI Tooling in debug builds.

These AndroidX components are generally provided under the Apache License 2.0. Kotlin, the Android Gradle plugin, the Compose compiler/plugin and transitive build/runtime components remain subject to their respective licences and terms.

The reviewed build does **not** directly declare Google Play Billing, Google Mobile Ads, Google UMP, AndroidX Navigation, Material 3, Material Icons, kotlinx.coroutines or JUnit/AndroidX Test as App dependencies.

The exact transitive inventory can change when dependencies are updated. Release engineering should retain the dependency report and build files for each published version and regenerate these notices when a dependency or version changes.

For a licensing question, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Open%20Source) with the subject **PressBench Open Source**.
