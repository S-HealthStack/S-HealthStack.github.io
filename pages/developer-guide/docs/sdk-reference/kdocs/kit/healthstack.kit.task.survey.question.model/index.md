---



title: healthstack.kit.task.survey.question.model
permalink: /kit/healthstack.kit.task.survey.question.model/index.html



sidebar: dev_doc_sidebar


---



//[kit](/kit.html)/[healthstack.kit.task.survey.question.model](index.html)



# Package healthstack.kit.task.survey.question.model



## Types


| Name | Summary |
|---|---|
| [ChoiceQuestionModel](-choice-question-model/index.html) | [androidJvm]<br>class [ChoiceQuestionModel](-choice-question-model/index.html)&lt;[R](-choice-question-model/index.html)&gt;(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, answer: [R](-choice-question-model/index.html)? = null, val candidates: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[R](-choice-question-model/index.html)&gt;, val viewType: [ChoiceQuestionModel.ViewType](-choice-question-model/-view-type/index.html) = Radio) : [QuestionModel](-question-model/index.html)&lt;[R](-choice-question-model/index.html)&gt; |
| [MultiChoiceQuestionModel](-multi-choice-question-model/index.html) | [androidJvm]<br>open class [MultiChoiceQuestionModel](-multi-choice-question-model/index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val candidates: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;) : [QuestionModel](-question-model/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |
| [QuestionModel](-question-model/index.html) | [androidJvm]<br>abstract class [QuestionModel](-question-model/index.html)&lt;[R](-question-model/index.html)&gt;(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val question: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val type: [QuestionModel.QuestionType](-question-model/-question-type/index.html), answer: [R](-question-model/index.html)? = null) |
| [TextInputQuestionModel](-text-input-question-model/index.html) | [androidJvm]<br>class [TextInputQuestionModel](-text-input-question-model/index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), query: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, answer: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null) : [QuestionModel](-question-model/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |



