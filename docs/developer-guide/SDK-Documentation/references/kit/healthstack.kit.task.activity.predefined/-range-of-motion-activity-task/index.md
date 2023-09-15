
[Kit](../../../kit.html) > [healthstack.kit.task.activity.predefined](../index.html) > [RangeOfMotionActivityTask](index.html)



# RangeOfMotionActivityTask



[androidJvm]\
class [RangeOfMotionActivityTask](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, val steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
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
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true) : [ActivityTask](../../healthstack.kit.task.activity/-activity-task/index.html)



## Constructors


| | |
|---|---|
| [RangeOfMotionActivityTask](-range-of-motion-activity-task.html) | [androidJvm]<br>fun [RangeOfMotionActivityTask](-range-of-motion-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(         SimpleViewActivityStep(             id, name, RangeOfMotionIntroModel(id, name)         ),         SimpleViewActivityStep(             id,             name,             RangeOfMotionIntroModel(                 id = id,                 title = name,                 header = &quot;Right Arm Circumduction&quot;,                 body = listOf(                     &quot;Place phone in your right hand.&quot;,                     &quot;Straighten your right arm and move it in a full circle for 20 sec.&quot;                 ),                 drawableId = R.drawable.ic_activity_range_of_motion_right_arm,                 buttonText = &quot;Start Exercise&quot;,             )         ),         RangeOfMotionMeasureStep(             id, name, RangeOfMotionMeasureModel(id, name),         ),         SimpleViewActivityStep(             id,             name,             RangeOfMotionResultModel(                 id,                 name,                 header = completionTitle,                 body = completionDescription,                 buttonText = &quot;Continue&quot;             )         ),         SimpleViewActivityStep(             id,             name,             RangeOfMotionIntroModel(                 id = id,                 title = name,                 header = &quot;Left Arm Circumduction&quot;,                 body = listOf(                     &quot;Place phone in your left hand.&quot;,                     &quot;Straighten your left arm and move it in a full circle for 20 sec.&quot;,                 ),                 drawableId = R.drawable.ic_activity_range_of_motion_left_arm,                 buttonText = &quot;Start Exercise&quot;,             )         ),         RangeOfMotionMeasureStep(             id,             name,             RangeOfMotionMeasureModel(                 id,                 name,                 header = &quot;Left Arm Circumduction&quot;,                 body = listOf(                     &quot;Place phone in your left hand.&quot;,                     &quot;Straighten your left arm and move it in a full circle for 20 sec&quot;,                 ),                 isRightHand = false,             )         ),         SimpleViewActivityStep(             id,             name,             RangeOfMotionResultModel(                 id,                 name,                 header = completionTitle,                 body = completionDescription,             )         ),     ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true) |


## Functions


| Name | Summary |
|---|---|
| [CardView](-card-view.html) | [androidJvm]<br>@Composable<br>open override fun [CardView](-card-view.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A method for rendering CardView UI. |
| [equals](../../healthstack.kit.task.base/-task/equals.html) | [androidJvm]<br>open operator override fun [equals](../../healthstack.kit.task.base/-task/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [hashCode](../../healthstack.kit.task.base/-task/hash-code.html) | [androidJvm]<br>open override fun [hashCode](../../healthstack.kit.task.base/-task/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [Render](../../healthstack.kit.task.activity/-activity-task/-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](../../healthstack.kit.task.activity/-activity-task/-render.html)()<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [callback](../../healthstack.kit.task.base/-task/callback.html) | [androidJvm]<br>var [callback](../../healthstack.kit.task.base/-task/callback.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is finished |
| [canceled](../../healthstack.kit.task.base/-task/canceled.html) | [androidJvm]<br>var [canceled](../../healthstack.kit.task.base/-task/canceled.html): () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)? = null<br>a method handling task's state when it is canceled |
| [description](../../healthstack.kit.task.base/-task/description.html) | [androidJvm]<br>val [description](../../healthstack.kit.task.base/-task/description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>concise description of task |
| [id](../../healthstack.kit.task.base/-task/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-task/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [isActive](../../healthstack.kit.task.base/-task/is-active.html) | [androidJvm]<br>var [isActive](../../healthstack.kit.task.base/-task/is-active.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true |
| [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html) | [androidJvm]<br>var [isCompleted](../../healthstack.kit.task.base/-task/is-completed.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false<br>flag for completion of task |
| [name](../../healthstack.kit.task.base/-task/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-task/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [pageCallbacks](../../healthstack.kit.task.activity/-activity-task/page-callbacks.html) | [androidJvm]<br>open override val [pageCallbacks](../../healthstack.kit.task.activity/-activity-task/page-callbacks.html): [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html)<br>An object including callback. |
| [result](../../healthstack.kit.task.activity/-activity-task/result.html) | [androidJvm]<br>val [result](../../healthstack.kit.task.activity/-activity-task/result.html): [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt; |
| [startedAt](../../healthstack.kit.task.activity/-activity-task/started-at.html) | [androidJvm]<br>var [startedAt](../../healthstack.kit.task.activity/-activity-task/started-at.html): [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html)? = null |
| [steps](../../healthstack.kit.task.base/-ordered-task/steps.html) | [androidJvm]<br>val [steps](../../healthstack.kit.task.base/-ordered-task/steps.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; |
| [taskId](../../healthstack.kit.task.activity/-activity-task/task-id.html) | [androidJvm]<br>val [taskId](../../healthstack.kit.task.activity/-activity-task/task-id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
