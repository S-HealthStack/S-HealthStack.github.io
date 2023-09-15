
[Healthstack-Adapter](../../../healthstack-adapter.html) > [healthstack.backend.integration.adapter](../index.html) > [HealthStackBackendAPI](index.html) > [sync](sync.html)



# sync



[androidJvm]\




@POST(value = &quot;/api/projects/{projectId}/health-data&quot;)



abstract suspend fun [sync](sync.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodyhealthData: HealthData)




