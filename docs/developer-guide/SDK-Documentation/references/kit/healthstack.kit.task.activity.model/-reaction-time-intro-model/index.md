
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [ReactionTimeIntroModel](index.html)



# ReactionTimeIntroModel



[androidJvm]\
class [ReactionTimeIntroModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, goal: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;square&quot;, val header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, val body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(
        &quot;Hold phone in your right hand.&quot;,
        &quot;As soon as you see a \&quot;${goal}\&quot; appear, shake phone.&quot;,
        &quot;If you do not shake phone within 3 seconds of the ${goal}\'s appearing,&quot; +
            &quot; you will need to try again.&quot;
    ), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.ic_activity_reaction_time, val buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = &quot;Begin&quot;, val textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER) : [SimpleViewActivityModel](../../healthstack.kit.task.activity.model.common/-simple-view-activity-model/index.html)



## Constructors


| | |
|---|---|
| [ReactionTimeIntroModel](-reaction-time-intro-model.html) | [androidJvm]<br>fun [ReactionTimeIntroModel](-reaction-time-intro-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, goal: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;square&quot;, header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(         &quot;Hold phone in your right hand.&quot;,         &quot;As soon as you see a \&quot;${goal}\&quot; appear, shake phone.&quot;,         &quot;If you do not shake phone within 3 seconds of the ${goal}\'s appearing,&quot; +             &quot; you will need to try again.&quot;     ), drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.ic_activity_reaction_time, buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = &quot;Begin&quot;, textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER) |


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

