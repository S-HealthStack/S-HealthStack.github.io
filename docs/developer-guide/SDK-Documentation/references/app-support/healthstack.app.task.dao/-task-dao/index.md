
[App-Support](../../../index.html) > [healthstack.app.task.dao](../index.html) > [TaskDao](index.html)



# TaskDao



[androidJvm]\
interface [TaskDao](index.html)



## Functions


| Name | Summary |
|---|---|
| [findById](find-by-id.html) | [androidJvm]<br>abstract suspend fun [findById](find-by-id.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Task](../../healthstack.app.task.entity/-task/index.html)? |
| [getActiveTasks](get-active-tasks.html) | [androidJvm]<br>abstract fun [getActiveTasks](get-active-tasks.html)(now: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;&gt; |
| [getCompletedTasks](get-completed-tasks.html) | [androidJvm]<br>abstract fun [getCompletedTasks](get-completed-tasks.html)(from: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), to: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;&gt; |
| [getUpcomingTasks](get-upcoming-tasks.html) | [androidJvm]<br>abstract fun [getUpcomingTasks](get-upcoming-tasks.html)(from: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), to: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): Flow&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;&gt; |
| [insertAll](insert-all.html) | [androidJvm]<br>abstract suspend fun [insertAll](insert-all.html)(taskEntities: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task](../../healthstack.app.task.entity/-task/index.html)&gt;) |
| [removeAll](remove-all.html) | [androidJvm]<br>abstract suspend fun [removeAll](remove-all.html)() |
| [setResult](set-result.html) | [androidJvm]<br>abstract suspend fun [setResult](set-result.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), result: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task.Result](../../healthstack.app.task.entity/-task/-result/index.html)&gt;, startedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), submittedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |
| [setSubmittedAt](set-submitted-at.html) | [androidJvm]<br>abstract suspend fun [setSubmittedAt](set-submitted-at.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), submittedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |

