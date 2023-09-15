
[Interface](../../../interface.html) > [healthstack.healthdata.link](../index.html) > [HealthData](index.html)



# HealthData



[androidJvm]\
data class [HealthData](index.html)(val type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val data: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;&gt;)

Transfer object created to transmit health data according to Backend API Spec.



## Constructors


| | |
|---|---|
| [HealthData](-health-data.html) | [androidJvm]<br>fun [HealthData](-health-data.html)(type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), data: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;&gt;) |


## Types


| Name | Summary |
|---|---|
| [Companion](-companion/index.html) | [androidJvm]<br>object [Companion](-companion/index.html) |


## Properties


| Name | Summary |
|---|---|
| [data](data.html) | [androidJvm]<br>val [data](data.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;&gt;<br>List of actual data collected. |
| [type](type.html) | [androidJvm]<br>val [type](type.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Type of health data. (ex) BloodPressure, HeartRate, SleepSession |

