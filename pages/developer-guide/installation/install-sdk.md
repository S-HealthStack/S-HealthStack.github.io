---
title: Installing the App SDK
sidebar: doc_sidebar
permalink: install-sdk.html
toc: false
---

Follow these instructions to install, build, and verify the app SDK.

> If you are installing the full stack, this installation requires successful prior completion of the [backend system installation](install-backend.md).

# Prerequisites

## I. Install OpenJDK 11

1. Set up and install OpenJDK 11 using the instructions at [https://openjdk.org/install/](https://openjdk.org/install/){:target="_blank"}.

## II. Install Android Studio 

1. Set up and install Android Studio on Windows, macOS, or Linux using the instructions at [https://developer.android.com/studio](https://developer.android.com/studio){:target="_blank"}.

## III. Clone the Repository

1. Clone the app SDK repository. 

   ```
   git clone https://github.com/S-HealthStack/app-sdk
   ```

# Build
<!-- Zain to check if detekt is supported -->

## IV. Prepare the Modules
1. Clean all modules.
   ```
   ./gradlew clean 
   ```

2. Build either all modules or just the kit.

   - To build all modules, including sample modules:

      ```
      ./gradlew build -x detekt
      ```

   - To build just the kit module and generate an android archive package (aar):

      ```
      ./gradlew :kit:build -x detekt
      ```

## V. Unit Test

1. Test either all modules or just the kit.

   - To test all modules, including samples:

      ```
      ./gradlew test
      ```

   - To test just the kit:

      ```
      ./gradlew :kit:test
      ```


## VI. Check the Coding Style

1. Use the [Compose API guidelines](https://github.com/androidx/androidx/blob/androidx-main/compose/docs/compose-api-guidelines.md){:target="_blank"} to check your coding style. The guidelines outline the patterns, best practices, and prescriptive style guidelines for writing idiomatic Jetpack Compose APIs. 

## VII. Create a Firebase Project

1. Follow the instructions at [https://firebase.google.com/docs/android/setup](https://firebase.google.com/docs/android/setup){:target="_blank"} to add a Firebase project to the Firebase account you created during backend system installation.

## VIII. Per App Configuration

After app creation, for each app you need to:

1. Register your app with your Firebase project by updating the ***\<repository\>*/app/google-service.json** configuration file.

2. For full-stack implementations only, associate your app with the backend system and portal study.

Refer to [Configuring the App Environment](../app-creation/configure-app.md) for details.

## IX. Reference Documentation

Refer to our [API reference](../docs/api-reference/API-Documentation.md) and [SDK reference](../docs/sdk-reference/SDK-Documentation.md) documentation for details on all the backend API endpoints and SDK packages.