
[App-Support](../../../index.html) > [healthstack.app.status](../index.html) > [StatusDataType](index.html)



# StatusDataType



[androidJvm]\
abstract class [StatusDataType](index.html)

An abstract class representing a type of health data for which status information can be retrieved.



## Constructors


| | |
|---|---|
| [StatusDataType](-status-data-type.html) | [androidJvm]<br>fun [StatusDataType](-status-data-type.html)() |


## Functions


| Name | Summary |
|---|---|
| [getIcon](get-icon.html) | [androidJvm]<br>abstract fun [getIcon](get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns the icon resource ID for this health data type. |
| [getLatestStatus](get-latest-status.html) | [androidJvm]<br>abstract suspend fun [getLatestStatus](get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?<br>Returns the unit string for this health data type. |
| [getUnitString](get-unit-string.html) | [androidJvm]<br>abstract fun [getUnitString](get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the unit string for this health data type. |


## Inheritors


| Name |
|---|
| [HealthStatus](../-health-status/index.html) |
| [TaskStatus](../-task-status/index.html) |

