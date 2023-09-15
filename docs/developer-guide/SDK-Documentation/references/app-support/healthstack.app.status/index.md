
[App-Support](../../index.html) > [healthstack.app.status](index.html)



# Package healthstack.app.status



## Types


| Name | Summary |
|---|---|
| [HealthStatus](-health-status/index.html) | [androidJvm]<br>abstract class [HealthStatus](-health-status/index.html) : [StatusDataType](-status-data-type/index.html) |
| [HeartRateStatus](-heart-rate-status/index.html) | [androidJvm]<br>object [HeartRateStatus](-heart-rate-status/index.html) : [SampleHealthDataStatus](-sample-health-data-status/index.html)<br>An object representing the status of heart rate. Inherits from SampleHealthDataStatus, which represents a type of health data for which status information can be retrieved using a single data point. |
| [SampleHealthDataStatus](-sample-health-data-status/index.html) | [androidJvm]<br>abstract class [SampleHealthDataStatus](-sample-health-data-status/index.html)(healthDataName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) : [HealthStatus](-health-status/index.html)<br>Returns the data key used to extract the heart rate status information. |
| [SleepSessionStatus](-sleep-session-status/index.html) | [androidJvm]<br>object [SleepSessionStatus](-sleep-session-status/index.html) : [HealthStatus](-health-status/index.html)<br>An object representing the status of sleep sessions. |
| [StatusDataType](-status-data-type/index.html) | [androidJvm]<br>abstract class [StatusDataType](-status-data-type/index.html)<br>An abstract class representing a type of health data for which status information can be retrieved. |
| [TaskStatus](-task-status/index.html) | [androidJvm]<br>object [TaskStatus](-task-status/index.html) : [StatusDataType](-status-data-type/index.html) |

