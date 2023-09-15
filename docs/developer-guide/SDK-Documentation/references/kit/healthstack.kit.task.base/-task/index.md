
[Kit](../../../kit.html) > [healthstack.kit.task.base](../index.html) > [Task](index.html)



# Task



[androidJvm]\
abstract class [Task](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))

An object representing a flow of actions(= a list of pages) such as survey flow or onBoarding flow.



It usually has one or more [Step](../-step/index.html)s as property.



SimpleTask - Task with one Step. OrderedTask - Task with multiple Steps.



## Constructors


| | |
|---|---|
| [Task](-task.html) | [androidJvm]<br>fun [Task](-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [CardView](-card-view.html) | [androidJvm]<br>@Composable<br>abstract fun [CardView](-card-view.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A method for rendering CardView UI. |
| [equals](equals.html) | [androidJvm]<br>open operator override fun [equals](equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](hash-code.html) | [androidJvm]<br>open override fun [hashCode](hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>abstract fun [Render](-render.html)()<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [callback](callback.html) | [androidJvm]<br>var [callback](callback.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is finished |
| [canceled](canceled.html) | [androidJvm]<br>var [canceled](canceled.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is canceled |
| [description](description.html) | [androidJvm]<br>val [description](description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>concise description of task |
| [id](id.html) | [androidJvm]<br>val [id](id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [isActive](is-active.html) | [androidJvm]<br>var [isActive](is-active.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true |
| [isCompleted](is-completed.html) | [androidJvm]<br>var [isCompleted](is-completed.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false<br>flag for completion of task |
| [name](name.html) | [androidJvm]<br>val [name](name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |


## Inheritors


| Name |
|---|
| [OrderedTask](../-ordered-task/index.html) |
| [SurveyTask](../../healthstack.kit.task.survey/-survey-task/index.html) |

