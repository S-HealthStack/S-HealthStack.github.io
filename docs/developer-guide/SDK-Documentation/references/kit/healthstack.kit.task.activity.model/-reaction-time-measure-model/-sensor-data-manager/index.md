
[Kit](../../../../kit.html) > [healthstack.kit.task.activity.model](../../index.html) > [ReactionTimeMeasureModel](../index.html) > [SensorDataManager](index.html)



# SensorDataManager



[androidJvm]\
class [SensorDataManager](index.html) : [SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener.html)



## Constructors


| | |
|---|---|
| [SensorDataManager](-sensor-data-manager.html) | [androidJvm]<br>fun [SensorDataManager](-sensor-data-manager.html)() |


## Functions


| Name | Summary |
|---|---|
| [cancel](cancel.html) | [androidJvm]<br>fun [cancel](cancel.html)() |
| [getData](get-data.html) | [androidJvm]<br>fun [getData](get-data.html)(): Flow&lt;[Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)&gt; |
| [init](init.html) | [androidJvm]<br>fun [init](init.html)() |
| [onAccuracyChanged](on-accuracy-changed.html) | [androidJvm]<br>open override fun [onAccuracyChanged](on-accuracy-changed.html)(sensor: [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor.html), accuracy: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |
| [onSensorChanged](on-sensor-changed.html) | [androidJvm]<br>open override fun [onSensorChanged](on-sensor-changed.html)(event: [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent.html)) |

