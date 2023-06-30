---



title: Step
permalink: /kit/healthstack.kit.task.base/-step/index.html



sidebar: dev_doc_sidebar


---



//[kit](/kit.html)/[healthstack.kit.task.base](../index.html)/[Step](index.html)



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
| [ConsentTextStep](../../healthstack.kit.task.onboarding.step/-consent-text-step/index.html) |
| [EligibilityIntroStep](../../healthstack.kit.task.onboarding.step/-eligibility-intro-step/index.html) |
| [EligibilityResultStep](../../healthstack.kit.task.onboarding.step/-eligibility-result-step/index.html) |
| [IntroStep](../../healthstack.kit.task.onboarding.step/-intro-step/index.html) |
| [RegistrationCompletedStep](../../healthstack.kit.task.signup.step/-registration-completed-step/index.html) |
| [SignUpStep](../../healthstack.kit.task.signup.step/-sign-up-step/index.html) |
| [SurveyStep](../../healthstack.kit.task.survey.step/-survey-step/index.html) |



