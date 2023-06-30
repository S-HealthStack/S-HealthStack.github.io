---



title: SampleHealthDataStatus
permalink: /app-support/healthstack.app.status/-sample-health-data-status/index.html



sidebar: dev_doc_sidebar


---



//[app-support](/app-support.html)/[healthstack.app.status](../index.html)/[SampleHealthDataStatus](index.html)



# SampleHealthDataStatus



[androidJvm]\
abstract class [SampleHealthDataStatus](index.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) : [StatusDataType](../-status-data-type/index.html)



## Constructors


| | |
|---|---|
| [SampleHealthDataStatus](-sample-health-data-status.html) | [androidJvm]<br>fun [SampleHealthDataStatus](-sample-health-data-status.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [getDataKey](get-data-key.html) | [androidJvm]<br>abstract fun [getDataKey](get-data-key.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [getIcon](../-status-data-type/get-icon.html) | [androidJvm]<br>abstract fun [getIcon](../-status-data-type/get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getLatestStatus](get-latest-status.html) | [androidJvm]<br>open suspend override fun [getLatestStatus](get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? |
| [getUnitString](../-status-data-type/get-unit-string.html) | [androidJvm]<br>abstract fun [getUnitString](../-status-data-type/get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |


## Inheritors


| Name |
|---|
| [HeartRateStatus](../-heart-rate-status/index.html) |



