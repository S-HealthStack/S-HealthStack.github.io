
[Kit](../../../kit.html) > [healthstack.kit.task.survey](../index.html) > [SurveyTask](index.html)



# SurveyTask



[androidJvm]\
open class [SurveyTask](index.html) : [Task](../../healthstack.kit.task.base/-task/index.html)



## Types


| Name | Summary |
|---|---|
| [Builder](-builder/index.html) | [androidJvm]<br>class [Builder](-builder/index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), callback: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), pageable: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true) |


## Functions


| Name | Summary |
|---|---|
| [CardView](-card-view.html) | [androidJvm]<br>@Composable<br>open override fun [CardView](-card-view.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A method for rendering CardView UI. |
| [equals](../../healthstack.kit.task.base/-task/equals.html) | [androidJvm]<br>open operator override fun [equals](../../healthstack.kit.task.base/-task/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](../../healthstack.kit.task.base/-task/hash-code.html) | [androidJvm]<br>open override fun [hashCode](../../healthstack.kit.task.base/-task/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)()<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [callback](../../healthstack.kit.task.base/-task/callback.html) | [androidJvm]<br>var [callback](../../healthstack.kit.task.base/-task/callback.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is finished |
| [canceled](../../healthstack.kit.task.base/-task/canceled.html) | [androidJvm]<br>var [canceled](../../healthstack.kit.task.base/-task/canceled.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is canceled |
| [description](../../healthstack.kit.task.base/-task/description.html) | [androidJvm]<br>val [description](../../healthstack.kit.task.base/-task/description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>concise description of task |
| [id](../../healthstack.kit.task.base/-task/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-task/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [isActive](../../healthstack.kit.task.base/-task/is-active.html) | [androidJvm]<br>var [isActive](../../healthstack.kit.task.base/-task/is-active.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true |
| [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html) | [androidJvm]<br>var [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false<br>flag for completion of task |
| [name](../../healthstack.kit.task.base/-task/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-task/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [revisionId](revision-id.html) | [androidJvm]<br>val [revisionId](revision-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [startedAt](started-at.html) | [androidJvm]<br>var [startedAt](started-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null |
| [step](step.html) | [androidJvm]<br>val [step](step.html): [SurveyStep](../../healthstack.kit.task.survey.step/-survey-step/index.html) |
| [taskId](task-id.html) | [androidJvm]<br>val [taskId](task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

