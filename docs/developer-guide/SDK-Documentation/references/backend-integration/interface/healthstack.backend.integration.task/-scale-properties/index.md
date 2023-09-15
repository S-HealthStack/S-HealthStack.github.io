
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [ScaleProperties](index.html)



# ScaleProperties



[androidJvm]\
class [ScaleProperties](index.html)(val tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, val low: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), val high: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), val lowLabel: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, val highLabel: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?) : [ItemProperties](../-item-properties/index.html)

Item properties for the scale question.



## Parameters


androidJvm

| | |
|---|---|
| tag | Type of UI component to render. (ex) Radio, Dropdown |



## Constructors


| | |
|---|---|
| [ScaleProperties](-scale-properties.html) | [androidJvm]<br>fun [ScaleProperties](-scale-properties.html)(tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, low: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), high: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), lowLabel: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, highLabel: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?) |


## Properties


| Name | Summary |
|---|---|
| [high](high.html) | [androidJvm]<br>val [high](high.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Maximum number in Scale. |
| [highLabel](high-label.html) | [androidJvm]<br>val [highLabel](high-label.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?<br>Label of maximum number in Scale. |
| [low](low.html) | [androidJvm]<br>val [low](low.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Minimum number in Scale. |
| [lowLabel](low-label.html) | [androidJvm]<br>val [lowLabel](low-label.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?<br>Label of minimum number in Scale. |
| [skipLogic](../-item-properties/skip-logic.html) | [androidJvm]<br>@SerializedName(value = &quot;skip_logic&quot;)<br>val [skipLogic](../-item-properties/skip-logic.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? |
| [tag](../-item-properties/tag.html) | [androidJvm]<br>val [tag](../-item-properties/tag.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of UI component to render. (ex) Radio, Dropdown |

