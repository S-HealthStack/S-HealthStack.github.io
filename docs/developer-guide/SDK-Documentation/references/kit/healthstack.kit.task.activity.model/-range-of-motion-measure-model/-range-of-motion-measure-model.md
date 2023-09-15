
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [RangeOfMotionMeasureModel](index.html) > [RangeOfMotionMeasureModel](-range-of-motion-measure-model.html)



# RangeOfMotionMeasureModel



[androidJvm]\
fun [RangeOfMotionMeasureModel](-range-of-motion-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Right Arm Circumduction&quot;, body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(
        &quot;Place phone in your right hand.&quot;,
        &quot;Straighten your right arm and move it in a full circle for 20 sec&quot;,
    ), textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER, timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 20, autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, interactionType: [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) = InteractionType.VIBRATE, isRightHand: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true, dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = if (isRightHand) &quot;right&quot; else &quot;left&quot;, sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt; = listOf(GYROSCOPE, ACCELEROMETER))




