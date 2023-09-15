
[Kit](../../../kit.html) > [healthstack.kit.task.base](../index.html) > [OrderedTask](index.html)



# OrderedTask



[androidJvm]\
open class [OrderedTask](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../-step/index.html)&lt;out [StepModel](../-step-model/index.html), *&gt;&gt;) : [Task](../-task/index.html)

[Task](../-task/index.html) with multiple [Step](../-step/index.html)s OnboardingTask is an example of OrderedTask



## Constructors


| | |
|---|---|
| [OrderedTask](-ordered-task.html) | [androidJvm]<br>fun [OrderedTask](-ordered-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../-step/index.html)&lt;out [StepModel](../-step-model/index.html), *&gt;&gt;) |


## Types


| Name | Summary |
|---|---|
| [Progress](-progress/index.html) | [androidJvm]<br>inner class [Progress](-progress/index.html)<br>Inner class indicating progress of this [OrderedTask](index.html) |


## Functions


| Name | Summary |
|---|---|
| [CardView](-card-view.html) | [androidJvm]<br>@Composable<br>open override fun [CardView](-card-view.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A method for rendering CardView UI. |
| [equals](../-task/equals.html) | [androidJvm]<br>open operator override fun [equals](../-task/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](../-task/hash-code.html) | [androidJvm]<br>open override fun [hashCode](../-task/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)()<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [callback](../-task/callback.html) | [androidJvm]<br>var [callback](../-task/callback.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is finished |
| [canceled](../-task/canceled.html) | [androidJvm]<br>var [canceled](../-task/canceled.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is canceled |
| [description](../-task/description.html) | [androidJvm]<br>val [description](../-task/description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>concise description of task |
| [id](../-task/id.html) | [androidJvm]<br>val [id](../-task/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [isActive](../-task/is-active.html) | [androidJvm]<br>var [isActive](../-task/is-active.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true |
| [isCompleted](../-task/is-completed.html) | [androidJvm]<br>var [isCompleted](../-task/is-completed.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false<br>flag for completion of task |
| [name](../-task/name.html) | [androidJvm]<br>val [name](../-task/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [pageCallbacks](page-callbacks.html) | [androidJvm]<br>open val [pageCallbacks](page-callbacks.html): [CallbackCollection](../-callback-collection/index.html)<br>An object including callback. |
| [steps](steps.html) | [androidJvm]<br>val [steps](steps.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../-step/index.html)&lt;out [StepModel](../-step-model/index.html), *&gt;&gt; |


## Inheritors


| Name |
|---|
| [ActivityTask](../../healthstack.kit.task.activity/-activity-task/index.html) |
| [OnboardingTask](../../healthstack.kit.task.onboarding/-onboarding-task/index.html) |
| [SignUpTask](../../healthstack.kit.task.signup/-sign-up-task/index.html) |

