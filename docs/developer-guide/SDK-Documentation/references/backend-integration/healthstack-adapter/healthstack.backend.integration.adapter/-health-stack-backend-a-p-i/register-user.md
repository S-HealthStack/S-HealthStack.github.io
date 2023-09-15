
[Healthstack-Adapter](../../../healthstack-adapter.html) > [healthstack.backend.integration.adapter](../index.html) > [HealthStackBackendAPI](index.html) > [registerUser](register-user.html)



# registerUser



[androidJvm]\




@POST(value = &quot;/api/projects/{projectId}/users&quot;)



abstract suspend fun [registerUser](register-user.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Bodyuser: User)




