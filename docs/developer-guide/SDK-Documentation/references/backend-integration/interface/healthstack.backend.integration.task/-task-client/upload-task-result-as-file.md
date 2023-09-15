
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskClient](index.html) > [uploadTaskResultAsFile](upload-task-result-as-file.html)



# uploadTaskResultAsFile



[androidJvm]\
abstract suspend fun [uploadTaskResultAsFile](upload-task-result-as-file.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), sourcePath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), targetPath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))



Uploads the user's task execution result as a file to Backend.



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| sourcePath | Absolute path of the result file stored in device. |
| targetPath | Bucket path for the result file to be uploaded. |




