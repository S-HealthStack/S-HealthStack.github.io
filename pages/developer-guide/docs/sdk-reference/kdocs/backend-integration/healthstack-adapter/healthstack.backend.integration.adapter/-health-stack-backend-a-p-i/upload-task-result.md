---
title: uploadTaskResult
permalink: /backend-integration/healthstack-adapter/healthstack.backend.integration.adapter/-health-stack-backend-a-p-i/upload-task-result.html

sidebar: dev_doc_sidebar
---
//[healthstack-adapter](../../../healthstack-adapter.html)/[healthstack.backend.integration.adapter](../index.html)/[HealthStackBackendAPI](index.html)/[uploadTaskResult](upload-task-result.html)



# uploadTaskResult



[androidJvm]\




@PATCH(value = &quot;/api/projects/{projectId}/tasks&quot;)



abstract suspend fun [uploadTaskResult](upload-task-result.html)(@Header(value = &quot;id-token&quot;)idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @Path(value = &quot;projectId&quot;)projectId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), @BodytaskResult: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;TaskResult&gt;)




