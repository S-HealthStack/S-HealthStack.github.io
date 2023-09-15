## Missing `google-services.json` file in the source code for Firebase integration.

The app uses firebase to provide a 3rd party login to users. The `google-services.json` file must be included in the source code. A reference to integrate it can be found [here](https://s-healthstack.io/install-sdk.html).

---

## Need guidance on backend installation for the app.

The app fetches project information such as surveys and activity tasks from the backend. For testing, it's recommended to follow the backend installation guide instead of integrating your own backend system. Detailed instructions can be found [here](https://s-healthstack.io/install-backend.html).

---

## Error encountered while trying to build the modules related to `healthstack.sample`.

The error seems to arise from a missing client for the package name 'healthstack.sample'. Ensure that the correct configurations are available and that the associated files for this client are not missing.

---

## Possibility of using the graphics and UI from the Samsung Health app in the new build.

(No specific answer provided in the email chain, would need further follow-up.)

---

## How to capture and export accelerometry continuously, not just during the Activity Task?

The app regularly sends over health data logged by Health Connect at intervals that can be set by the user. For sensor data related to each activity task, it's collected & synced when the activity is conducted. Specific activity tasks and their associated sensor types were provided.

---

## Which data types from Health Connect can be utilized?

The app can utilize all data types supported by Health Connect. By modifying the list of `healthDataRequired`, you can adjust the app to collect additional data types recorded by Health Connect. However, to have data input, that data needs to exist in Health Connect.

---

## Resolution to `./gradlew clean` failing for app-sdk?

This appears to be an issue with the system failing to communicate with the Gradle plugin repository. Ensure that your system is online, and if you're using a proxy environment, check proxy settings. If a proxy is in use, the issue might be an SSL handshake failure. Check SSL settings and proxy configurations.

