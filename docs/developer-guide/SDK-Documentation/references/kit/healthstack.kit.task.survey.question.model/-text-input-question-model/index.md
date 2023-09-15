
[Kit](../../../kit.html) > [healthstack.kit.task.survey.question.model](../index.html) > [TextInputQuestionModel](index.html)



# TextInputQuestionModel



[androidJvm]\
class [TextInputQuestionModel](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; = emptyList(), answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val maxCharacter: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 500) : [QuestionModel](../-question-model/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;



## Constructors


| | |
|---|---|
| [TextInputQuestionModel](-text-input-question-model.html) | [androidJvm]<br>fun [TextInputQuestionModel](-text-input-question-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, skipLogics: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; = emptyList(), answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, maxCharacter: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 500) |


## Functions


| Name | Summary |
|---|---|
| [getResponse](get-response.html) | [androidJvm]<br>open override fun [getResponse](get-response.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [isCorrect](../-question-model/is-correct.html) | [androidJvm]<br>fun [isCorrect](../-question-model/is-correct.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |


## Properties


| Name | Summary |
|---|---|
| [drawableId](../-question-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../-question-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? |
| [explanation](../-question-model/explanation.html) | [androidJvm]<br>val [explanation](../-question-model/explanation.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
| [id](../-question-model/id.html) | [androidJvm]<br>val [id](../-question-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [input](input.html) | [androidJvm]<br>var [input](input.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [maxCharacter](max-character.html) | [androidJvm]<br>val [maxCharacter](max-character.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 500 |
| [question](../-question-model/question.html) | [androidJvm]<br>val [question](../-question-model/question.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [skipLogics](../-question-model/skip-logics.html) | [androidJvm]<br>val [skipLogics](../-question-model/skip-logics.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt; |
| [type](../-question-model/type.html) | [androidJvm]<br>val [type](../-question-model/type.html): [QuestionModel.QuestionType](../-question-model/-question-type/index.html) |

