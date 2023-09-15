
[App-Support](../../../index.html) > [healthstack.app.status](../index.html) > [SleepSessionStatus](index.html)



# SleepSessionStatus



[androidJvm]\
object [SleepSessionStatus](index.html) : [HealthStatus](../-health-status/index.html)

An object representing the status of sleep sessions.



## Functions


| Name | Summary |
|---|---|
| [getIcon](get-icon.html) | [androidJvm]<br>open override fun [getIcon](get-icon.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns the icon resource ID for sleep sessions. |
| [getLatestStatus](get-latest-status.html) | [androidJvm]<br>open suspend override fun [getLatestStatus](get-latest-status.html)(): [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?<br>Returns an Instant representing midnight of the current day. |
| [getUnitString](get-unit-string.html) | [androidJvm]<br>open override fun [getUnitString](get-unit-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns the unit string for sleep sessions. |
| [toViewModel](to-view-model.html) | [androidJvm]<br>open override fun [toViewModel](to-view-model.html)(): [SleepSessionStatusViewModel](../../healthstack.app.viewmodel/-sleep-session-status-view-model/index.html) |

