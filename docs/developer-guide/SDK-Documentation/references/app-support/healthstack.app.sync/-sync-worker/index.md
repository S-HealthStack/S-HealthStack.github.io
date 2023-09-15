
[App-Support](../../../index.html) > [healthstack.app.sync](../index.html) > [SyncWorker](index.html)



# SyncWorker



[androidJvm]\
class [SyncWorker](index.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) : [CoroutineWorker](https://developer.android.com/reference/kotlin/androidx/work/CoroutineWorker.html)

A [CoroutineWorker](https://developer.android.com/reference/kotlin/androidx/work/CoroutineWorker.html) that performs synchronization of health data with the backend.



## Constructors


| | |
|---|---|
| [SyncWorker](-sync-worker.html) | [androidJvm]<br>fun [SyncWorker](-sync-worker.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) |


## Functions


| Name | Summary |
|---|---|
| [doWork](do-work.html) | [androidJvm]<br>open suspend override fun [doWork](do-work.html)(): [ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html)<br>The main entry point of the worker that performs the synchronization. |
| [getApplicationContext](index.html#-560782721%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getApplicationContext](index.html#-560782721%2FFunctions%2F-1544593023)(): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) |
| [getBackgroundExecutor](index.html#1421258461%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>open fun [getBackgroundExecutor](index.html#1421258461%2FFunctions%2F-1544593023)(): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html) |
| [getForegroundInfo](index.html#1577343784%2FFunctions%2F-1544593023) | [androidJvm]<br>open suspend fun [getForegroundInfo](index.html#1577343784%2FFunctions%2F-1544593023)(): [ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html) |
| [getForegroundInfoAsync](index.html#67363926%2FFunctions%2F-1544593023) | [androidJvm]<br>override fun [getForegroundInfoAsync](index.html#67363926%2FFunctions%2F-1544593023)(): ListenableFuture&lt;[ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)&gt; |
| [getId](index.html#-1759193821%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getId](index.html#-1759193821%2FFunctions%2F-1544593023)(): [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html) |
| [getInputData](index.html#-907781528%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getInputData](index.html#-907781528%2FFunctions%2F-1544593023)(): [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html) |
| [getNetwork](index.html#-1225012274%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RequiresApi](https://developer.android.com/reference/kotlin/androidx/annotation/RequiresApi.html)(value = 28)<br>@[Nullable](https://developer.android.com/reference/kotlin/androidx/annotation/Nullable.html)<br>fun [getNetwork](index.html#-1225012274%2FFunctions%2F-1544593023)(): [Network](https://developer.android.com/reference/kotlin/android/net/Network.html)? |
| [getRunAttemptCount](index.html#1096617839%2FFunctions%2F-1544593023) | [androidJvm]<br>@[IntRange](https://developer.android.com/reference/kotlin/androidx/annotation/IntRange.html)(from = 0)<br>fun [getRunAttemptCount](index.html#1096617839%2FFunctions%2F-1544593023)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getTags](index.html#1356325797%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getTags](index.html#1356325797%2FFunctions%2F-1544593023)(): [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |
| [getTaskExecutor](index.html#1625383462%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>open fun [getTaskExecutor](index.html#1625383462%2FFunctions%2F-1544593023)(): TaskExecutor |
| [getTriggeredContentAuthorities](index.html#514689021%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RequiresApi](https://developer.android.com/reference/kotlin/androidx/annotation/RequiresApi.html)(value = 24)<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getTriggeredContentAuthorities](index.html#514689021%2FFunctions%2F-1544593023)(): [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |
| [getTriggeredContentUris](index.html#-1016068107%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RequiresApi](https://developer.android.com/reference/kotlin/androidx/annotation/RequiresApi.html)(value = 24)<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [getTriggeredContentUris](index.html#-1016068107%2FFunctions%2F-1544593023)(): [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html)&gt; |
| [getWorkerFactory](index.html#-473896752%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>open fun [getWorkerFactory](index.html#-473896752%2FFunctions%2F-1544593023)(): [WorkerFactory](https://developer.android.com/reference/kotlin/androidx/work/WorkerFactory.html) |
| [isRunInForeground](index.html#-1414702901%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>open fun [isRunInForeground](index.html#-1414702901%2FFunctions%2F-1544593023)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isStopped](index.html#-43937871%2FFunctions%2F-1544593023) | [androidJvm]<br>fun [isStopped](index.html#-43937871%2FFunctions%2F-1544593023)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isUsed](index.html#2101847327%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>fun [isUsed](index.html#2101847327%2FFunctions%2F-1544593023)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [onStopped](index.html#-1990082143%2FFunctions%2F-1544593023) | [androidJvm]<br>override fun [onStopped](index.html#-1990082143%2FFunctions%2F-1544593023)() |
| [setForeground](index.html#317365985%2FFunctions%2F-1544593023) | [androidJvm]<br>suspend fun [setForeground](index.html#317365985%2FFunctions%2F-1544593023)(foregroundInfo: [ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)) |
| [setForegroundAsync](index.html#-1269350234%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>fun [setForegroundAsync](index.html#-1269350234%2FFunctions%2F-1544593023)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)foregroundInfo: [ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)): ListenableFuture&lt;[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)&gt; |
| [setProgress](index.html#1755411902%2FFunctions%2F-1544593023) | [androidJvm]<br>suspend fun [setProgress](index.html#1755411902%2FFunctions%2F-1544593023)(data: [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html)) |
| [setProgressAsync](index.html#-348364649%2FFunctions%2F-1544593023) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)<br>open fun [setProgressAsync](index.html#-348364649%2FFunctions%2F-1544593023)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)data: [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html)): ListenableFuture&lt;[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)&gt; |
| [setRunInForeground](index.html#-318507078%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>open fun [setRunInForeground](index.html#-318507078%2FFunctions%2F-1544593023)(runInForeground: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setUsed](index.html#1019169525%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>fun [setUsed](index.html#1019169525%2FFunctions%2F-1544593023)() |
| [startWork](index.html#-1181660772%2FFunctions%2F-1544593023) | [androidJvm]<br>override fun [startWork](index.html#-1181660772%2FFunctions%2F-1544593023)(): ListenableFuture&lt;[ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html)&gt; |
| [stop](index.html#-441314364%2FFunctions%2F-1544593023) | [androidJvm]<br>@[RestrictTo](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.html)(value = [[RestrictTo.Scope.LIBRARY_GROUP](https://developer.android.com/reference/kotlin/androidx/annotation/RestrictTo.Scope.LIBRARY_GROUP.html)])<br>fun [stop](index.html#-441314364%2FFunctions%2F-1544593023)() |


## Properties


| Name | Summary |
|---|---|
| [coroutineContext](index.html#1269180052%2FProperties%2F-1544593023) | [androidJvm]<br>~~open~~ ~~val~~ [~~coroutineContext~~](index.html#1269180052%2FProperties%2F-1544593023)~~:~~ CoroutineDispatcher |

