
[Kit](../../../kit.html) > [healthstack.kit.task.activity](../index.html) > [ActivityTask](index.html)



# ActivityTask



[androidJvm]\
abstract class [ActivityTask](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt;) : [OrderedTask](../../healthstack.kit.task.base/-ordered-task/index.html)



## Constructors


| | |
|---|---|
| [ActivityTask](-activity-task.html) | [androidJvm]<br>fun [ActivityTask](-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt;) |


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
| [pageCallbacks](page-callbacks.html) | [androidJvm]<br>open override val [pageCallbacks](page-callbacks.html): [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html)<br>An object including callback. |
| [result](result.html) | [androidJvm]<br>val [result](result.html): [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; |
| [startedAt](started-at.html) | [androidJvm]<br>var [startedAt](started-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null |
| [steps](../../healthstack.kit.task.base/-ordered-task/steps.html) | [androidJvm]<br>val [steps](../../healthstack.kit.task.base/-ordered-task/steps.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; |
| [taskId](task-id.html) | [androidJvm]<br>val [taskId](task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |


## Inheritors


| Name |
|---|
| [ColorWordChallengeActivityTask](../../healthstack.kit.task.activity.predefined/-color-word-challenge-activity-task/index.html) |
| [GaitAndBalanceActivityTask](../../healthstack.kit.task.activity.predefined/-gait-and-balance-activity-task/index.html) |
| [GuidedBreathingActivityTask](../../healthstack.kit.task.activity.predefined/-guided-breathing-activity-task/index.html) |
| [MobileSpirometryActivityTask](../../healthstack.kit.task.activity.predefined/-mobile-spirometry-activity-task/index.html) |
| [RangeOfMotionActivityTask](../../healthstack.kit.task.activity.predefined/-range-of-motion-activity-task/index.html) |
| [ReactionTimeActivityTask](../../healthstack.kit.task.activity.predefined/-reaction-time-activity-task/index.html) |
| [SpeechRecognitionActivityTask](../../healthstack.kit.task.activity.predefined/-speech-recognition-activity-task/index.html) |
| [SustainedPhonationActivityTask](../../healthstack.kit.task.activity.predefined/-sustained-phonation-activity-task/index.html) |
| [TappingSpeedActivityTask](../../healthstack.kit.task.activity.predefined/-tapping-speed-activity-task/index.html) |

