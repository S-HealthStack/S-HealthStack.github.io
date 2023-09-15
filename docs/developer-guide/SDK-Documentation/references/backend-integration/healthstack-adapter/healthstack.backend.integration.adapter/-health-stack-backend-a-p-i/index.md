
[Healthstack-Adapter](../../../healthstack-adapter.html) > [healthstack.backend.integration.adapter](../index.html) > [HealthStackBackendAPI](index.html)



# HealthStackBackendAPI



[androidJvm]\
interface [HealthStackBackendAPI](index.html)



## Functions


| Name | Summary |
|---|---|
| [getTasks](get-tasks.html) | [androidJvm]<br>@GET(value = &quot;/api/projects/{projectId}/tasks&quot;)<br>abstract suspend fun [getTasks](get-tasks.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Query(value = &quot;last_sync_time&quot;)lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;end_time&quot;)endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;status&quot;)status: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;PUBLISHED&quot;): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskSpec&gt; |
| [getUploadUrl](get-upload-url.html) | [androidJvm]<br>@GET(value = &quot;/cloud-storage/projects/{projectId}/participants/upload-url&quot;)<br>abstract suspend fun [getUploadUrl](get-upload-url.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Query(value = &quot;object_name&quot;)objectName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [registerUser](register-user.html) | [androidJvm]<br>@POST(value = &quot;/api/projects/{projectId}/users&quot;)<br>abstract suspend fun [registerUser](register-user.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Bodyuser: User) |
| [sync](sync.html) | [androidJvm]<br>@POST(value = &quot;/api/projects/{projectId}/health-data&quot;)<br>abstract suspend fun [sync](sync.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodyhealthData: HealthData) |
| [updateUser](update-user.html) | [androidJvm]<br>@PATCH(value = &quot;/api/projects/{projectId}/users/{userId}&quot;)<br>abstract suspend fun [updateUser](update-user.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;userId&quot;)userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodyuserProfile: UserProfile) |
| [uploadTaskResult](upload-task-result.html) | [androidJvm]<br>@PATCH(value = &quot;/api/projects/{projectId}/tasks&quot;)<br>abstract suspend fun [uploadTaskResult](upload-task-result.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodytaskResult: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskResult&gt;) |

