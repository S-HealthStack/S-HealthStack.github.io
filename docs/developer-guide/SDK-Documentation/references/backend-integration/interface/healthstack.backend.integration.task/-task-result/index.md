
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskResult](index.html)



# TaskResult



[androidJvm]\
data class [TaskResult](index.html)(val userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), val startedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val submittedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val itemResults: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ItemResult](../-item-result/index.html)&gt;)

Data Transfer Object for uploading the result of the task.



## Constructors


| | |
|---|---|
| [TaskResult](-task-result.html) | [androidJvm]<br>fun [TaskResult](-task-result.html)(userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), startedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), submittedAt: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), itemResults: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ItemResult](../-item-result/index.html)&gt;) |


## Properties


| Name | Summary |
|---|---|
| [itemResults](item-results.html) | [androidJvm]<br>val [itemResults](item-results.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ItemResult](../-item-result/index.html)&gt;<br>Results of items belonging to task. |
| [revisionId](revision-id.html) | [androidJvm]<br>val [revisionId](revision-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>If the task is modified, the modified ID for history management. |
| [startedAt](started-at.html) | [androidJvm]<br>val [startedAt](started-at.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Time when the user started the task. |
| [submittedAt](submitted-at.html) | [androidJvm]<br>val [submittedAt](submitted-at.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Time when the user submitted the task. |
| [taskId](task-id.html) | [androidJvm]<br>val [taskId](task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>ID of the completed task. |
| [userId](user-id.html) | [androidJvm]<br>val [userId](user-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>ID of the user who upload the task result. |

