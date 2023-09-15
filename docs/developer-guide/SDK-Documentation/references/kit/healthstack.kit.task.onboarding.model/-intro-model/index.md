
[Kit](../../../kit.html) > [healthstack.kit.task.onboarding.model](../index.html) > [IntroModel](index.html)



# IntroModel



[androidJvm]\
open class [IntroModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.sample_image_alpha4, val logoDrawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val summaries: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)&lt;[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;&gt;? = null, val sections: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[IntroModel.IntroSection](-intro-section/index.html)&gt;) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [IntroModel](-intro-model.html) | [androidJvm]<br>fun [IntroModel](-intro-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = R.drawable.sample_image_alpha4, logoDrawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, summaries: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)&lt;[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;&gt;? = null, sections: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[IntroModel.IntroSection](-intro-section/index.html)&gt;) |


## Types


| Name | Summary |
|---|---|
| [IntroSection](-intro-section/index.html) | [androidJvm]<br>data class [IntroSection](-intro-section/index.html)(val subTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [logoDrawableId](logo-drawable-id.html) | [androidJvm]<br>val [logoDrawableId](logo-drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null |
| [sections](sections.html) | [androidJvm]<br>val [sections](sections.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[IntroModel.IntroSection](-intro-section/index.html)&gt; |
| [summaries](summaries.html) | [androidJvm]<br>val [summaries](summaries.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)&lt;[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;&gt;? = null |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

