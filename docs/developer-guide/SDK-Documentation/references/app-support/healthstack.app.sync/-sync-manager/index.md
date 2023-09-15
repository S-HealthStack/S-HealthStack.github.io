
[App-Support](../../../index.html) > [healthstack.app.sync](../index.html) > [SyncManager](index.html)



# SyncManager



[androidJvm]\
class [SyncManager](index.html)

SyncManager is a singleton class using Android's WorkManager for scheduled health data synchronization tasks. Each task is specified by a [HealthDataSyncSpec](-health-data-sync-spec/index.html), which includes the health data type and its sync interval.



## Types


| Name | Summary |
|---|---|
| [Companion](-companion/index.html) | [androidJvm]<br>object [Companion](-companion/index.html) |
| [HealthDataSyncSpec](-health-data-sync-spec/index.html) | [androidJvm]<br>data class [HealthDataSyncSpec](-health-data-sync-spec/index.html)(val healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val syncInterval: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), val syncTimeUnit: [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html))<br>A data class representing a specification for health data synchronization. |


## Functions


| Name | Summary |
|---|---|
| [startBackgroundSync](start-background-sync.html) | [androidJvm]<br>fun [startBackgroundSync](start-background-sync.html)()<br>Starts the background synchronization for the specified health data types. |

