
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [RangeOfMotionMeasureModel](index.html)



# RangeOfMotionMeasureModel



[androidJvm]\
class [RangeOfMotionMeasureModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Right Arm Circumduction&quot;, val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(
        &quot;Place phone in your right hand.&quot;,
        &quot;Straighten your right arm and move it in a full circle for 20 sec&quot;,
    ), val textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER, val timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 20, val autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, val interactionType: [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) = InteractionType.VIBRATE, isRightHand: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, val dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = if (isRightHand) &quot;right&quot; else &quot;left&quot;, val sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt; = listOf(GYROSCOPE, ACCELEROMETER)) : [SimpleTimerActivityModel](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/index.html)



## Constructors


| | |
|---|---|
| [RangeOfMotionMeasureModel](-range-of-motion-measure-model.html) | [androidJvm]<br>fun [RangeOfMotionMeasureModel](-range-of-motion-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Right Arm Circumduction&quot;, body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(         &quot;Place phone in your right hand.&quot;,         &quot;Straighten your right arm and move it in a full circle for 20 sec&quot;,     ), textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER, timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 20, autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, interactionType: [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) = InteractionType.VIBRATE, isRightHand: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = if (isRightHand) &quot;right&quot; else &quot;left&quot;, sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt; = listOf(GYROSCOPE, ACCELEROMETER)) |


## Functions


| Name | Summary |
|---|---|
| [close](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/close.html) | [androidJvm]<br>fun [close](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/close.html)() |
| [init](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/init.html) | [androidJvm]<br>fun [init](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/init.html)() |


## Properties


| Name | Summary |
|---|---|
| [accelerometer](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/accelerometer.html) | [androidJvm]<br>val [accelerometer](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/accelerometer.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt;&gt;? |
| [autoFlip](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/auto-flip.html) | [androidJvm]<br>val [autoFlip](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/auto-flip.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false |
| [body](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/body.html) | [androidJvm]<br>val [body](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/body.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null |
| [dataPrefix](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/data-prefix.html) | [androidJvm]<br>val [dataPrefix](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/data-prefix.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [gyroscope](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/gyroscope.html) | [androidJvm]<br>val [gyroscope](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/gyroscope.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt;&gt;? |
| [header](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/header.html) | [androidJvm]<br>val [header](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/header.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [interactionType](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/interaction-type.html) | [androidJvm]<br>val [interactionType](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/interaction-type.html): [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) |
| [sensors](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/sensors.html) | [androidJvm]<br>val [sensors](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/sensors.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt; |
| [textType](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/text-type.html) | [androidJvm]<br>val [textType](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/text-type.html): [TextType](../../healthstack.kit.ui/-text-type/index.html) |
| [timeMillis](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/time-millis.html) | [androidJvm]<br>val [timeMillis](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/time-millis.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)&gt; |
| [timeSeconds](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/time-seconds.html) | [androidJvm]<br>val [timeSeconds](../../healthstack.kit.task.activity.model.common/-simple-timer-activity-model/time-seconds.html): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 10 |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

