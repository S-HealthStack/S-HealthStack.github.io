
[App-Support](../../../../index.html) > [healthstack.app.sync](../../index.html) > [SyncManager](../index.html) > [HealthDataSyncSpec](index.html)



# HealthDataSyncSpec



[androidJvm]\
data class [HealthDataSyncSpec](index.html)(val healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val syncInterval: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), val syncTimeUnit: [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html))

A data class representing a specification for health data synchronization.



## Constructors


| | |
|---|---|
| [HealthDataSyncSpec](-health-data-sync-spec.html) | [androidJvm]<br>fun [HealthDataSyncSpec](-health-data-sync-spec.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), syncInterval: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), syncTimeUnit: [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html)) |


## Properties


| Name | Summary |
|---|---|
| [healthDataTypeString](health-data-type-string.html) | [androidJvm]<br>val [healthDataTypeString](health-data-type-string.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>The health data type to synchronize. |
| [syncInterval](sync-interval.html) | [androidJvm]<br>val [syncInterval](sync-interval.html): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)<br>The synchronization interval. |
| [syncTimeUnit](sync-time-unit.html) | [androidJvm]<br>val [syncTimeUnit](sync-time-unit.html): [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html)<br>The [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html) for the synchronization interval. |

