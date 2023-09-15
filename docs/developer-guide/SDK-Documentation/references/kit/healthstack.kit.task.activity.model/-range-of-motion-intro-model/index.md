
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [RangeOfMotionIntroModel](index.html)



# RangeOfMotionIntroModel



[androidJvm]\
class [RangeOfMotionIntroModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(
        &quot;Place phone in your right hand.&quot;,
        &quot;Straighten your right arm and move it in a full circle for the given sec.&quot;,
        &quot;Then, place phone in your left hand.&quot;,
        &quot;Straighten your left arm and move it in a full circle for the given sec.&quot;,
    ), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.ic_activity_range_of_motion_right_arm, val buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = &quot;Begin&quot;, val textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER) : [SimpleViewActivityModel](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/index.html)



## Constructors


| | |
|---|---|
| [RangeOfMotionIntroModel](-range-of-motion-intro-model.html) | [androidJvm]<br>fun [RangeOfMotionIntroModel](-range-of-motion-intro-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Range of Motion&quot;, body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(         &quot;Place phone in your right hand.&quot;,         &quot;Straighten your right arm and move it in a full circle for the given sec.&quot;,         &quot;Then, place phone in your left hand.&quot;,         &quot;Straighten your left arm and move it in a full circle for the given sec.&quot;,     ), drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.ic_activity_range_of_motion_right_arm, buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = &quot;Begin&quot;, textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER) |


## Properties


| Name | Summary |
|---|---|
| [body](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/body.html) | [androidJvm]<br>val [body](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/body.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = null |
| [buttonText](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/button-text.html) | [androidJvm]<br>val [buttonText](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/button-text.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [header](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/header.html) | [androidJvm]<br>val [header](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/header.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [textType](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/text-type.html) | [androidJvm]<br>val [textType](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/text-type.html): [TextType](../../healthstack.kit.ui/-text-type/index.html) |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

