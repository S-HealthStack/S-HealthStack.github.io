
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [GaitAndBalanceActivityTask](index.html) > [GaitAndBalanceActivityTask](-gait-and-balance-activity-task.html)



# GaitAndBalanceActivityTask



[androidJvm]\
fun [GaitAndBalanceActivityTask](-gait-and-balance-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Gait &amp; Balance&quot;, description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleViewActivityStep(
            id, name,
            GaitAndBalanceIntroModel(id)
        ),
        SimpleViewActivityStep(
            id, name,
            GaitAndBalanceGMeasureModel(
                id,
                header = &quot;Walk in a straight line unassisted for 20 steps&quot;,
                buttonText = &quot;Done&quot;
            )
        ),
        SimpleViewActivityStep(
            id, name,
            GaitAndBalanceGMeasureModel(
                id,
                header = &quot;Turn around and walk back to your starting point&quot;,
                drawableId = R.drawable.ic_activity_gait_and_balance_back,
                buttonText = &quot;Done&quot;
            )
        ),
        SimpleTimerActivityStep(
            id, name,
            GaitAndBalanceBMeasureModel(
                id,
                header = &quot;Stand still for 20 seconds&quot;,
                timeSeconds = 20,
                interactionType = VIBRATE,
            )
        ),
        SimpleViewActivityStep(
            id, name,
            GaitAndBalanceResultModel(id, name, header = completionTitle, body = completionDescription)
        )
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




