
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [ColorWordChallengeActivityTask](index.html) > [ColorWordChallengeActivityTask](-color-word-challenge-activity-task.html)



# ColorWordChallengeActivityTask



[androidJvm]\
fun [ColorWordChallengeActivityTask](-color-word-challenge-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleViewActivityStep(
            id, name, ColorWordChallengeIntroModel(id, name)
        ),
        ColorWordChallengeMeasureStep(
            id, name, ColorWordChallengeMeasureModel(id, name),
        ),
        SimpleViewActivityStep(
            id, name, ColorWordChallengeResultModel(id, name, header = completionTitle, body = completionDescription)
        ),
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




