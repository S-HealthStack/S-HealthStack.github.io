
[Healthplatform](../../../healthplatform.html) > [healthstack.healthdata.link.healthplatform](../index.html) > [HealthPlatformAdapter](index.html)



# HealthPlatformAdapter



[androidJvm]\
class [HealthPlatformAdapter](index.html)(healthDataClient: HealthDataClient, healthDataTypeNames: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;) : HealthDataLink



## Constructors


| | |
|---|---|
| [HealthPlatformAdapter](-health-platform-adapter.html) | [androidJvm]<br>fun [HealthPlatformAdapter](-health-platform-adapter.html)(healthDataClient: HealthDataClient, healthDataTypeNames: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;) |


## Types


| Name | Summary |
|---|---|
| [Companion](-companion/index.html) | [androidJvm]<br>object [Companion](-companion/index.html) |


## Functions


| Name | Summary |
|---|---|
| [getChanges](get-changes.html) | [androidJvm]<br>open suspend override fun [getChanges](get-changes.html)(token: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Change |
| [getChangesToken](get-changes-token.html) | [androidJvm]<br>open suspend override fun [getChangesToken](get-changes-token.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [getHealthData](get-health-data.html) | [androidJvm]<br>open suspend override fun [getHealthData](get-health-data.html)(startTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), endTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): HealthData |
| [hasAllPermissions](has-all-permissions.html) | [androidJvm]<br>open suspend override fun [hasAllPermissions](has-all-permissions.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hasPermissions](has-permissions.html) | [androidJvm]<br>suspend fun [hasPermissions](has-permissions.html)(permissions: [Set](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-set/index.html)&lt;Permission&gt;): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isIntervalData](is-interval-data.html) | [androidJvm]<br>open override fun [isIntervalData](is-interval-data.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [requestPermissions](request-permissions.html) | [androidJvm]<br>open suspend override fun [requestPermissions](request-permissions.html)() |

