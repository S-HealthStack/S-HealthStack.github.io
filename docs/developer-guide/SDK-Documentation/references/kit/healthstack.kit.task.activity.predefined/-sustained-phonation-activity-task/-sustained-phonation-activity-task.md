
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [SustainedPhonationActivityTask](index.html) > [SustainedPhonationActivityTask](-sustained-phonation-activity-task.html)



# SustainedPhonationActivityTask



[androidJvm]\
fun [SustainedPhonationActivityTask](-sustained-phonation-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleAudioActivityStep(
            id, name, SustainedPhonationIntroModel(id, name)
        ),
        SustainedPhonationMeasureStep(
            id, name, SustainedPhonationMeasureModel(id, name)
        ),
        SimpleViewActivityStep(
            id, name, SustainedPhonationResultModel(id, name, header = completionTitle, body = completionDescription)
        ),
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




