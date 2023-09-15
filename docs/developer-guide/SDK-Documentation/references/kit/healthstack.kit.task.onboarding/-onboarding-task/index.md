
[Kit](../../../kit.html) > [healthstack.kit.task.onboarding](../index.html) > [OnboardingTask](index.html)



# OnboardingTask



[androidJvm]\
open class [OnboardingTask](index.html) : [OrderedTask](../../healthstack.kit.task.base/-ordered-task/index.html)



## Constructors


| | |
|---|---|
| [OnboardingTask](-onboarding-task.html) | [androidJvm]<br>fun [OnboardingTask](-onboarding-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), introStep: [IntroStep](../../healthstack.kit.task.onboarding.step/-intro-step/index.html)) |
| [OnboardingTask](-onboarding-task.html) | [androidJvm]<br>fun [OnboardingTask](-onboarding-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), introStep: [IntroStep](../../healthstack.kit.task.onboarding.step/-intro-step/index.html), eligibilityIntroStep: [EligibilityIntroStep](../../healthstack.kit.task.onboarding.step/-eligibility-intro-step/index.html), eligibilityCheckerStep: [EligibilityCheckerStep](../../healthstack.kit.task.onboarding.step/-eligibility-checker-step/index.html), eligibilityResultStep: [EligibilityResultStep](../../healthstack.kit.task.onboarding.step/-eligibility-result-step/index.html), consentTextStep: [ConsentTextStep](../../healthstack.kit.task.onboarding.step/-consent-text-step/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [CardView](../../healthstack.kit.task.base/-ordered-task/-card-view.html) | [androidJvm]<br>@Composable<br>open override fun [CardView](../../healthstack.kit.task.base/-ordered-task/-card-view.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A method for rendering CardView UI. |
| [equals](../../healthstack.kit.task.base/-task/equals.html) | [androidJvm]<br>open operator override fun [equals](../../healthstack.kit.task.base/-task/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](../../healthstack.kit.task.base/-task/hash-code.html) | [androidJvm]<br>open override fun [hashCode](../../healthstack.kit.task.base/-task/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [Render](../../healthstack.kit.task.base/-ordered-task/-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](../../healthstack.kit.task.base/-ordered-task/-render.html)()<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [callback](../../healthstack.kit.task.base/-task/callback.html) | [androidJvm]<br>var [callback](../../healthstack.kit.task.base/-task/callback.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is finished |
| [canceled](../../healthstack.kit.task.base/-task/canceled.html) | [androidJvm]<br>var [canceled](../../healthstack.kit.task.base/-task/canceled.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is canceled |
| [description](../../healthstack.kit.task.base/-task/description.html) | [androidJvm]<br>val [description](../../healthstack.kit.task.base/-task/description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>concise description of task |
| [eligibility](eligibility.html) | [androidJvm]<br>var [eligibility](eligibility.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false |
| [id](../../healthstack.kit.task.base/-task/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-task/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [isActive](../../healthstack.kit.task.base/-task/is-active.html) | [androidJvm]<br>var [isActive](../../healthstack.kit.task.base/-task/is-active.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true |
| [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html) | [androidJvm]<br>var [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false<br>flag for completion of task |
| [name](../../healthstack.kit.task.base/-task/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-task/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [pageCallbacks](page-callbacks.html) | [androidJvm]<br>open override val [pageCallbacks](page-callbacks.html): [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html)<br>An object including callback. |
| [steps](../../healthstack.kit.task.base/-ordered-task/steps.html) | [androidJvm]<br>val [steps](../../healthstack.kit.task.base/-ordered-task/steps.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; |

