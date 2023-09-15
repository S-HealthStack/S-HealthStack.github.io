
[App-Support](../../../index.html) > [healthstack.app.status](../index.html) > [HealthStatus](index.html)



# HealthStatus



[androidJvm]\
abstract class [HealthStatus](index.html) : [StatusDataType](../-status-data-type/index.html)



## Constructors


| | |
|---|---|
| [HealthStatus](-health-status.html) | [androidJvm]<br>fun [HealthStatus](-health-status.html)() |


## Functions


| Name | Summary |
|---|---|
| [getIcon](../-status-data-type/get-icon.html) | [androidJvm]<br>abstract fun [getIcon](../-status-data-type/get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns the icon resource ID for this health data type. |
| [getLatestStatus](../-status-data-type/get-latest-status.html) | [androidJvm]<br>abstract suspend fun [getLatestStatus](../-status-data-type/get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?<br>Returns the unit string for this health data type. |
| [getUnitString](../-status-data-type/get-unit-string.html) | [androidJvm]<br>abstract fun [getUnitString](../-status-data-type/get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the unit string for this health data type. |
| [toViewModel](to-view-model.html) | [androidJvm]<br>abstract fun [toViewModel](to-view-model.html)(): [HealthStatusViewModel](../../healthstack.app.viewmodel/-health-status-view-model/index.html) |


## Inheritors


| Name |
|---|
| [SampleHealthDataStatus](../-sample-health-data-status/index.html) |
| [SleepSessionStatus](../-sleep-session-status/index.html) |

