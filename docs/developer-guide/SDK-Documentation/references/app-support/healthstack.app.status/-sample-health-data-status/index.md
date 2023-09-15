
[App-Support](../../../index.html) > [healthstack.app.status](../index.html) > [SampleHealthDataStatus](index.html)



# SampleHealthDataStatus



[androidJvm]\
abstract class [SampleHealthDataStatus](index.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) : [HealthStatus](../-health-status/index.html)

Returns the data key used to extract the heart rate status information.



#### Return



The data key.



## Constructors


| | |
|---|---|
| [SampleHealthDataStatus](-sample-health-data-status.html) | [androidJvm]<br>fun [SampleHealthDataStatus](-sample-health-data-status.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [getDataKey](get-data-key.html) | [androidJvm]<br>abstract fun [getDataKey](get-data-key.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the data key used to extract the status information. |
| [getIcon](../-status-data-type/get-icon.html) | [androidJvm]<br>abstract fun [getIcon](../-status-data-type/get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns the icon resource ID for this health data type. |
| [getLatestStatus](get-latest-status.html) | [androidJvm]<br>open suspend override fun [getLatestStatus](get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?<br>Retrieves the latest status information for this health data type. |
| [getUnitString](../-status-data-type/get-unit-string.html) | [androidJvm]<br>abstract fun [getUnitString](../-status-data-type/get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the unit string for this health data type. |
| [toViewModel](../-health-status/to-view-model.html) | [androidJvm]<br>abstract fun [toViewModel](../-health-status/to-view-model.html)(): [HealthStatusViewModel](../../healthstack.app.viewmodel/-health-status-view-model/index.html) |


## Inheritors


| Name |
|---|
| [HeartRateStatus](../-heart-rate-status/index.html) |

