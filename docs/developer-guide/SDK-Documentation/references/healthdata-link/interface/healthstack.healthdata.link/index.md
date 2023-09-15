
[Interface](../../interface.html) > [healthstack.healthdata.link](index.html)



# Package healthstack.healthdata.link



## Types


| Name | Summary |
|---|---|
| [Change](-change/index.html) | [androidJvm]<br>class [Change](-change/index.html)(val healthData: [HealthData](-health-data/index.html), val token: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))<br>A data object representing Change. |
| [HealthData](-health-data/index.html) | [androidJvm]<br>data class [HealthData](-health-data/index.html)(val type: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val data: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;&gt;)<br>Transfer object created to transmit health data according to Backend API Spec. |
| [HealthDataLink](-health-data-link/index.html) | [androidJvm]<br>interface [HealthDataLink](-health-data-link/index.html)<br>An interface for handling health data. |
| [HealthDataLinkHolder](-health-data-link-holder/index.html) | [androidJvm]<br>object [HealthDataLinkHolder](-health-data-link-holder/index.html)<br>An object holding singleton instance of [HealthDataLink](-health-data-link/index.html) |

