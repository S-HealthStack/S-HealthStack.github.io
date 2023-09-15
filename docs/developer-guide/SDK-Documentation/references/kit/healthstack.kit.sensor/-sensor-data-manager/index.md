
[Kit](../../../kit.html) > [healthstack.kit.sensor](../index.html) > [SensorDataManager](index.html)



# SensorDataManager



[androidJvm]\
class [SensorDataManager](index.html)(sensorTypes: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../-sensor-type/index.html)&gt;) : [SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener.html)



## Constructors


| | |
|---|---|
| [SensorDataManager](-sensor-data-manager.html) | [androidJvm]<br>fun [SensorDataManager](-sensor-data-manager.html)(sensorTypes: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SensorType](../-sensor-type/index.html)&gt;) |


## Functions


| Name | Summary |
|---|---|
| [close](close.html) | [androidJvm]<br>fun [close](close.html)() |
| [init](init.html) | [androidJvm]<br>fun [init](init.html)() |
| [onAccuracyChanged](on-accuracy-changed.html) | [androidJvm]<br>open override fun [onAccuracyChanged](on-accuracy-changed.html)(sensor: [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor.html)?, accuracy: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |
| [onSensorChanged](on-sensor-changed.html) | [androidJvm]<br>open override fun [onSensorChanged](on-sensor-changed.html)(event: [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent.html)) |


## Properties


| Name | Summary |
|---|---|
| [ret](ret.html) | [androidJvm]<br>var [ret](ret.html): [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)&gt;&gt;&gt; |
| [times](times.html) | [androidJvm]<br>var [times](times.html): [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)&lt;[Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)&gt; |

