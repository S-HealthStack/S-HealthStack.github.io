
[Interface](../../../index.html) > [healthstack.backend.integration.healthdata](../index.html) > [HealthDataSyncClient](index.html)



# HealthDataSyncClient



[androidJvm]\
interface [HealthDataSyncClient](index.html)

Interface for syncing data with backend.



## Functions


| Name | Summary |
|---|---|
| [sync](sync.html) | [androidJvm]<br>abstract suspend fun [sync](sync.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), healthData: HealthData)<br>Used to transmit the user's health data to the backend. Backend can distinguish users through id token. |


## Inheritors


| Name |
|---|
| [BackendFacade](../../healthstack.backend.integration/-backend-facade/index.html) |

