
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TaskSpec](index.html)



# TaskSpec



[androidJvm]\
data class [TaskSpec](index.html)(val revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), val taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, val schedule: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val startTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val endTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val validTime: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), val items: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Item](../-item/index.html)&gt;)

Stores the information of the task received from backend.



## Constructors


| | |
|---|---|
| [TaskSpec](-task-spec.html) | [androidJvm]<br>fun [TaskSpec](-task-spec.html)(revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, schedule: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), startTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), endTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), validTime: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), items: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Item](../-item/index.html)&gt;) |


## Properties


| Name | Summary |
|---|---|
| [description](description.html) | [androidJvm]<br>val [description](description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?<br>Description of the task. |
| [endTime](end-time.html) | [androidJvm]<br>val [endTime](end-time.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Expiration time when task is no longer exposed. |
| [items](items.html) | [androidJvm]<br>val [items](items.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Item](../-item/index.html)&gt;<br>Items of the task |
| [revisionId](revision-id.html) | [androidJvm]<br>val [revisionId](revision-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>If the task is modified, the modified ID for history management. |
| [schedule](schedule.html) | [androidJvm]<br>val [schedule](schedule.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Schedule of the task. (CronQuartz format) |
| [startTime](start-time.html) | [androidJvm]<br>val [startTime](start-time.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Time to activate task. |
| [taskId](task-id.html) | [androidJvm]<br>@SerializedName(value = &quot;id&quot;)<br>val [taskId](task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>ID of the task. |
| [title](title.html) | [androidJvm]<br>val [title](title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Title of the task. |
| [type](type.html) | [androidJvm]<br>val [type](type.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [validTime](valid-time.html) | [androidJvm]<br>val [validTime](valid-time.html): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)<br>The time given to the user to perform the task. |

