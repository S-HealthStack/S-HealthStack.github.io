
[App-Support](../../index.html) > [healthstack.app.sync](index.html)



# Package healthstack.app.sync



## Types


| Name | Summary |
|---|---|
| [FileSyncManager](-file-sync-manager/index.html) | [androidJvm]<br>class [FileSyncManager](-file-sync-manager/index.html) |
| [FileSyncWorker](-file-sync-worker/index.html) | [androidJvm]<br>class [FileSyncWorker](-file-sync-worker/index.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) : [CoroutineWorker](https://developer.android.com/reference/kotlin/androidx/work/CoroutineWorker.html) |
| [SyncManager](-sync-manager/index.html) | [androidJvm]<br>class [SyncManager](-sync-manager/index.html)<br>SyncManager is a singleton class using Android's WorkManager for scheduled health data synchronization tasks. Each task is specified by a [HealthDataSyncSpec](-sync-manager/-health-data-sync-spec/index.html), which includes the health data type and its sync interval. |
| [SyncWorker](-sync-worker/index.html) | [androidJvm]<br>class [SyncWorker](-sync-worker/index.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) : [CoroutineWorker](https://developer.android.com/reference/kotlin/androidx/work/CoroutineWorker.html)<br>A [CoroutineWorker](https://developer.android.com/reference/kotlin/androidx/work/CoroutineWorker.html) that performs synchronization of health data with the backend. |

