
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [DateTimeProperties](index.html)



# DateTimeProperties



[androidJvm]\
class [DateTimeProperties](index.html)(val tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, val isTime: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), val isDate: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), val isRange: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) : [ItemProperties](../-item-properties/index.html)

Item properties for the date/time question.



## Parameters


androidJvm

| | |
|---|---|
| isTime | if format of the answer is time |
| isDate | if format of the answer is date |
| isRange | if format of the answer is range |



## Constructors


| | |
|---|---|
| [DateTimeProperties](-date-time-properties.html) | [androidJvm]<br>fun [DateTimeProperties](-date-time-properties.html)(tag: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), skipLogic: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? = null, isTime: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), isDate: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), isRange: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [isDate](is-date.html) | [androidJvm]<br>val [isDate](is-date.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isRange](is-range.html) | [androidJvm]<br>val [isRange](is-range.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isTime](is-time.html) | [androidJvm]<br>val [isTime](is-time.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [skipLogic](../-item-properties/skip-logic.html) | [androidJvm]<br>@SerializedName(value = &quot;skip_logic&quot;)<br>val [skipLogic](../-item-properties/skip-logic.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SkipLogic](../-skip-logic/index.html)&gt;? |
| [tag](../-item-properties/tag.html) | [androidJvm]<br>val [tag](../-item-properties/tag.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of UI component to render. (ex) Radio, Dropdown |

