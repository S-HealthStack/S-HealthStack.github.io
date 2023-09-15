
[Kit](../../../kit.html) > [healthstack.kit.task.base](../index.html) > [View](index.html)



# View



[androidJvm]\
abstract class [View](index.html)&lt;[T](index.html) : [StepModel](../-step-model/index.html)&gt;

A UI rendering object for [Step](../-step/index.html).



It has composable function [Render](-render.html), which renders UI using data in healthstack.kit.tqask.base.TaskModel.



## Constructors


| | |
|---|---|
| [View](-view.html) | [androidJvm]<br>fun [View](-view.html)() |


## Functions


| Name | Summary |
|---|---|
| [Render](-render.html) | [androidJvm]<br>@Composable<br>abstract fun [Render](-render.html)(model: [T](index.html), callbackCollection: [CallbackCollection](../-callback-collection/index.html), holder: [SubStepHolder](../../healthstack.kit.task.survey.question/-sub-step-holder/index.html)?)<br>A method rendering UI. |


## Inheritors


| Name |
|---|
| [ColorWordChallengeMeasureView](../../healthstack.kit.task.activity.view/-color-word-challenge-measure-view/index.html) |
| [GuidedBreathingMeasureView](../../healthstack.kit.task.activity.view/-guided-breathing-measure-view/index.html) |
| [MobileSpirometryMeasureView](../../healthstack.kit.task.activity.view/-mobile-spirometry-measure-view/index.html) |
| [ReactionTimeMeasureView](../../healthstack.kit.task.activity.view/-reaction-time-measure-view/index.html) |
| [SpeechRecognitionMeasureView](../../healthstack.kit.task.activity.view/-speech-recognition-measure-view/index.html) |
| [SustainedPhonationMeasureView](../../healthstack.kit.task.activity.view/-sustained-phonation-measure-view/index.html) |
| [TappingSpeedMeasureView](../../healthstack.kit.task.activity.view/-tapping-speed-measure-view/index.html) |
| [SimpleActivityView](../../healthstack.kit.task.activity.view.common/-simple-activity-view/index.html) |
| [SimpleAudioActivityView](../../healthstack.kit.task.activity.view.common/-simple-audio-activity-view/index.html) |
| [SimpleTimerActivityView](../../healthstack.kit.task.activity.view.common/-simple-timer-activity-view/index.html) |
| [ConsentTextView](../../healthstack.kit.task.onboarding.view/-consent-text-view/index.html) |
| [EligibilityIntroView](../../healthstack.kit.task.onboarding.view/-eligibility-intro-view/index.html) |
| [EligibilityResultView](../../healthstack.kit.task.onboarding.view/-eligibility-result-view/index.html) |
| [IntroView](../../healthstack.kit.task.onboarding.view/-intro-view/index.html) |
| [RegistrationCompletedView](../../healthstack.kit.task.signup.view/-registration-completed-view/index.html) |
| [SignUpView](../../healthstack.kit.task.signup.view/-sign-up-view/index.html) |
| [SurveyView](../../healthstack.kit.task.survey.view/-survey-view/index.html) |

