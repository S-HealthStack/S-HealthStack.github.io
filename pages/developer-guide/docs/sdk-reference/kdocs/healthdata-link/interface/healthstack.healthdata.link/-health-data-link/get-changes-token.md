---
title: getChangesToken
permalink: /healthdata-link/interface/healthstack.healthdata.link/-health-data-link/get-changes-token.html

sidebar: dev_doc_sidebar
---
//[interface](../../../interface.html)/[healthstack.healthdata.link](../index.html)/[HealthDataLink](index.html)/[getChangesToken](get-changes-token.html)



# getChangesToken



[androidJvm]\
abstract suspend fun [getChangesToken](get-changes-token.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)



A method requesting initial changes token.



It requests changes token for a specific (time) moment.



#### Return



Changes token.



## Parameters


androidJvm

| | |
|---|---|
| healthDataTypeName | Type of health data to read. |




