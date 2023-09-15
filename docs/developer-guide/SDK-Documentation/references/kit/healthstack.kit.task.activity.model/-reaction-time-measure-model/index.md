
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [ReactionTimeMeasureModel](index.html)



# ReactionTimeMeasureModel



[androidJvm]\
class [ReactionTimeMeasureModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, val goal: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;square&quot;, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [ReactionTimeMeasureModel](-reaction-time-measure-model.html) | [androidJvm]<br>fun [ReactionTimeMeasureModel](-reaction-time-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Reaction Time&quot;, goal: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;square&quot;, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null) |


## Types


| Name | Summary |
|---|---|
| [SensorDataManager](-sensor-data-manager/index.html) | [androidJvm]<br>class [SensorDataManager](-sensor-data-manager/index.html) : [SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener.html) |
| [TestShape](-test-shape/index.html) | [androidJvm]<br>enum [TestShape](-test-shape/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[ReactionTimeMeasureModel.TestShape](-test-shape/index.html)&gt; |


## Functions


| Name | Summary |
|---|---|
| [close](close.html) | [androidJvm]<br>fun [close](close.html)() |
| [getData](get-data.html) | [androidJvm]<br>fun [getData](get-data.html)(): Flow&lt;[Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)&gt; |
| [init](init.html) | [androidJvm]<br>fun [init](init.html)() |
| [isGoal](is-goal.html) | [androidJvm]<br>fun [isGoal](is-goal.html)(shape: [ReactionTimeMeasureModel.TestShape](-test-shape/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |


## Properties


| Name | Summary |
|---|---|
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [goal](goal.html) | [androidJvm]<br>val [goal](goal.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

