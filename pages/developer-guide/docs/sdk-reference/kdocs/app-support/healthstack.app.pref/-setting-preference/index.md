---



title: SettingPreference
permalink: /app-support/healthstack.app.pref/-setting-preference/index.html



sidebar: dev_doc_sidebar


---



//[app-support](/app-support.html)/[healthstack.app.pref](../index.html)/[SettingPreference](index.html)



# SettingPreference



[androidJvm]\
class [SettingPreference](index.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html))



## Constructors


| | |
|---|---|
| [SettingPreference](-setting-preference.html) | [androidJvm]<br>fun [SettingPreference](-setting-preference.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |


## Types


| Name | Summary |
|---|---|
| [Companion](-companion/index.html) | [androidJvm]<br>object [Companion](-companion/index.html) |


## Functions


| Name | Summary |
|---|---|
| [setAppStage](set-app-stage.html) | [androidJvm]<br>suspend fun [setAppStage](set-app-stage.html)(stage: [AppStage](../-app-stage/index.html)) |
| [setTaskSyncTime](set-task-sync-time.html) | [androidJvm]<br>suspend fun [setTaskSyncTime](set-task-sync-time.html)(taskSyncTime: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [appStage](app-stage.html) | [androidJvm]<br>val [appStage](app-stage.html): Flow&lt;[AppStage](../-app-stage/index.html)&gt; |
| [taskSyncTime](task-sync-time.html) | [androidJvm]<br>val [taskSyncTime](task-sync-time.html): Flow&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |



