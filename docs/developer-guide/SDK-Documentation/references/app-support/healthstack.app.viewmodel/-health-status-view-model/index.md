
[App-Support](../../../index.html) > [healthstack.app.viewmodel](../index.html) > [HealthStatusViewModel](index.html)



# HealthStatusViewModel



[androidJvm]\
abstract class [HealthStatusViewModel](index.html)(healthStatus: [HealthStatus](../../healthstack.app.status/-health-status/index.html), intervalTimeMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html)



## Constructors


| | |
|---|---|
| [HealthStatusViewModel](-health-status-view-model.html) | [androidJvm]<br>fun [HealthStatusViewModel](-health-status-view-model.html)(healthStatus: [HealthStatus](../../healthstack.app.status/-health-status/index.html), intervalTimeMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [addCloseable](../-task-view-model/index.html#264516373%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun [addCloseable](../-task-view-model/index.html#264516373%2FFunctions%2F-1544593023)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)p0: [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable.html)) |
| [clear](../-task-view-model/index.html#-1936886459%2FFunctions%2F-1544593023) | [androidJvm]<br>@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)<br>fun [clear](../-task-view-model/index.html#-1936886459%2FFunctions%2F-1544593023)() |
| [getTag](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [getTag](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [T](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) |
| [onCleared](../-task-view-model/index.html#-1930136507%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun [onCleared](../-task-view-model/index.html#-1930136507%2FFunctions%2F-1544593023)() |
| [setTagIfAbsent](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [setTagIfAbsent](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), p1: [T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023)): [T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) |


## Properties


| Name | Summary |
|---|---|
| [healthState](health-state.html) | [androidJvm]<br>val [healthState](health-state.html): StateFlow&lt;[HealthState](../-health-state/index.html)&gt; |
| [lifecycle](lifecycle.html) | [androidJvm]<br>var [lifecycle](lifecycle.html): [Lifecycle.Event](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.Event.html) |


## Inheritors


| Name |
|---|
| [HeartRateStatusViewModel](../-heart-rate-status-view-model/index.html) |
| [SleepSessionStatusViewModel](../-sleep-session-status-view-model/index.html) |

