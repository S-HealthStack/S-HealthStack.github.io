
[Kit](../../kit.html) > [healthstack.kit.task.activity.model.common](index.html)



# Package healthstack.kit.task.activity.model.common



## Types


| Name | Summary |
|---|---|
| [SimpleAudioActivityModel](-simple-audio-activity-model/index.html) | [androidJvm]<br>open class [SimpleAudioActivityModel](-simple-audio-activity-model/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val textType: [TextType](../healthstack.kit.ui/-text-type/index.html) = TextType.PARAGRAPH) : [StepModel](../healthstack.kit.task.base/-step-model/index.html) |
| [SimpleTimerActivityModel](-simple-timer-activity-model/index.html) | [androidJvm]<br>open class [SimpleTimerActivityModel](-simple-timer-activity-model/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null, val timeSeconds: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) = 10, val textType: [TextType](../healthstack.kit.ui/-text-type/index.html) = PARAGRAPH, val interactionType: [InteractionType](../healthstack.kit.ui.util/-interaction-type/index.html) = NOTHING, val autoFlip: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, val dataPrefix: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val sensors: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../healthstack.kit.sensor/-sensor-type/index.html)&gt;) : [StepModel](../healthstack.kit.task.base/-step-model/index.html) |
| [SimpleViewActivityModel](-simple-view-activity-model/index.html) | [androidJvm]<br>open class [SimpleViewActivityModel](-simple-view-activity-model/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val textType: [TextType](../healthstack.kit.ui/-text-type/index.html) = PARAGRAPH) : [StepModel](../healthstack.kit.task.base/-step-model/index.html) |

