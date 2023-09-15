
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [TappingSpeedActivityTask](index.html) > [TappingSpeedActivityTask](-tapping-speed-activity-task.html)



# TappingSpeedActivityTask



[androidJvm]\
fun [TappingSpeedActivityTask](-tapping-speed-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Tapping Speed&quot;, description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleViewActivityStep(
            id, name,
            TappingSpeedIntroModel(
                id, name
            )
        ),
        SimpleViewActivityStep(
            id, name,
            TappingSpeedIntroModel(
                id, name,
                body = &quot;Place your phone on a flat surface.\n&quot; +
                    &quot;Use two fingers on right hand to alternatively tap the buttons on the screen.\n&quot; +
                    &quot;Keep tapping for 10 seconds.&quot;,
                buttonText = &quot;Start Exercise&quot;
            )
        ),
        TappingSpeedMeasureStep(
            id, name,
            TappingSpeedMeasureModel(
                id, name, null, measureTimeSecond = 10
            )
        ),
        SimpleViewActivityStep(
            id, name,
            TappingSpeedIntroModel(
                id, name,
                body = &quot;Place your phone on a flat surface.\n&quot; +
                    &quot;Use two fingers on left hand to alternatively tap the buttons on the screen.\n&quot; +
                    &quot;Keep tapping for 10 seconds.&quot;,
                drawableId = R.drawable.ic_left_tapping_speed,
                buttonText = &quot;Start Exercise&quot;
            )
        ),
        TappingSpeedMeasureStep(
            id, name,
            TappingSpeedMeasureModel(
                id, name, null, false, 10
            )
        ),
        SimpleViewActivityStep(
            id, name,
            TappingSpeedResultModel(
                id, name, header = completionTitle, body = completionDescription
            )
        )
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




