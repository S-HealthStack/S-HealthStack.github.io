---
title: Installing the App SDK
sidebar: doc_sidebar
permalink: install-sdk.html
toc: false
---

Follow these instructions to install, build, and verify the app SDK.

> If you are installing the full stack, this installation requires successful prior completion of the [backend system installation](install-backend.md).

# Prerequisites

## I. Install OpenJDK 17

1. Set up and install OpenJDK 17 using the instructions at [https://openjdk.org/install/](https://openjdk.org/install/).

## II. Install Android Studio 

1. Set up and install Android Studio on Windows, macOS, or Linux using the instructions at [https://developer.android.com/studio](https://developer.android.com/studio).

## III. Clone the Repository

1. Clone the app SDK repository (we recommend cloning into the same **INSTALL_PATH** as the backend-system so app-sdk and backend-system are at the same level)

   ```
   git clone https://github.com/S-HealthStack/app-sdk.git
   ```

# Build

## IV. Prepare the Modules

```
cd app-sdk
```

1. Clean all modules.

   (Mac users may need to run `chmod +x gradlew` and/or `rm -rf /Users/<YOUR_ID>/.gradle/wrapper/dists/gradle-7.3.3-bin/` first)

   ```
   ./gradlew clean 
   ```

2. Build all modules

   ```
   ./gradlew build -x detekt -x lint                      
   ```

## V. Create a Firebase Project

1. Follow the instructions at [https://firebase.google.com/docs/android/setup](https://firebase.google.com/docs/android/setup) to add a Firebase project to the Firebase account you created during backend system installation, and note that our app file name (to place the google-services.json file is `kit`.

   ```
   applicationId = "healthstack.sample"
   ```

NOTE that you should download the resulting `google-services.json` file from firebase into `app-sdk -> samples` (as you'll notice there is no `app` folder as the firebase documentation suggests).

## VI. Per App Configuration

After app creation, for each app you need to:

1. Register your app with your Firebase project by updating the `\<repository\>*/app/google-service.json` configuration file.

<!-- This is where we are at with testing -->

2. For full-stack implementations only, associate your app with the backend system and portal study.

Refer to [Configuring the App Environment](../app-creation/configure-app.md) for details.

## VII. Reference Documentation

Refer to our [API reference](../docs/api-reference/all-endpoints/api-overview.md) and [SDK reference](../docs/sdk-reference/SDK-Documentation.md) documentation for details on all the backend API endpoints and SDK packages.
