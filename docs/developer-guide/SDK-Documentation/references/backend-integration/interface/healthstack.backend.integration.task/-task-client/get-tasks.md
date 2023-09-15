
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskClient](index.html) > [getTasks](get-tasks.html)



# getTasks



[androidJvm]\
abstract suspend fun [getTasks](get-tasks.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) = LocalDateTime.now(Clock.systemUTC())): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[TaskSpec](../-task-spec/index.html)&gt;



Retrieves the task that has been published since the lastSyncTime the task was retrieved.



#### Return



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| lastSyncTime | Get tasks that published after lastSyncTime |
| endTime | Retrieves all tasks created before endTime |




