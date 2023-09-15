
[Kit](../../../kit.html) > [healthstack.kit.task.survey.step](../index.html) > [SurveyStep](index.html)



# SurveyStep



[androidJvm]\
open class [SurveyStep](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)&gt; = SurveyView(), val subStepHolder: [SubStepHolder](../../healthstack.kit.task.survey.question/-sub-step-holder/index.html)) : [Step](../../healthstack.kit.task.base/-step/index.html)&lt;[SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html), [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)&gt;



## Constructors


| | |
|---|---|
| [SurveyStep](-survey-step.html) | [androidJvm]<br>fun [SurveyStep](-survey-step.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)&gt; = SurveyView(), subStepHolder: [SubStepHolder](../../healthstack.kit.task.survey.question/-sub-step-holder/index.html)) |


## Types


| Name | Summary |
|---|---|
| [Builder](-builder/index.html) | [androidJvm]<br>class [Builder](-builder/index.html)(title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)&gt; = SurveyView()) |


## Functions


| Name | Summary |
|---|---|
| [getState](../../healthstack.kit.task.base/-step/get-state.html) | [androidJvm]<br>fun [getState](../../healthstack.kit.task.base/-step/get-state.html)(): [SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)<br>A method for getting state of Step. |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)(callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html))<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [id](../../healthstack.kit.task.base/-step/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [model](../../healthstack.kit.task.base/-step/model.html) | [androidJvm]<br>val [model](../../healthstack.kit.task.base/-step/model.html): [SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)<br>data object for UI & state management |
| [name](../../healthstack.kit.task.base/-step/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-step/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [result](../../healthstack.kit.task.base/-step/result.html) | [androidJvm]<br>var [result](../../healthstack.kit.task.base/-step/result.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [subStepHolder](sub-step-holder.html) | [androidJvm]<br>val [subStepHolder](sub-step-holder.html): [SubStepHolder](../../healthstack.kit.task.survey.question/-sub-step-holder/index.html) |
| [view](../../healthstack.kit.task.base/-step/view.html) | [androidJvm]<br>val [view](../../healthstack.kit.task.base/-step/view.html): [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SurveyModel](../../healthstack.kit.task.survey.model/-survey-model/index.html)&gt;<br>view object holding UI method |


## Inheritors


| Name |
|---|
| [EligibilityCheckerStep](../../healthstack.kit.task.onboarding.step/-eligibility-checker-step/index.html) |

