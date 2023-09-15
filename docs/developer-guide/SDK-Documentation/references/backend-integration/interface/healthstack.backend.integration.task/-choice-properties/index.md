
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [ChoiceProperties](index.html)



# ChoiceProperties



[androidJvm]\
class [ChoiceProperties](index.html)(val tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, val options: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Option](../-option/index.html)&gt;) : [ItemProperties](../-item-properties/index.html)

Item properties for the choice question.



## Parameters


androidJvm

| | |
|---|---|
| tag | Type of UI component to render. (ex) Radio, Dropdown |



## Constructors


| | |
|---|---|
| [ChoiceProperties](-choice-properties.html) | [androidJvm]<br>fun [ChoiceProperties](-choice-properties.html)(tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, options: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Option](../-option/index.html)&gt;) |


## Properties


| Name | Summary |
|---|---|
| [options](options.html) | [androidJvm]<br>val [options](options.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Option](../-option/index.html)&gt;<br>Values given as options. [Option](../-option/index.html) |
| [skipLogic](../-item-properties/skip-logic.html) | [androidJvm]<br>@SerializedName(value = &quot;skip_logic&quot;)<br>val [skipLogic](../-item-properties/skip-logic.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? |
| [tag](../-item-properties/tag.html) | [androidJvm]<br>val [tag](../-item-properties/tag.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of UI component to render. (ex) Radio, Dropdown |

