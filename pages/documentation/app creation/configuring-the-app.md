---
title: Configuring the App Environment
sidebar: doc_sidebar
permalink: configuring-the-app.html
toc: false
---

Several steps are required to connect the app with the outside world:


1. Register your app with Firebase and update the starter-app/app/google-service.json configuration file. Refer to https://firebase.google.com/docs/android/setup for details.

2. Edit <span style="color:red">starter-app/app/src/main/java/com/samsung/healthstack/starter_app/???.xml to associate the API endpoint of the backend system and the app's portal ID.</span>

3. <span style="color:red">Make the app available for downloading.</span>