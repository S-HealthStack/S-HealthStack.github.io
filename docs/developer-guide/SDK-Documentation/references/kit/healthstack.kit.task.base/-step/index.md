
[Kit](../../../kit.html) > [healthstack.kit.task.base](../index.html) > [Step](index.html)



# Step



[androidJvm]\
abstract class [Step](index.html)&lt;[T](index.html) : [StepModel](../-step-model/index.html), [R](index.html)&gt;(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val model: [T](index.html), val view: [View](../-view/index.html)&lt;[T](index.html)&gt;, getResult: () -&gt; [R](index.html))

An object representing an action(=a single page) such as Intro page.



It maps a [Model](../-step-model/index.html) and a [View](../-view/index.html).



Then, View renders UI with data of Model.



## Constructors


| | |
|---|---|
| [Step](-step.html) | [androidJvm]<br>fun &lt;[T](index.html) : [StepModel](../-step-model/index.html), [R](index.html)&gt; [Step](-step.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [T](index.html), view: [View](../-view/index.html)&lt;[T](index.html)&gt;, getResult: () -&gt; [R](index.html)) |


## Functions


| Name | Summary |
|---|---|
| [getState](get-state.html) | [androidJvm]<br>fun [getState](get-state.html)(): [T](index.html)<br>A method for getting state of Step. |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>abstract fun [Render](-render.html)(callbackCollection: [CallbackCollection](../-callback-collection/index.html))<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [id](id.html) | [androidJvm]<br>val [id](id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [model](model.html) | [androidJvm]<br>val [model](model.html): [T](index.html)<br>data object for UI & state management |
| [name](name.html) | [androidJvm]<br>val [name](name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [result](result.html) | [androidJvm]<br>var [result](result.html): [R](index.html) |
| [view](view.html) | [androidJvm]<br>val [view](view.html): [View](../-view/index.html)&lt;[T](index.html)&gt;<br>view object holding UI method |


## Inheritors


| Name |
|---|
| [ColorWordChallengeMeasureStep](../../healthstack.kit.task.activity.step/-color-word-challenge-measure-step/index.html) |
| [GuidedBreathingMeasureStep](../../healthstack.kit.task.activity.step/-guided-breathing-measure-step/index.html) |
| [MobileSpirometryMeasureStep](../../healthstack.kit.task.activity.step/-mobile-spirometry-measure-step/index.html) |
| [RangeOfMotionMeasureStep](../../healthstack.kit.task.activity.step/-range-of-motion-measure-step/index.html) |
| [ReactionTimeMeasureStep](../../healthstack.kit.task.activity.step/-reaction-time-measure-step/index.html) |
| [SpeechRecognitionMeasureStep](../../healthstack.kit.task.activity.step/-speech-recognition-measure-step/index.html) |
| [SustainedPhonationMeasureStep](../../healthstack.kit.task.activity.step/-sustained-phonation-measure-step/index.html) |
| [TappingSpeedMeasureStep](../../healthstack.kit.task.activity.step/-tapping-speed-measure-step/index.html) |
| [SimpleAudioActivityStep](../../healthstack.kit.task.activity.step.common/-simple-audio-activity-step/index.html) |
| [SimpleTimerActivityStep](../../healthstack.kit.task.activity.step.common/-simple-timer-activity-step/index.html) |
| [SimpleViewActivityStep](../../healthstack.kit.task.activity.step.common/-simple-view-activity-step/index.html) |
| [ConsentTextStep](../../healthstack.kit.task.onboarding.step/-consent-text-step/index.html) |
| [EligibilityIntroStep](../../healthstack.kit.task.onboarding.step/-eligibility-intro-step/index.html) |
| [EligibilityResultStep](../../healthstack.kit.task.onboarding.step/-eligibility-result-step/index.html) |
| [IntroStep](../../healthstack.kit.task.onboarding.step/-intro-step/index.html) |
| [RegistrationCompletedStep](../../healthstack.kit.task.signup.step/-registration-completed-step/index.html) |
| [SignUpStep](../../healthstack.kit.task.signup.step/-sign-up-step/index.html) |
| [SurveyStep](../../healthstack.kit.task.survey.step/-survey-step/index.html) |

