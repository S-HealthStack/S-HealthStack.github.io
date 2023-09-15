
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [SustainedPhonationMeasureModel](index.html)



# SustainedPhonationMeasureModel



[androidJvm]\
class [SustainedPhonationMeasureModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Sustained Phonation&quot;, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val noiseThreshold: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3000, inhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, exhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, val recorder: [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) = AudioRecorder) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [SustainedPhonationMeasureModel](-sustained-phonation-measure-model.html) | [androidJvm]<br>fun [SustainedPhonationMeasureModel](-sustained-phonation-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Sustained Phonation&quot;, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, noiseThreshold: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3000, inhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, exhaleSecond: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 5, recorder: [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) = AudioRecorder) |


## Types


| Name | Summary |
|---|---|
| [BreathingState](-breathing-state/index.html) | [androidJvm]<br>enum [BreathingState](-breathing-state/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[SustainedPhonationMeasureModel.BreathingState](-breathing-state/index.html)&gt; |


## Functions


| Name | Summary |
|---|---|
| [delete](delete.html) | [androidJvm]<br>fun [delete](delete.html)() |
| [getAmplitudes](get-amplitudes.html) | [androidJvm]<br>fun [getAmplitudes](get-amplitudes.html)(): Flow&lt;[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)&gt; |
| [start](start.html) | [androidJvm]<br>fun [start](start.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |
| [stop](stop.html) | [androidJvm]<br>fun [stop](stop.html)() |


## Properties


| Name | Summary |
|---|---|
| [cycleAnim](cycle-anim.html) | [androidJvm]<br>val [cycleAnim](cycle-anim.html): TweenSpec&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt; |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [exhaleAnim](exhale-anim.html) | [androidJvm]<br>val [exhaleAnim](exhale-anim.html): TweenSpec&lt;Dp&gt; |
| [filePath](file-path.html) | [androidJvm]<br>var [filePath](file-path.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [inhaleAnim](inhale-anim.html) | [androidJvm]<br>val [inhaleAnim](inhale-anim.html): TweenSpec&lt;Dp&gt; |
| [noiseThreshold](noise-threshold.html) | [androidJvm]<br>val [noiseThreshold](noise-threshold.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3000 |
| [recorder](recorder.html) | [androidJvm]<br>val [recorder](recorder.html): [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) |
| [startAnim](start-anim.html) | [androidJvm]<br>val [startAnim](start-anim.html): TweenSpec&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt; |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

