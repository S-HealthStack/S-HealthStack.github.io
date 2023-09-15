
[Kit](../../../kit.html) > [healthstack.kit.task.onboarding.model](../index.html) > [EligibilityIntroModel](index.html)



# EligibilityIntroModel



[androidJvm]\
open class [EligibilityIntroModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val conditions: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[EligibilityIntroModel.EligibilityCondition](-eligibility-condition/index.html)&gt;, val viewType: [EligibilityIntroModel.ViewType](-view-type/index.html)) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [EligibilityIntroModel](-eligibility-intro-model.html) | [androidJvm]<br>fun [EligibilityIntroModel](-eligibility-intro-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, conditions: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[EligibilityIntroModel.EligibilityCondition](-eligibility-condition/index.html)&gt;, viewType: [EligibilityIntroModel.ViewType](-view-type/index.html)) |


## Types


| Name | Summary |
|---|---|
| [EligibilityCondition](-eligibility-condition/index.html) | [androidJvm]<br>data class [EligibilityCondition](-eligibility-condition/index.html)(val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val constraints: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;) |
| [ViewType](-view-type/index.html) | [androidJvm]<br>enum [ViewType](-view-type/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[EligibilityIntroModel.ViewType](-view-type/index.html)&gt; |


## Properties


| Name | Summary |
|---|---|
| [conditions](conditions.html) | [androidJvm]<br>val [conditions](conditions.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[EligibilityIntroModel.EligibilityCondition](-eligibility-condition/index.html)&gt; |
| [description](description.html) | [androidJvm]<br>val [description](description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |
| [viewType](view-type.html) | [androidJvm]<br>val [viewType](view-type.html): [EligibilityIntroModel.ViewType](-view-type/index.html) |

