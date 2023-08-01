---
title: getChanges
permalink: /healthdata-link/interface/healthstack.healthdata.link/-health-data-link/get-changes.html

sidebar: dev_doc_sidebar
---
//[interface](../../../interface.html)/[healthstack.healthdata.link](../index.html)/[HealthDataLink](index.html)/[getChanges](get-changes.html)



# getChanges



[androidJvm]\
abstract suspend fun [getChanges](get-changes.html)(token: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Change](../-change/index.html)



A method reading all events about changes generated after given changes token.



Change events are usually categorized of Upsertion and Deletion.



#### Return



[Change](../-change/index.html)



## Parameters


androidJvm

| | |
|---|---|
| token | Changes token. |
| healthDataTypeName | Type of health data to read. |




