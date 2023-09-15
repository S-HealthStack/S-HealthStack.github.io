
[Healthconnect](../../../healthconnect.html) > [healthstack.healthdata.link.healthconnect](../index.html) > [HealthConnectAdapter](index.html)



# HealthConnectAdapter



[androidJvm]\
class [HealthConnectAdapter](index.html)(healthDataTypeNames: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;, healthConnectClient: [HealthConnectClient](https://developer.android.com/reference/kotlin/androidx/health/connect/client/HealthConnectClient.html)) : HealthDataLink



## Constructors


| | |
|---|---|
| [HealthConnectAdapter](-health-connect-adapter.html) | [androidJvm]<br>fun [HealthConnectAdapter](-health-connect-adapter.html)(healthDataTypeNames: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;, healthConnectClient: [HealthConnectClient](https://developer.android.com/reference/kotlin/androidx/health/connect/client/HealthConnectClient.html)) |


## Functions


| Name | Summary |
|---|---|
| [createLauncher](create-launcher.html) | [androidJvm]<br>fun [createLauncher](create-launcher.html)(context: [ComponentActivity](https://developer.android.com/reference/kotlin/androidx/activity/ComponentActivity.html)) |
| [getChanges](get-changes.html) | [androidJvm]<br>open suspend override fun [getChanges](get-changes.html)(token: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Change |
| [getChangesToken](get-changes-token.html) | [androidJvm]<br>open suspend override fun [getChangesToken](get-changes-token.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [getHealthData](get-health-data.html) | [androidJvm]<br>open suspend override fun [getHealthData](get-health-data.html)(startTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), endTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): HealthData |
| [hasAllPermissions](has-all-permissions.html) | [androidJvm]<br>open suspend override fun [hasAllPermissions](has-all-permissions.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isIntervalData](is-interval-data.html) | [androidJvm]<br>open override fun [isIntervalData](is-interval-data.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [requestPermissions](request-permissions.html) | [androidJvm]<br>open suspend override fun [requestPermissions](request-permissions.html)() |

