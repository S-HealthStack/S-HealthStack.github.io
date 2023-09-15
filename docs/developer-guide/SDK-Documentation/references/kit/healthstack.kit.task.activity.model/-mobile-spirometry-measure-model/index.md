
[Kit](../../../kit.html) > [healthstack.kit.task.activity.model](../index.html) > [MobileSpirometryMeasureModel](index.html)



# MobileSpirometryMeasureModel



[androidJvm]\
class [MobileSpirometryMeasureModel](index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Mobile Spirometry&quot;, val count: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3, val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, val buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Stop Recording&quot;, val recorder: [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) = AudioRecorder) : [StepModel](../../healthstack.kit.task.base/-step-model/index.html)



## Constructors


| | |
|---|---|
| [MobileSpirometryMeasureModel](-mobile-spirometry-measure-model.html) | [androidJvm]<br>fun [MobileSpirometryMeasureModel](-mobile-spirometry-measure-model.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Mobile Spirometry&quot;, count: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3, drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)? = null, buttonText: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = &quot;Stop Recording&quot;, recorder: [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) = AudioRecorder) |


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
| [buttonText](button-text.html) | [androidJvm]<br>val [buttonText](button-text.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [count](count.html) | [androidJvm]<br>val [count](count.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 3 |
| [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html) | [androidJvm]<br>val [drawableId](../../healthstack.kit.task.base/-step-model/drawable-id.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?<br>a representative image for UI |
| [filePath](file-path.html) | [androidJvm]<br>var [filePath](file-path.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [id](../../healthstack.kit.task.base/-step-model/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step-model/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [recorder](recorder.html) | [androidJvm]<br>val [recorder](recorder.html): [AudioRecorder.Companion](../../healthstack.kit.sensor/-audio-recorder/-companion/index.html) |
| [title](../../healthstack.kit.task.base/-step-model/title.html) | [androidJvm]<br>val [title](../../healthstack.kit.task.base/-step-model/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>a title of UI |

