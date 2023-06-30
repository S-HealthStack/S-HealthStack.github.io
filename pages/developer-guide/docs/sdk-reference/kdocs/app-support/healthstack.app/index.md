---



title: healthstack.app
permalink: /app-support/healthstack.app/index.html



sidebar: dev_doc_sidebar


---



//[app-support](/app-support.html)/[healthstack.app](index.html)



# Package healthstack.app



## Functions


| Name | Summary |
|---|---|
| [BaseApplication](-base-application.html) | [androidJvm]<br>@Composable<br>fun [BaseApplication](-base-application.html)(onboardingTask: OnboardingTask, singUpTask: SignUpTask, statusList: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, healthDataSyncSpecs: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SyncManager.HealthDataSyncSpec](../healthstack.app.sync/-sync-manager/-health-data-sync-spec/index.html)&gt;) |
| [HealthStatusCard](-health-status-card.html) | [androidJvm]<br>@Composable<br>fun [HealthStatusCard](-health-status-card.html)(dataType: [StatusDataType](../healthstack.app.status/-status-data-type/index.html), vm: [HealthStatusViewModel](../healthstack.app.viewmodel/-health-status-view-model/index.html)) |
| [Home](-home.html) | [androidJvm]<br>@Composable<br>fun [Home](-home.html)(dataTypeStatus: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html)) |
| [StatusCards](-status-cards.html) | [androidJvm]<br>@Composable<br>fun [StatusCards](-status-cards.html)(dataTypeStatus: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html)) |
| [Tasks](-tasks.html) | [androidJvm]<br>@Composable<br>fun [Tasks](-tasks.html)(title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), state: [TaskViewModel.TasksState](../healthstack.app.viewmodel/-task-view-model/-tasks-state/index.html), onReload: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { }, onStartTask: (Task) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { }) |
| [TaskStatusCard](-task-status-card.html) | [androidJvm]<br>@Composable<br>fun [TaskStatusCard](-task-status-card.html)(dataType: [StatusDataType](../healthstack.app.status/-status-data-type/index.html), viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html)) |



