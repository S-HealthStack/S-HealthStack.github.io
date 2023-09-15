
[App-Support](../../app-support.html) > [healthstack.app](index.html) > [BaseApplication](-base-application.html)



# BaseApplication



[androidJvm]\




@Composable



fun [BaseApplication](-base-application.html)(onboardingTask: OnboardingTask, singUpTask: SignUpTask, statusList: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[StatusDataType](../healthstack.app.status/-status-data-type/index.html)&gt;, healthDataSyncSpecs: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[SyncManager.HealthDataSyncSpec](../healthstack.app.sync/-sync-manager/-health-data-sync-spec/index.html)&gt;)



Composable function representing the entire application.



## Parameters


androidJvm

| | |
|---|---|
| onboardingTask | the onboarding task to be performed when the app is launched. |
| singUpTask | the sign up task to be performed after the onboarding task is completed. |
| statusList | the list of status data types to be displayed in the UI. |
| healthDataSyncSpecs | the list of health data sync specifications to be used by the SyncManager. |




