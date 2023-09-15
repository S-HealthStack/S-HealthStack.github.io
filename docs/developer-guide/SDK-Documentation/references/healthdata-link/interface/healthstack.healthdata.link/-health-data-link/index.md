
[Interface](../../../interface.html) > [healthstack.healthdata.link](../index.html) > [HealthDataLink](index.html)



# HealthDataLink



[androidJvm]\
interface [HealthDataLink](index.html)

An interface for handling health data.



It has several methods for general health data client.



## Functions


| Name | Summary |
|---|---|
| [getChanges](get-changes.html) | [androidJvm]<br>abstract suspend fun [getChanges](get-changes.html)(token: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Change](../-change/index.html)<br>A method reading all events about changes generated after given changes token. |
| [getChangesToken](get-changes-token.html) | [androidJvm]<br>abstract suspend fun [getChangesToken](get-changes-token.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>A method requesting initial changes token. |
| [getHealthData](get-health-data.html) | [androidJvm]<br>abstract suspend fun [getHealthData](get-health-data.html)(startTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), endTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HealthData](../-health-data/index.html)<br>A method reading health data. |
| [hasAllPermissions](has-all-permissions.html) | [androidJvm]<br>abstract suspend fun [hasAllPermissions](has-all-permissions.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>A method checking if all permissions are acquired. |
| [isIntervalData](is-interval-data.html) | [androidJvm]<br>abstract fun [isIntervalData](is-interval-data.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>A method checking if the given health data type is Interval data. |
| [requestPermissions](request-permissions.html) | [androidJvm]<br>abstract suspend fun [requestPermissions](request-permissions.html)()<br>A method requesting all permissions. |

