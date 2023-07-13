---
title: sync
permalink: /backend-integration/interface/healthstack.backend.integration.healthdata/-health-data-sync-client/sync.html

sidebar: dev_doc_sidebar
---
//[interface](../../../index.html)/[healthstack.backend.integration.healthdata](../index.html)/[HealthDataSyncClient](index.html)/[sync](sync.html)



# sync



[androidJvm]\
abstract suspend fun [sync](sync.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthData: HealthData)



Used to transmit the user's health data to the backend. Backend can distinguish users through id token.



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| healthData | Health data of users collected through the healthstack.healthdata.link.HealthDataLink. |




