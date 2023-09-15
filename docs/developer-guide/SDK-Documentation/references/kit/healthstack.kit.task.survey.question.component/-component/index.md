
[Kit](../../../kit.html) > [healthstack.kit.task.survey.question.component](../index.html) > [Component](index.html)



# Component



[androidJvm]\
abstract class [Component](index.html)&lt;[T](index.html) : [QuestionModel](../../healthstack.kit.task.survey.question.model/-question-model/index.html)&lt;*&gt;&gt;

A UI rendering object for SubStep such as healthstack.kit.step.sub.QuestionSubStep.



It has composable function [Render](-render.html), which renders UI using data in healthstack.kit.model.Model.



It looks similar with healthstack.kit.view.View.



But Component cannot render a whole page unlike View.



Component can only render a partial &quot;UI component&quot; such as one question in a survey



## Constructors


| | |
|---|---|
| [Component](-component.html) | [androidJvm]<br>fun [Component](-component.html)() |


## Functions


| Name | Summary |
|---|---|
| [Render](-render.html) | [androidJvm]<br>@Composable<br>abstract fun [Render](-render.html)(model: [T](index.html), callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html))<br>A method rendering UI. |


## Inheritors


| Name |
|---|
| [QuestionComponent](../-question-component/index.html) |

