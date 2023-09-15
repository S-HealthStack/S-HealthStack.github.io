
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [ItemProperties](index.html)



# ItemProperties



[androidJvm]\
open class [ItemProperties](index.html)(val tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;?)

System distinguishes the UI component based on the tag.



## Constructors


| | |
|---|---|
| [ItemProperties](-item-properties.html) | [androidJvm]<br>fun [ItemProperties](-item-properties.html)(tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;?) |


## Properties


| Name | Summary |
|---|---|
| [skipLogic](skip-logic.html) | [androidJvm]<br>@SerializedName(value = &quot;skip_logic&quot;)<br>val [skipLogic](skip-logic.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? |
| [tag](tag.html) | [androidJvm]<br>val [tag](tag.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of UI component to render. (ex) Radio, Dropdown |


## Inheritors


| Name |
|---|
| [TextProperties](../-text-properties/index.html) |
| [ChoiceProperties](../-choice-properties/index.html) |
| [RankingProperties](../-ranking-properties/index.html) |
| [DateTimeProperties](../-date-time-properties/index.html) |
| [ScaleProperties](../-scale-properties/index.html) |

