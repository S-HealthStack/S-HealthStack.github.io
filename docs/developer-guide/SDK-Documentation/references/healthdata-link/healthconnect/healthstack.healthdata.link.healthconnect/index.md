
[Healthconnect](../../healthconnect.html) > [healthstack.healthdata.link.healthconnect](index.html)



# Package healthstack.healthdata.link.healthconnect



## Types


| Name | Summary |
|---|---|
| [HealthConnectAdapter](-health-connect-adapter/index.html) | [androidJvm]<br>class [HealthConnectAdapter](-health-connect-adapter/index.html)(healthDataTypeNames: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;, healthConnectClient: [HealthConnectClient](https://developer.android.com/reference/kotlin/androidx/health/connect/client/HealthConnectClient.html)) : HealthDataLink |
| [HealthConnectUtils](-health-connect-utils/index.html) | [androidJvm]<br>object [HealthConnectUtils](-health-connect-utils/index.html) |


## Functions


| Name | Summary |
|---|---|
| [toChange](to-change.html) | [androidJvm]<br>fun [ChangesResponse](https://developer.android.com/reference/kotlin/androidx/health/connect/client/response/ChangesResponse.html).[toChange](to-change.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Change |
| [toHealthData](to-health-data.html) | [androidJvm]<br>fun [ReadRecordsResponse](https://developer.android.com/reference/kotlin/androidx/health/connect/client/response/ReadRecordsResponse.html)&lt;out [Record](https://developer.android.com/reference/kotlin/androidx/health/connect/client/records/Record.html)&gt;.[toHealthData](to-health-data.html)(healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): HealthData<br>fun [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Record](https://developer.android.com/reference/kotlin/androidx/health/connect/client/records/Record.html)&gt;.[toHealthData](to-health-data.html)(healthDataSet: [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;&gt;) |

