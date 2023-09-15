
[Interface](../../../index.html) > [healthstack.backend.integration.task](../index.html) > [Contents](index.html)



# Contents



[androidJvm]\
data class [Contents](index.html)(val type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val required: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val itemProperties: [ItemProperties](../-item-properties/index.html)? = null, val completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, val completionDescription: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null)

Stores the information of the contents received from backend.



## Constructors


| | |
|---|---|
| [Contents](-contents.html) | [androidJvm]<br>fun [Contents](-contents.html)(type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), required: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, explanation: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, itemProperties: [ItemProperties](../-item-properties/index.html)? = null, completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null, completionDescription: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null) |


## Properties


| Name | Summary |
|---|---|
| [completionDescription](completion-description.html) | [androidJvm]<br>val [completionDescription](completion-description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null |
| [completionTitle](completion-title.html) | [androidJvm]<br>val [completionTitle](completion-title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null |
| [explanation](explanation.html) | [androidJvm]<br>val [explanation](explanation.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null<br>Explanation of the content. |
| [itemProperties](item-properties.html) | [androidJvm]<br>@SerializedName(value = &quot;properties&quot;)<br>val [itemProperties](item-properties.html): [ItemProperties](../-item-properties/index.html)? = null<br>Properties(tag) of the content. [ItemProperties](../-item-properties/index.html) |
| [required](required.html) | [androidJvm]<br>val [required](required.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>If item is required or not. |
| [title](title.html) | [androidJvm]<br>val [title](title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? = null<br>Title of the content. |
| [type](type.html) | [androidJvm]<br>val [type](type.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of the content. |

