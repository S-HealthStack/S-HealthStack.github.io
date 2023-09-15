
[App-Support](../../../index.html) > [healthstack.app.status](../index.html) > [HeartRateStatus](index.html)



# HeartRateStatus



[androidJvm]\
object [HeartRateStatus](index.html) : [SampleHealthDataStatus](../-sample-health-data-status/index.html)

An object representing the status of heart rate. Inherits from SampleHealthDataStatus, which represents a type of health data for which status information can be retrieved using a single data point.



## Functions


| Name | Summary |
|---|---|
| [getDataKey](get-data-key.html) | [androidJvm]<br>open override fun [getDataKey](get-data-key.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the data key used to extract the heart rate status information. |
| [getIcon](get-icon.html) | [androidJvm]<br>open override fun [getIcon](get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns the resource ID of the icon representing the heart rate status. |
| [getLatestStatus](../-sample-health-data-status/get-latest-status.html) | [androidJvm]<br>open suspend override fun [getLatestStatus](../-sample-health-data-status/get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?<br>Retrieves the latest status information for this health data type. |
| [getUnitString](get-unit-string.html) | [androidJvm]<br>open override fun [getUnitString](get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the unit of measurement for the heart rate data. |
| [toViewModel](to-view-model.html) | [androidJvm]<br>open override fun [toViewModel](to-view-model.html)(): [HeartRateStatusViewModel](../../healthstack.app.viewmodel/-heart-rate-status-view-model/index.html) |

