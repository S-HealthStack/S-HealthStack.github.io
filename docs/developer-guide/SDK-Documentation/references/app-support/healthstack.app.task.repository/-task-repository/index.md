
[App-Support](../../../index.html) > [healthstack.app.task.repository](../index.html) > [TaskRepository](index.html)



# TaskRepository



[androidJvm]\
interface [TaskRepository](index.html)



## Functions


| Name | Summary |
|---|---|
| [getActiveTasks](get-active-tasks.html) | [androidJvm]<br>abstract fun [getActiveTasks](get-active-tasks.html)(targetTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [getCompletedTasks](get-completed-tasks.html) | [androidJvm]<br>abstract fun [getCompletedTasks](get-completed-tasks.html)(targetDay: [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [getCompletedTasksToSync](get-completed-tasks-to-sync.html) | [androidJvm]<br>abstract fun [getCompletedTasksToSync](get-completed-tasks-to-sync.html)(from: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), to: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;&gt; |
| [getUpcomingTasks](get-upcoming-tasks.html) | [androidJvm]<br>abstract fun [getUpcomingTasks](get-upcoming-tasks.html)(targetTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [insertAll](insert-all.html) | [androidJvm]<br>abstract suspend fun [insertAll](insert-all.html)(tasks: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;) |
| [updateResult](update-result.html) | [androidJvm]<br>abstract suspend fun [updateResult](update-result.html)(task: Task) |


## Inheritors


| Name |
|---|
| [TaskRepositoryImpl](../-task-repository-impl/index.html) |

