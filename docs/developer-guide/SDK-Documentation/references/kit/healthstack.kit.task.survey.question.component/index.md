
[Kit](../../kit.html) > [healthstack.kit.task.survey.question.component](index.html)



# Package healthstack.kit.task.survey.question.component



## Types


| Name | Summary |
|---|---|
| [ChoiceQuestionComponent](-choice-question-component/index.html) | [androidJvm]<br>class [ChoiceQuestionComponent](-choice-question-component/index.html)&lt;[T](-choice-question-component/index.html) : [ChoiceQuestionModel](../healthstack.kit.task.survey.question.model/-choice-question-model/index.html)&lt;*&gt;&gt; : [QuestionComponent](-question-component/index.html)&lt;[T](-choice-question-component/index.html)&gt; |
| [Component](-component/index.html) | [androidJvm]<br>abstract class [Component](-component/index.html)&lt;[T](-component/index.html) : [QuestionModel](../healthstack.kit.task.survey.question.model/-question-model/index.html)&lt;*&gt;&gt;<br>A UI rendering object for SubStep such as healthstack.kit.step.sub.QuestionSubStep. |
| [DateTimeQuestionComponent](-date-time-question-component/index.html) | [androidJvm]<br>class [DateTimeQuestionComponent](-date-time-question-component/index.html) : [QuestionComponent](-question-component/index.html)&lt;[DateTimeQuestionModel](../healthstack.kit.task.survey.question.model/-date-time-question-model/index.html)&gt; |
| [ImageQuestionComponent](-image-question-component/index.html) | [androidJvm]<br>class [ImageQuestionComponent](-image-question-component/index.html) : [QuestionComponent](-question-component/index.html)&lt;[ImageChoiceQuestionModel](../healthstack.kit.task.survey.question.model/-image-choice-question-model/index.html)&gt; |
| [MultiChoiceQuestionComponent](-multi-choice-question-component/index.html) | [androidJvm]<br>class [MultiChoiceQuestionComponent](-multi-choice-question-component/index.html) : [QuestionComponent](-question-component/index.html)&lt;[MultiChoiceQuestionModel](../healthstack.kit.task.survey.question.model/-multi-choice-question-model/index.html)&gt; |
| [QuestionComponent](-question-component/index.html) | [androidJvm]<br>abstract class [QuestionComponent](-question-component/index.html)&lt;[T](-question-component/index.html) : [QuestionModel](../healthstack.kit.task.survey.question.model/-question-model/index.html)&lt;*&gt;&gt; : [Component](-component/index.html)&lt;[T](-question-component/index.html)&gt; |
| [RankingQuestionComponent](-ranking-question-component/index.html) | [androidJvm]<br>class [RankingQuestionComponent](-ranking-question-component/index.html) : [QuestionComponent](-question-component/index.html)&lt;[RankingQuestionModel](../healthstack.kit.task.survey.question.model/-ranking-question-model/index.html)&gt; |
| [ResultObject](-result-object/index.html) | [androidJvm]<br>data class [ResultObject](-result-object/index.html)(val startTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;&quot;, val endTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;&quot;, val startDate: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;&quot;, val endDate: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;&quot;) |
| [TextInputQuestionComponent](-text-input-question-component/index.html) | [androidJvm]<br>class [TextInputQuestionComponent](-text-input-question-component/index.html) : [QuestionComponent](-question-component/index.html)&lt;[TextInputQuestionModel](../healthstack.kit.task.survey.question.model/-text-input-question-model/index.html)&gt; |


## Functions


| Name | Summary |
|---|---|
| [DropdownPreview](-dropdown-preview.html) | [androidJvm]<br>@[PreviewGenerated](../healthstack.kit.annotation/-preview-generated/index.html)<br>@Preview(showBackground = true)<br>@Composable<br>fun [DropdownPreview](-dropdown-preview.html)() |
| [RadioGroup](-radio-group.html) | [androidJvm]<br>@Composable<br>fun [RadioGroup](-radio-group.html)(choiceQuestion: [ChoiceQuestionModel](../healthstack.kit.task.survey.question.model/-choice-question-model/index.html)&lt;*&gt;, modifier: Modifier) |
| [RadioPreview](-radio-preview.html) | [androidJvm]<br>@[PreviewGenerated](../healthstack.kit.annotation/-preview-generated/index.html)<br>@Preview(showBackground = true)<br>@Composable<br>fun [RadioPreview](-radio-preview.html)() |
| [SliderPreview](-slider-preview.html) | [androidJvm]<br>@[PreviewGenerated](../healthstack.kit.annotation/-preview-generated/index.html)<br>@Preview(showBackground = true)<br>@Composable<br>fun [SliderPreview](-slider-preview.html)() |

