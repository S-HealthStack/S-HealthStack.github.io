
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskClient](index.html) > [uploadTaskResult](upload-task-result.html)



# uploadTaskResult



[androidJvm]\
abstract suspend fun [uploadTaskResult](upload-task-result.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), result: [TaskResult](../-task-result/index.html))



Uploads the user's task execution result to Backend.



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| result | [healthstack.backend.integration.task.TaskResult](../-task-result/index.html) |




