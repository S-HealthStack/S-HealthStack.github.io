
[Kit](../../../kit.html) > [healthstack.kit.task.survey.question](../index.html) > [SubStepHolder](index.html)



# SubStepHolder



[androidJvm]\
class [SubStepHolder](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val subSteps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[QuestionSubStep](../-question-sub-step/index.html)&lt;*, *&gt;&gt;&gt;)

An object for holding one or more SubSteps



SubStep's healthstack.kit.view.component.Component only renders a partial UI component.



So, a Component has to depend on higher UI object.



SubStepHolder helps managing SubSteps, and integrating UIs of Components



For example, multiple QuestionSubSteps can be managed by a SubStepHolder.



## Constructors


| | |
|---|---|
| [SubStepHolder](-sub-step-holder.html) | [androidJvm]<br>fun [SubStepHolder](-sub-step-holder.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), subSteps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[QuestionSubStep](../-question-sub-step/index.html)&lt;*, *&gt;&gt;&gt;) |


## Functions


| Name | Summary |
|---|---|
| [isSufficient](is-sufficient.html) | [androidJvm]<br>fun [isSufficient](is-sufficient.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>A method to get result using its subSteps. |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>fun [Render](-render.html)(callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html), index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [id](id.html) | [androidJvm]<br>val [id](id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [name](name.html) | [androidJvm]<br>val [name](name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [subSteps](sub-steps.html) | [androidJvm]<br>val [subSteps](sub-steps.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[QuestionSubStep](../-question-sub-step/index.html)&lt;*, *&gt;&gt;&gt;<br>a list of subSteps to manage |

