
[App-Support](../../app-support.html) > [healthstack.app](index.html)



# Package healthstack.app



## Types


| Name | Summary |
|---|---|
| [EducationView](-education-view/index.html) | [androidJvm]<br>class [EducationView](-education-view/index.html)(val changeNavigation: ([AppStage](../healthstack.app.pref/-app-stage/index.html)) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), publications: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;Publication&gt;) |
| [HomeScreenState](-home-screen-state/index.html) | [androidJvm]<br>enum [HomeScreenState](-home-screen-state/index.html) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[HomeScreenState](-home-screen-state/index.html)&gt; <br>Enum class representing the possible states of the home screen. |


## Functions


| Name | Summary |
|---|---|
| [BaseApplication](-base-application.html) | [androidJvm]<br>@Composable<br>fun [BaseApplication](-base-application.html)(onboardingTask: OnboardingTask, singUpTask: SignUpTask, statusList: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, healthDataSyncSpecs: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SyncManager.HealthDataSyncSpec](../healthstack.app.sync/-sync-manager/-health-data-sync-spec/index.html)&gt;)<br>Composable function representing the entire application. |
| [HealthStatusCard](-health-status-card.html) | [androidJvm]<br>@Composable<br>fun [HealthStatusCard](-health-status-card.html)(data: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[HealthStatus](../healthstack.app.status/-health-status/index.html)&gt;) |
| [Home](-home.html) | [androidJvm]<br>@Composable<br>fun [Home](-home.html)(dataTypeStatus: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html), changeNavigation: ([AppStage](../healthstack.app.pref/-app-stage/index.html)) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))<br>A composable function representing the entire application. |
| [HomeTaskCard](-home-task-card.html) | [androidJvm]<br>@Composable<br>fun [HomeTaskCard](-home-task-card.html)(title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), state: [TaskViewModel.TasksState](../healthstack.app.viewmodel/-task-view-model/-tasks-state/index.html), onReload: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { }, onStartTask: (Task) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { })<br>A composable function that displays a card view for a list of tasks. |
| [StatusCards](-status-cards.html) | [androidJvm]<br>@Composable<br>fun [StatusCards](-status-cards.html)(dataTypeStatus: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html)) |
| [TaskStatusCard](-task-status-card.html) | [androidJvm]<br>@Composable<br>fun [TaskStatusCard](-task-status-card.html)(dataType: [StatusDataType](../healthstack.app.status/-status-data-type/index.html), viewModel: [TaskViewModel](../healthstack.app.viewmodel/-task-view-model/index.html)) |

