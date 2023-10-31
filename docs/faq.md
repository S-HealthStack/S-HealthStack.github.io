# Frequently Asked Questions (FAQ)

## Mobile App UI
### How can I modify the UI on the starter-app?
You can customize the UI by modifying the `kit module` in `app-sdk`. Specifically, you can edit the files in `kit/src/main/java/healthstack/kit/ui/`. For theme or color changes, update the `AppColors.kt` file.

### Are the screens and flows for the mobile app available in Android Studio?
Yes, the screens and flows for the mobile app are available in Android Studio, and they are not configured in the container and backend.

## Data Synchronization
### How does data synchronization work in the app?
The app uses Android WorkManager for periodic data sync. Once the user permits the use of their health data and finishes logging in, WorkManager is initialized and periodically syncs health data from HealthConnect to the backend, even when the app is not open.

### What is the minimum interval for data sync, and can it be manually triggered?
The least interval that can be set for data sync is 15 minutes. WorkManager cannot be manually triggered; it operates based on the configuration.

### Is it expected for data to only be pushed when the app is engaged?
No, once WorkManager is initialized, it syncs data periodically even when the app is not engaged. Various sequences of opening and closing the ResearchSample app and Samsung Health may trigger data transfer, but WorkManager operates independently based on the configuration.

## Web Portal UI
### How do I modify the UI of the web portal?
You might need to change UI materials before building the container. The SRA team (Quazi & Mike) can provide a more precise answer.

## Health Data Capturing
### How can I capture more types of health data from Samsung Health?
There are two steps: specify the app’s permissions for Health Connect in the `health_permissions.xml` file, and add `HealthDataSyncSpecs` to `MainActivity.kt`. The HealthConnectAdapter currently supports 11 types of health data.

## Technical Issues and Troubleshooting
### What should I do if the account verification email is not sent when creating a web portal account?
Ensure that SMTP access is activated on the account and that outbound calls on the corresponding SMTP port are allowed from your server. If using 2-Factor Authentication (2FA), try signing in with an App Password. If not, you might need to allow less secure apps to access your account.

### What could cause authentication issues when sending emails from the account service?
If you are using 2-Factor Authentication (2FA), try signing in with an App Password. If not, you might need to allow less secure apps to access your account.

## Miscellaneous
### Where can I find logs or monitor the WorkManager for debugging?
You can briefly monitor the WorkManager in the "App Inspection" tab in Android Studio.

### How can I monitor and troubleshoot WorkManager for data synchronization?
You can briefly monitor WorkManager in the "App Inspection" tab in Android Studio. This can help you check if data sync is happening as expected and identify any issues.

### How can I change the configuration for data synchronization?
The data synchronization process is handled by WorkManager, and the interval for data sync is set in the configuration. You can modify this configuration according to your needs, but the minimum interval that can be set is 15 minutes.

## Firebase Integration
### Missing `google-services.json` file in the source code
The app uses Firebase to provide a 3rd party login to users. The `google-services.json` file must be included in the source code. A reference to integrate it can be found [here](https://s-healthstack.io/install-sdk.html).

## Backend Installation
### Need guidance on backend installation for the app
The app fetches project information such as surveys and activity tasks from the backend. For testing, it's recommended to follow the backend installation guide instead of integrating your own backend system. Detailed instructions can be found [here](https://s-healthstack.io/install-backend.html).

## Build Issues
### Error encountered while trying to build the modules related to `healthstack.sample`
The error seems to arise from a missing client for the package name 'healthstack.sample'. Ensure that the correct configurations are available and that the associated files for this client are not missing.

## UI and Graphics
### Possibility of using the graphics and UI from the Samsung Health app in the new build
(No specific answer provided in the email chain, would need further follow-up.)

## Health Data
### How to capture and export accelerometry continuously, not just during the Activity Task?
The app regularly sends over health data logged by Health Connect at intervals that can be set by the user. For sensor data related to each activity task, it's collected & synced when the activity is conducted. Specific activity tasks and their associated sensor types were provided.

### Which data types from Health Connect can be utilized?
The app can utilize all data types supported by Health Connect. By modifying the list of `healthDataRequired`, you can adjust the app to collect additional data types recorded by Health Connect. However, to have data input, that data needs to exist in Health Connect.

## Gradle Issues
### Resolution to `./gradlew clean` failing for app-sdk?
This appears to be an issue with the system failing to communicate with the Gradle plugin repository. Ensure that your system is online, and if you're using a proxy environment, check proxy settings. If a proxy is in use, the issue might be an SSL handshake failure. Check SSL settings and proxy configurations.
