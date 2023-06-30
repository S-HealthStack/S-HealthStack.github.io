---



title: HealthStatusViewModel
permalink: /app-support/healthstack.app.viewmodel/-health-status-view-model/index.html



sidebar: dev_doc_sidebar


---



//[app-support](/app-support.html)/[healthstack.app.viewmodel](../index.html)/[HealthStatusViewModel](index.html)



# HealthStatusViewModel



[androidJvm]\
class [HealthStatusViewModel](index.html)(dataType: [StatusDataType](../../healthstack.app.status/-status-data-type/index.html)) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html)



## Constructors


| | |
|---|---|
| [HealthStatusViewModel](-health-status-view-model.html) | [androidJvm]<br>fun [HealthStatusViewModel](-health-status-view-model.html)(dataType: [StatusDataType](../../healthstack.app.status/-status-data-type/index.html)) |


## Types


| Name | Summary |
|---|---|
| [HealthState](-health-state/index.html) | [androidJvm]<br>data class [HealthState](-health-state/index.html)(val state: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [clear](../-task-view-model/index.html#-1936886459%2FFunctions%2F-1544593023) | [androidJvm]<br>@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)<br>fun [clear](../-task-view-model/index.html#-1936886459%2FFunctions%2F-1544593023)() |
| [getTag](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [getTag](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [T](../-task-view-model/index.html#-215894976%2FFunctions%2F-1544593023) |
| [onCleared](../-task-view-model/index.html#-1930136507%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun [onCleared](../-task-view-model/index.html#-1930136507%2FFunctions%2F-1544593023)() |
| [setTagIfAbsent](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [setTagIfAbsent](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), p1: [T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023)): [T](../-task-view-model/index.html#-1567230750%2FFunctions%2F-1544593023) |


## Properties


| Name | Summary |
|---|---|
| [healthState](health-state.html) | [androidJvm]<br>val [healthState](health-state.html): StateFlow&lt;[HealthStatusViewModel.HealthState](-health-state/index.html)&gt; |



