
[Kit](../../../kit.html) > [healthstack.kit.task.survey.question.model](../index.html) > [MultiChoiceQuestionModel](index.html)



# MultiChoiceQuestionModel



[androidJvm]\
open class [MultiChoiceQuestionModel](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; = emptyList(), val candidates: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;, tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) : [QuestionModel](../-question-model/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;



## Constructors


| | |
|---|---|
| [MultiChoiceQuestionModel](-multi-choice-question-model.html) | [androidJvm]<br>fun [MultiChoiceQuestionModel](-multi-choice-question-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; = emptyList(), candidates: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;, tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Types


| Name | Summary |
|---|---|
| [ViewType](-view-type/index.html) | [androidJvm]<br>enum [ViewType](-view-type/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[MultiChoiceQuestionModel.ViewType](-view-type/index.html)&gt; |


## Functions


| Name | Summary |
|---|---|
| [deselect](deselect.html) | [androidJvm]<br>fun [deselect](deselect.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |
| [getResponse](get-response.html) | [androidJvm]<br>open override fun [getResponse](get-response.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [isCorrect](../-question-model/is-correct.html) | [androidJvm]<br>fun [isCorrect](../-question-model/is-correct.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isSelected](is-selected.html) | [androidJvm]<br>fun [isSelected](is-selected.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [select](select.html) | [androidJvm]<br>fun [select](select.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [candidates](candidates.html) | [androidJvm]<br>val [candidates](candidates.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |
| [drawableId](../-question-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../-question-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? |
| [explanation](../-question-model/explanation.html) | [androidJvm]<br>val [explanation](../-question-model/explanation.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
| [id](../-question-model/id.html) | [androidJvm]<br>val [id](../-question-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [question](../-question-model/question.html) | [androidJvm]<br>val [question](../-question-model/question.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [skipLogics](../-question-model/skip-logics.html) | [androidJvm]<br>val [skipLogics](../-question-model/skip-logics.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; |
| [type](../-question-model/type.html) | [androidJvm]<br>val [type](../-question-model/type.html): [QuestionModel.QuestionType](../-question-model/-question-type/index.html) |
| [viewType](view-type.html) | [androidJvm]<br>val [viewType](view-type.html): [MultiChoiceQuestionModel.ViewType](-view-type/index.html) |

