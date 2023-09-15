
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskClient](index.html)



# TaskClient



[androidJvm]\
interface [TaskClient](index.html)

Interface for get task from the backend and upload result to the backend.



## Functions


| Name | Summary |
|---|---|
| [getTasks](get-tasks.html) | [androidJvm]<br>abstract suspend fun [getTasks](get-tasks.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) = LocalDateTime.now(Clock.systemUTC())): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[TaskSpec](../-task-spec/index.html)&gt;<br>Retrieves the task that has been published since the lastSyncTime the task was retrieved. |
| [uploadTaskResult](upload-task-result.html) | [androidJvm]<br>abstract suspend fun [uploadTaskResult](upload-task-result.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), result: [TaskResult](../-task-result/index.html))<br>Uploads the user's task execution result to Backend. |
| [uploadTaskResultAsFile](upload-task-result-as-file.html) | [androidJvm]<br>abstract suspend fun [uploadTaskResultAsFile](upload-task-result-as-file.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), sourcePath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), targetPath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))<br>Uploads the user's task execution result as a file to Backend. |


## Inheritors


| Name |
|---|
| [BackendFacade](../../healthstack.backend.integration/-backend-facade/index.html) |

