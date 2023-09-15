
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model.common](../index.html) > [SimpleTimerActivityModel](index.html)



# SimpleTimerActivityModel



[androidJvm]\
open class [SimpleTimerActivityModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null, val timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 10, val textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = PARAGRAPH, val interactionType: [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) = NOTHING, val autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, val dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt;) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [SimpleTimerActivityModel](-simple-timer-activity-model.html) | [androidJvm]<br>fun [SimpleTimerActivityModel](-simple-timer-activity-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null, timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 10, textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = PARAGRAPH, interactionType: [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) = NOTHING, autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt;) |


## Functions


| Name | Summary |
|---|---|
| [close](close.html) | [androidJvm]<br>fun [close](close.html)() |
| [init](init.html) | [androidJvm]<br>fun [init](init.html)() |


## Properties


| Name | Summary |
|---|---|
| [accelerometer](accelerometer.html) | [androidJvm]<br>val [accelerometer](accelerometer.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt;&gt;? |
| [autoFlip](auto-flip.html) | [androidJvm]<br>val [autoFlip](auto-flip.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false |
| [body](body.html) | [androidJvm]<br>val [body](body.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null |
| [dataPrefix](data-prefix.html) | [androidJvm]<br>val [dataPrefix](data-prefix.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [gyroscope](gyroscope.html) | [androidJvm]<br>val [gyroscope](gyroscope.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt;&gt;? |
| [header](header.html) | [androidJvm]<br>val [header](header.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [interactionType](interaction-type.html) | [androidJvm]<br>val [interactionType](interaction-type.html): [InteractionType](../../healthstack.kit.ui.util/-interaction-type/index.html) |
| [sensors](sensors.html) | [androidJvm]<br>val [sensors](sensors.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../../healthstack.kit.sensor/-sensor-type/index.html)&gt; |
| [textType](text-type.html) | [androidJvm]<br>val [textType](text-type.html): [TextType](../../healthstack.kit.ui/-text-type/index.html) |
| [timeMillis](time-millis.html) | [androidJvm]<br>val [timeMillis](time-millis.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)&gt; |
| [timeSeconds](time-seconds.html) | [androidJvm]<br>val [timeSeconds](time-seconds.html): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 10 |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |


## Inheritors


| Name |
|---|
| [GaitAndBalanceBMeasureModel](../../healthstack.kit.task.activity.model/-gait-and-balance-b-measure-model/index.html) |
| [RangeOfMotionMeasureModel](../../healthstack.kit.task.activity.model/-range-of-motion-measure-model/index.html) |

