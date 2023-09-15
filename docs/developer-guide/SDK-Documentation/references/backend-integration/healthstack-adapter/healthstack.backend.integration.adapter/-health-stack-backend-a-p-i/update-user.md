
[Healthstack-Adapter](../../../healthstack-adapter.html) > [healthstack.backend.integration.adapter](../index.html) > [HealthStackBackendAPI](index.html) > [updateUser](update-user.html)



# updateUser



[androidJvm]\




@PATCH(value = &quot;/api/projects/{projectId}/users/{userId}&quot;)



abstract suspend fun [updateUser](update-user.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;userId&quot;)userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodyuserProfile: UserProfile)




