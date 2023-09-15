
[Kit](../../../../kit.html) > [healthstack.kit.task.survey](../../index.html) > [SurveyTask](../index.html) > [Builder](index.html)



# Builder



[androidJvm]\
class [Builder](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), callback: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), pageable: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)



## Constructors


| | |
|---|---|
| [Builder](-builder.html) | [androidJvm]<br>fun [Builder](-builder.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), revisionId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), callback: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), pageable: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true) |


## Functions


| Name | Summary |
|---|---|
| [addQuestion](add-question.html) | [androidJvm]<br>fun &lt;[R](add-question.html)&gt; [addQuestion](add-question.html)(question: [QuestionModel](../../../healthstack.kit.task.survey.question.model/-question-model/index.html)&lt;[R](add-question.html)&gt;) |
| [addSection](add-section.html) | [androidJvm]<br>fun [addSection](add-section.html)() |
| [build](build.html) | [androidJvm]<br>fun [build](build.html)(): [SurveyTask](../index.html) |

