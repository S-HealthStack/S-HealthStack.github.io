
[Interface](../../../interface.html) > [healthstack.healthdata.link](../index.html) > [HealthDataLink](index.html) > [getHealthData](get-health-data.html)



# getHealthData



[androidJvm]\
abstract suspend fun [getHealthData](get-health-data.html)(startTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), endTime: [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html), healthDataTypeName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HealthData](../-health-data/index.html)



A method reading health data.



It reads health data generated between startTime and endTime.



#### Return



[HealthData](../-health-data/index.html)



## Parameters


androidJvm

| | |
|---|---|
| startTime | Start point of time range |
| endTime | End point of time range |
| healthDataTypeName | Type of health data to read. |




