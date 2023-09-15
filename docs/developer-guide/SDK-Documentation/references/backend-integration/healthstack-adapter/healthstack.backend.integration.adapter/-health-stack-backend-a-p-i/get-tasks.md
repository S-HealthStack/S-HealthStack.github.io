
[Healthstack-Adapter](../../../healthstack-adapter.html) > [healthstack.backend.integration.adapter](../index.html) > [HealthStackBackendAPI](index.html) > [getTasks](get-tasks.html)



# getTasks



[androidJvm]\




@GET(value = &quot;/api/projects/{projectId}/tasks&quot;)



abstract suspend fun [getTasks](get-tasks.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Query(value = &quot;last_sync_time&quot;)lastSyncTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;end_time&quot;)endTime: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), @Query(value = &quot;status&quot;)status: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;PUBLISHED&quot;): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskSpec&gt;




