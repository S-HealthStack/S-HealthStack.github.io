
[App-Support](../../../index.html) > [healthstack.app.viewmodel](../index.html) > [TaskViewModel](index.html)



# TaskViewModel



[androidJvm]\
class [TaskViewModel](index.html)(taskRepository: [TaskRepository](../../healthstack.app.task.repository/-task-repository/index.html), settingPreference: [SettingPreference](../../healthstack.app.pref/-setting-preference/index.html)) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html)



## Constructors


| | |
|---|---|
| [TaskViewModel](-task-view-model.html) | [androidJvm]<br>fun [TaskViewModel](-task-view-model.html)(taskRepository: [TaskRepository](../../healthstack.app.task.repository/-task-repository/index.html), settingPreference: [SettingPreference](../../healthstack.app.pref/-setting-preference/index.html)) |


## Types


| Name | Summary |
|---|---|
| [TasksState](-tasks-state/index.html) | [androidJvm]<br>data class [TasksState](-tasks-state/index.html)(val tasks: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;) |


## Functions


| Name | Summary |
|---|---|
| [addCloseable](index.html#264516373%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun [addCloseable](index.html#264516373%2FFunctions%2F-1544593023)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)p0: [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable.html)) |
| [clear](index.html#-1936886459%2FFunctions%2F-1544593023) | [androidJvm]<br>@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)<br>fun [clear](index.html#-1936886459%2FFunctions%2F-1544593023)() |
| [done](done.html) | [androidJvm]<br>fun [done](done.html)(task: Task) |
| [getTag](index.html#-215894976%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](index.html#-215894976%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [getTag](index.html#-215894976%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [T](index.html#-215894976%2FFunctions%2F-1544593023) |
| [onCleared](index.html#-1930136507%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun [onCleared](index.html#-1930136507%2FFunctions%2F-1544593023)() |
| [setTagIfAbsent](index.html#-1567230750%2FFunctions%2F-1544593023) | [androidJvm]<br>open fun &lt;[T](index.html#-1567230750%2FFunctions%2F-1544593023) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; [setTagIfAbsent](index.html#-1567230750%2FFunctions%2F-1544593023)(p0: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), p1: [T](index.html#-1567230750%2FFunctions%2F-1544593023)): [T](index.html#-1567230750%2FFunctions%2F-1544593023) |
| [syncTasks](sync-tasks.html) | [androidJvm]<br>fun [syncTasks](sync-tasks.html)() |


## Properties


| Name | Summary |
|---|---|
| [activeTasks](active-tasks.html) | [androidJvm]<br>val [activeTasks](active-tasks.html): StateFlow&lt;[TaskViewModel.TasksState](-tasks-state/index.html)&gt; |
| [completedTasks](completed-tasks.html) | [androidJvm]<br>val [completedTasks](completed-tasks.html): StateFlow&lt;[TaskViewModel.TasksState](-tasks-state/index.html)&gt; |
| [todayTasks](today-tasks.html) | [androidJvm]<br>val [todayTasks](today-tasks.html): StateFlow&lt;[TaskViewModel.TasksState](-tasks-state/index.html)&gt; |

