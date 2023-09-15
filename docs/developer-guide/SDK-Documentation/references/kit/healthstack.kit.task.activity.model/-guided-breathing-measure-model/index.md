
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [GuidedBreathingMeasureModel](index.html)



# GuidedBreathingMeasureModel



[androidJvm]\
class [GuidedBreathingMeasureModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Guided Breathing&quot;, val numCycle: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3, inhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, exhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [GuidedBreathingMeasureModel](-guided-breathing-measure-model.html) | [androidJvm]<br>fun [GuidedBreathingMeasureModel](-guided-breathing-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Guided Breathing&quot;, numCycle: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3, inhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, exhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5) |


## Types


| Name | Summary |
|---|---|
| [BreathingState](-breathing-state/index.html) | [androidJvm]<br>enum [BreathingState](-breathing-state/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[GuidedBreathingMeasureModel.BreathingState](-breathing-state/index.html)&gt; |


## Properties


| Name | Summary |
|---|---|
| [cycleAnim](cycle-anim.html) | [androidJvm]<br>val [cycleAnim](cycle-anim.html): TweenSpec&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt; |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [exhaleAnim](exhale-anim.html) | [androidJvm]<br>val [exhaleAnim](exhale-anim.html): TweenSpec&lt;Dp&gt; |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [inhaleAnim](inhale-anim.html) | [androidJvm]<br>val [inhaleAnim](inhale-anim.html): TweenSpec&lt;Dp&gt; |
| [numCycle](num-cycle.html) | [androidJvm]<br>val [numCycle](num-cycle.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3 |
| [startAnim](start-anim.html) | [androidJvm]<br>val [startAnim](start-anim.html): TweenSpec&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt; |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

