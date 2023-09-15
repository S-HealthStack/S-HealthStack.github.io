
[App-Support](../../../index.html) > [healthstack.app.task.repository](../index.html) > [TaskRepositoryImpl](index.html)



# TaskRepositoryImpl



[androidJvm]\
class [TaskRepositoryImpl](index.html) : [TaskRepository](../-task-repository/index.html)



## Constructors


| | |
|---|---|
| [TaskRepositoryImpl](-task-repository-impl.html) | [androidJvm]<br>fun [TaskRepositoryImpl](-task-repository-impl.html)() |


## Functions


| Name | Summary |
|---|---|
| [getActiveTasks](get-active-tasks.html) | [androidJvm]<br>open override fun [getActiveTasks](get-active-tasks.html)(targetTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [getCompletedTasks](get-completed-tasks.html) | [androidJvm]<br>open override fun [getCompletedTasks](get-completed-tasks.html)(now: [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [getCompletedTasksToSync](get-completed-tasks-to-sync.html) | [androidJvm]<br>open override fun [getCompletedTasksToSync](get-completed-tasks-to-sync.html)(from: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), to: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;&gt; |
| [getUpcomingTasks](get-upcoming-tasks.html) | [androidJvm]<br>open override fun [getUpcomingTasks](get-upcoming-tasks.html)(targetTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Task&gt;&gt; |
| [insertAll](insert-all.html) | [androidJvm]<br>open suspend override fun [insertAll](insert-all.html)(taskEntities: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;) |
| [updateResult](update-result.html) | [androidJvm]<br>open suspend override fun [updateResult](update-result.html)(task: Task) |

