
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [RangeOfMotionActivityTask](index.html) > [RangeOfMotionActivityTask](-range-of-motion-activity-task.html)



# RangeOfMotionActivityTask



[androidJvm]\
fun [RangeOfMotionActivityTask](-range-of-motion-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleViewActivityStep(
            id, name, RangeOfMotionIntroModel(id, name)
        ),
        SimpleViewActivityStep(
            id,
            name,
            RangeOfMotionIntroModel(
                id = id,
                title = name,
                header = &quot;Right Arm Circumduction&quot;,
                body = listOf(
                    &quot;Place phone in your right hand.&quot;,
                    &quot;Straighten your right arm and move it in a full circle for 20 sec.&quot;
                ),
                drawableId = R.drawable.ic_activity_range_of_motion_right_arm,
                buttonText = &quot;Start Exercise&quot;,
            )
        ),
        RangeOfMotionMeasureStep(
            id, name, RangeOfMotionMeasureModel(id, name),
        ),
        SimpleViewActivityStep(
            id,
            name,
            RangeOfMotionResultModel(
                id,
                name,
                header = completionTitle,
                body = completionDescription,
                buttonText = &quot;Continue&quot;
            )
        ),
        SimpleViewActivityStep(
            id,
            name,
            RangeOfMotionIntroModel(
                id = id,
                title = name,
                header = &quot;Left Arm Circumduction&quot;,
                body = listOf(
                    &quot;Place phone in your left hand.&quot;,
                    &quot;Straighten your left arm and move it in a full circle for 20 sec.&quot;,
                ),
                drawableId = R.drawable.ic_activity_range_of_motion_left_arm,
                buttonText = &quot;Start Exercise&quot;,
            )
        ),
        RangeOfMotionMeasureStep(
            id,
            name,
            RangeOfMotionMeasureModel(
                id,
                name,
                header = &quot;Left Arm Circumduction&quot;,
                body = listOf(
                    &quot;Place phone in your left hand.&quot;,
                    &quot;Straighten your left arm and move it in a full circle for 20 sec&quot;,
                ),
                isRightHand = false,
            )
        ),
        SimpleViewActivityStep(
            id,
            name,
            RangeOfMotionResultModel(
                id,
                name,
                header = completionTitle,
                body = completionDescription,
            )
        ),
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




