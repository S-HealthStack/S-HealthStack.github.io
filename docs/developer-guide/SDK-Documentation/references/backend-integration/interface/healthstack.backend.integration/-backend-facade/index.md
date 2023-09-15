
[Interface](../../../index.html) > [healthstack.backend.integration](../index.html) > [BackendFacade](index.html)



# BackendFacade



[androidJvm]\
interface [BackendFacade](index.html) : [HealthDataSyncClient](../../healthstack.backend.integration.healthdata/-health-data-sync-client/index.html), [UserRegistrationClient](../../healthstack.backend.integration.registration/-user-registration-client/index.html), [TaskClient](../../healthstack.backend.integration.task/-task-client/index.html)

Facade that collects the interface required for integrating with the backend that stores health data. It provides a simple integrated interface.



## Functions


| Name | Summary |
|---|---|
| [getTasks](../../healthstack.backend.integration.task/-task-client/get-tasks.html) | [androidJvm]<br>abstract suspend fun [getTasks](../../healthstack.backend.integration.task/-task-client/get-tasks.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) = LocalDateTime.now(Clock.systemUTC())): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[TaskSpec](../../healthstack.backend.integration.task/-task-spec/index.html)&gt;<br>Retrieves the task that has been published since the lastSyncTime the task was retrieved. |
| [registerUser](../../healthstack.backend.integration.registration/-user-registration-client/register-user.html) | [androidJvm]<br>abstract suspend fun [registerUser](../../healthstack.backend.integration.registration/-user-registration-client/register-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), user: [User](../../healthstack.backend.integration.registration/-user/index.html))<br>Used to register user's information who joined through the app to the backend. |
| [sync](../../healthstack.backend.integration.healthdata/-health-data-sync-client/sync.html) | [androidJvm]<br>abstract suspend fun [sync](../../healthstack.backend.integration.healthdata/-health-data-sync-client/sync.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthData: HealthData)<br>Used to transmit the user's health data to the backend. Backend can distinguish users through id token. |
| [updateUser](../../healthstack.backend.integration.registration/-user-registration-client/update-user.html) | [androidJvm]<br>abstract suspend fun [updateUser](../../healthstack.backend.integration.registration/-user-registration-client/update-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userProfile: [UserProfile](../../healthstack.backend.integration.registration/-user-profile/index.html))<br>Used to update user's profile who joined through the app to the backend. |
| [uploadTaskResult](../../healthstack.backend.integration.task/-task-client/upload-task-result.html) | [androidJvm]<br>abstract suspend fun [uploadTaskResult](../../healthstack.backend.integration.task/-task-client/upload-task-result.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), result: [TaskResult](../../healthstack.backend.integration.task/-task-result/index.html))<br>Uploads the user's task execution result to Backend. |
| [uploadTaskResultAsFile](../../healthstack.backend.integration.task/-task-client/upload-task-result-as-file.html) | [androidJvm]<br>abstract suspend fun [uploadTaskResultAsFile](../../healthstack.backend.integration.task/-task-client/upload-task-result-as-file.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), sourcePath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), targetPath: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))<br>Uploads the user's task execution result as a file to Backend. |

