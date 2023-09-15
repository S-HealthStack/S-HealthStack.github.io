
[Kit](../../../kit.html) > [healthstack.kit.task.survey.question.model](../index.html) > [QuestionModel](index.html)



# QuestionModel



[androidJvm]\
abstract class [QuestionModel](index.html)&lt;[R](index.html)&gt;(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val question: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val type: [QuestionModel.QuestionType](-question-type/index.html), val skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;, answer: [R](index.html)? = null)



## Constructors


| | |
|---|---|
| [QuestionModel](-question-model.html) | [androidJvm]<br>fun &lt;[R](index.html)&gt; [QuestionModel](-question-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), question: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, type: [QuestionModel.QuestionType](-question-type/index.html), skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;, answer: [R](index.html)? = null) |


## Types


| Name | Summary |
|---|---|
| [QuestionType](-question-type/index.html) | [androidJvm]<br>enum [QuestionType](-question-type/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[QuestionModel.QuestionType](-question-type/index.html)&gt; |


## Functions


| Name | Summary |
|---|---|
| [getResponse](get-response.html) | [androidJvm]<br>abstract fun [getResponse](get-response.html)(): [R](index.html)? |
| [isCorrect](is-correct.html) | [androidJvm]<br>fun [isCorrect](is-correct.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |


## Properties


| Name | Summary |
|---|---|
| [drawableId](drawable-id.html) | [androidJvm]<br>val [drawableId](drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null |
| [explanation](explanation.html) | [androidJvm]<br>val [explanation](explanation.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null |
| [id](id.html) | [androidJvm]<br>val [id](id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [question](question.html) | [androidJvm]<br>val [question](question.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [skipLogics](skip-logics.html) | [androidJvm]<br>val [skipLogics](skip-logics.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; |
| [type](type.html) | [androidJvm]<br>val [type](type.html): [QuestionModel.QuestionType](-question-type/index.html) |


## Inheritors


| Name |
|---|
| [ChoiceQuestionModel](../-choice-question-model/index.html) |
| [DateTimeQuestionModel](../-date-time-question-model/index.html) |
| [ImageChoiceQuestionModel](../-image-choice-question-model/index.html) |
| [MultiChoiceQuestionModel](../-multi-choice-question-model/index.html) |
| [RankingQuestionModel](../-ranking-question-model/index.html) |
| [TextInputQuestionModel](../-text-input-question-model/index.html) |

