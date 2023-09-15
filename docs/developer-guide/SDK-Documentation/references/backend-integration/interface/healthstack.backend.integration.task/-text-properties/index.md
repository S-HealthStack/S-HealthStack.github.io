
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [TextProperties](index.html)



# TextProperties



[androidJvm]\
class [TextProperties](index.html)(val tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null) : [ItemProperties](../-item-properties/index.html)

System distinguishes the UI component based on the tag.



## Constructors


| | |
|---|---|
| [TextProperties](-text-properties.html) | [androidJvm]<br>fun [TextProperties](-text-properties.html)(tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null) |


## Properties


| Name | Summary |
|---|---|
| [skipLogic](../-item-properties/skip-logic.html) | [androidJvm]<br>@SerializedName(value = &quot;skip_logic&quot;)<br>val [skipLogic](../-item-properties/skip-logic.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? |
| [tag](../-item-properties/tag.html) | [androidJvm]<br>val [tag](../-item-properties/tag.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of UI component to render. (ex) Radio, Dropdown |

