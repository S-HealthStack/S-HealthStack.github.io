---



title: HealthStackBackendAPI
permalink: /healthstack-adapter/healthstack.backend.integration.adapter/-health-stack-backend-a-p-i/index.html



sidebar: dev_doc_sidebar


---



//[healthstack-adapter](/healthstack-adapter.html)/[healthstack.backend.integration.adapter](../index.html)/[HealthStackBackendAPI](index.html)



# HealthStackBackendAPI



[androidJvm]\
interface [HealthStackBackendAPI](index.html)



## Functions


| Name | Summary |
|---|---|
| [getTasks](get-tasks.html) | [androidJvm]<br>@GET(value = &quot;api/projects/{projectId}/tasks&quot;)<br>abstract suspend fun [getTasks](get-tasks.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Query(value = &quot;last_sync_time&quot;)lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;end_time&quot;)endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;status&quot;)status: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;PUBLISHED&quot;): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskSpec&gt; |
| [registerUser](register-user.html) | [androidJvm]<br>@POST(value = &quot;/api/projects/{projectId}/users&quot;)<br>abstract suspend fun [registerUser](register-user.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Bodyuser: User) |
| [sync](sync.html) | [androidJvm]<br>@POST(value = &quot;/api/projects/{projectId}/health-data&quot;)<br>abstract suspend fun [sync](sync.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodyhealthData: HealthData) |
| [uploadTaskResult](upload-task-result.html) | [androidJvm]<br>@PATCH(value = &quot;api/projects/{projectId}/tasks&quot;)<br>abstract suspend fun [uploadTaskResult](upload-task-result.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodytaskResult: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskResult&gt;) |



