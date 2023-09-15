
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [ReactionTimeIntroModel](index.html) > [ReactionTimeIntroModel](-reaction-time-intro-model.html)



# ReactionTimeIntroModel



[androidJvm]\
fun [ReactionTimeIntroModel](-reaction-time-intro-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, goal: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;square&quot;, header: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, body: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;? = listOf(
        &quot;Hold phone in your right hand.&quot;,
        &quot;As soon as you see a \&quot;${goal}\&quot; appear, shake phone.&quot;,
        &quot;If you do not shake phone within 3 seconds of the ${goal}\'s appearing,&quot; +
            &quot; you will need to try again.&quot;
    ), drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.ic_activity_reaction_time, buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = &quot;Begin&quot;, textType: [TextType](../../healthstack.kit.ui/-text-type/index.html) = TextType.NUMBER)




