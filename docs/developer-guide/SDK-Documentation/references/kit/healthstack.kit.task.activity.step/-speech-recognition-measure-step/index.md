
[Kit](../../../kit.html) > [healthstack.kit.task.activity.step](../index.html) > [SpeechRecognitionMeasureStep](index.html)



# SpeechRecognitionMeasureStep



[androidJvm]\
class [SpeechRecognitionMeasureStep](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html)&gt; = SpeechRecognitionMeasureView()) : [Step](../../healthstack.kit.task.base/-step/index.html)&lt;[SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html), [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)&gt;



## Constructors


| | |
|---|---|
| [SpeechRecognitionMeasureStep](-speech-recognition-measure-step.html) | [androidJvm]<br>fun [SpeechRecognitionMeasureStep](-speech-recognition-measure-step.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html)&gt; = SpeechRecognitionMeasureView()) |


## Functions


| Name | Summary |
|---|---|
| [getState](../../healthstack.kit.task.base/-step/get-state.html) | [androidJvm]<br>fun [getState](../../healthstack.kit.task.base/-step/get-state.html)(): [SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html)<br>A method for getting state of Step. |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)(callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html))<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [id](../../healthstack.kit.task.base/-step/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [model](../../healthstack.kit.task.base/-step/model.html) | [androidJvm]<br>val [model](../../healthstack.kit.task.base/-step/model.html): [SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html)<br>data object for UI & state management |
| [name](../../healthstack.kit.task.base/-step/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-step/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [result](../../healthstack.kit.task.base/-step/result.html) | [androidJvm]<br>var [result](../../healthstack.kit.task.base/-step/result.html): [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |
| [view](../../healthstack.kit.task.base/-step/view.html) | [androidJvm]<br>val [view](../../healthstack.kit.task.base/-step/view.html): [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SpeechRecognitionMeasureModel](../../healthstack.kit.task.activity.model/-speech-recognition-measure-model/index.html)&gt;<br>view object holding UI method |

