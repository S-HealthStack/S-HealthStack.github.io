
[App-Support](../../../index.html) > [healthstack.app.task.entity](../index.html) > [Task](index.html)



# Task



[androidJvm]\
data class [Task](index.html)(val id: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), val taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val properties: [Task.Properties](-properties/index.html), val result: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task.Result](-result/index.html)&gt;? = null, val createdAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) = LocalDateTime.now(), val scheduledAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), val validUntil: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), val submittedAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null, val startedAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null)



## Constructors


| | |
|---|---|
| [Task](-task.html) | [androidJvm]<br>fun [Task](-task.html)(id: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), properties: [Task.Properties](-properties/index.html), result: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task.Result](-result/index.html)&gt;? = null, createdAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) = LocalDateTime.now(), scheduledAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), validUntil: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html), submittedAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null, startedAt: [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null) |


## Types


| Name | Summary |
|---|---|
| [Properties](-properties/index.html) | [androidJvm]<br>data class [Properties](-properties/index.html)(val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, val items: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Item&gt;) |
| [Result](-result/index.html) | [androidJvm]<br>data class [Result](-result/index.html)(val questionId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val response: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [toViewTask](to-view-task.html) | [androidJvm]<br>fun [toViewTask](to-view-task.html)(): Task |


## Properties


| Name | Summary |
|---|---|
| [createdAt](created-at.html) | [androidJvm]<br>val [createdAt](created-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) |
| [id](id.html) | [androidJvm]<br>val [id](id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null |
| [properties](properties.html) | [androidJvm]<br>val [properties](properties.html): [Task.Properties](-properties/index.html) |
| [result](result.html) | [androidJvm]<br>val [result](result.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Task.Result](-result/index.html)&gt;? = null |
| [revisionId](revision-id.html) | [androidJvm]<br>val [revisionId](revision-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [scheduledAt](scheduled-at.html) | [androidJvm]<br>val [scheduledAt](scheduled-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) |
| [startedAt](started-at.html) | [androidJvm]<br>val [startedAt](started-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null |
| [submittedAt](submitted-at.html) | [androidJvm]<br>val [submittedAt](submitted-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null |
| [taskId](task-id.html) | [androidJvm]<br>val [taskId](task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [type](type.html) | [androidJvm]<br>val [type](type.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [validUntil](valid-until.html) | [androidJvm]<br>val [validUntil](valid-until.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html) |

