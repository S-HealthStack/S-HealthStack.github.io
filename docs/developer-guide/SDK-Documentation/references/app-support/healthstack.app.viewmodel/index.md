
[App-Support](../../index.html) > [healthstack.app.viewmodel](index.html)



# Package healthstack.app.viewmodel



## Types


| Name | Summary |
|---|---|
| [HealthState](-health-state/index.html) | [androidJvm]<br>data class [HealthState](-health-state/index.html)(val state: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)) |
| [HealthStatusViewModel](-health-status-view-model/index.html) | [androidJvm]<br>abstract class [HealthStatusViewModel](-health-status-view-model/index.html)(healthStatus: [HealthStatus](../healthstack.app.status/-health-status/index.html), intervalTimeMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html) |
| [HeartRateStatusViewModel](-heart-rate-status-view-model/index.html) | [androidJvm]<br>object [HeartRateStatusViewModel](-heart-rate-status-view-model/index.html) : [HealthStatusViewModel](-health-status-view-model/index.html) |
| [SleepSessionStatusViewModel](-sleep-session-status-view-model/index.html) | [androidJvm]<br>object [SleepSessionStatusViewModel](-sleep-session-status-view-model/index.html) : [HealthStatusViewModel](-health-status-view-model/index.html) |
| [TaskViewModel](-task-view-model/index.html) | [androidJvm]<br>class [TaskViewModel](-task-view-model/index.html)(taskRepository: [TaskRepository](../healthstack.app.task.repository/-task-repository/index.html), settingPreference: [SettingPreference](../healthstack.app.pref/-setting-preference/index.html)) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html) |

