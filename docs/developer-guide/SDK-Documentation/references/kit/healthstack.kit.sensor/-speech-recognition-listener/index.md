
[Kit](../../../kit.html) > [healthstack.kit.sensor](../index.html) > [SpeechRecognitionListener](index.html)



# SpeechRecognitionListener



[androidJvm]\
class [SpeechRecognitionListener](index.html)(onResult: ([String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), onFinish: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), var currentAmplitude: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 0) : [RecognitionListener](https://developer.android.com/reference/kotlin/android/speech/RecognitionListener.html)



## Constructors


| | |
|---|---|
| [SpeechRecognitionListener](-speech-recognition-listener.html) | [androidJvm]<br>fun [SpeechRecognitionListener](-speech-recognition-listener.html)(onResult: ([String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), onFinish: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), currentAmplitude: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 0) |


## Functions


| Name | Summary |
|---|---|
| [onBeginningOfSpeech](on-beginning-of-speech.html) | [androidJvm]<br>open override fun [onBeginningOfSpeech](on-beginning-of-speech.html)() |
| [onBufferReceived](on-buffer-received.html) | [androidJvm]<br>open override fun [onBufferReceived](on-buffer-received.html)(p0: [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?) |
| [onEndOfSegmentedSession](index.html#-1753391848%2FFunctions%2F-106109196) | [androidJvm]<br>open fun [onEndOfSegmentedSession](index.html#-1753391848%2FFunctions%2F-106109196)() |
| [onEndOfSpeech](on-end-of-speech.html) | [androidJvm]<br>open override fun [onEndOfSpeech](on-end-of-speech.html)() |
| [onError](on-error.html) | [androidJvm]<br>open override fun [onError](on-error.html)(error: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |
| [onEvent](on-event.html) | [androidJvm]<br>open override fun [onEvent](on-event.html)(eventType: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), params: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)?) |
| [onPartialResults](on-partial-results.html) | [androidJvm]<br>open override fun [onPartialResults](on-partial-results.html)(partialResults: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)) |
| [onReadyForSpeech](on-ready-for-speech.html) | [androidJvm]<br>open override fun [onReadyForSpeech](on-ready-for-speech.html)(params: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)?) |
| [onResults](on-results.html) | [androidJvm]<br>open override fun [onResults](on-results.html)(results: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)) |
| [onRmsChanged](on-rms-changed.html) | [androidJvm]<br>open override fun [onRmsChanged](on-rms-changed.html)(rmsdB: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)) |
| [onSegmentResults](index.html#1190892620%2FFunctions%2F-106109196) | [androidJvm]<br>open fun [onSegmentResults](index.html#1190892620%2FFunctions%2F-106109196)(p0: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)) |


## Properties


| Name | Summary |
|---|---|
| [currentAmplitude](current-amplitude.html) | [androidJvm]<br>var [currentAmplitude](current-amplitude.html): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = 0 |

