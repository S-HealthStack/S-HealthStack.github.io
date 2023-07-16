---
title: Configuring the App Environment
sidebar: doc_sidebar
permalink: configure-app.html
toc: false
---

In addition to the one-time [app SDK installation steps](../installation/install-sdk.md), these configuration steps are required for each app you develop:

1. Register your app with [the Firebase project you created](../installation/install-sdk.md#vii-create-a-firebase-project) during app SDK installation and update the ***\<repository\>*/app/google-service.json** configuration file.
> For example:
> ```
> {
>   "project_info": {
>     "project_number": "100000000000",
>     "project_id": "sample-project",
>     "storage_bucket": "sample-project.appspot.com"
>   },
>   
>  "client": [
>     {
>       "client_info": {
>         "mobilesdk_app_id": "1:100000000000:android:abcdefgh",
>         "android_client_info": {
>           "package_name": "com.samsung.healthcare.kit.sample"
>         }
>       },
> }
> ```
> Refer to [https://firebase.google.com/docs/android/setup](https://firebase.google.com/docs/android/setup){:target="_blank"} for details.
2. For full-stack implementations only, associate your app with the backend system and portal study.
   > In **starter-app/app/src/main/res/values/strings.xml**, update the lines at the bottom of the file that specify your backend system's endpoint and your study's project ID, for example:
   >
   > ```
   > <string name="research_platform_endpoint">https://shs.dev.ai-service.io</string>
   > <string name="research_project_id">1</string>
   > ```
   >
   > Note: The project ID of your study is contained in the JSON response of a `POST /api/projects` request.

3. Make the app available for downloading.
