
[Kit](../../../kit.html) > [healthstack.kit.datastore](../index.html) > [PreferenceDataStore](index.html)



# PreferenceDataStore



[androidJvm]\
class [PreferenceDataStore](index.html)(val context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html))



## Constructors


| | |
|---|---|
| [PreferenceDataStore](-preference-data-store.html) | [androidJvm]<br>fun [PreferenceDataStore](-preference-data-store.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |


## Types


| Name | Summary |
|---|---|
| [Companion](-companion/index.html) | [androidJvm]<br>object [Companion](-companion/index.html) |


## Functions


| Name | Summary |
|---|---|
| [setProfile](set-profile.html) | [androidJvm]<br>suspend fun [setProfile](set-profile.html)(profile: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |
| [setPush](set-push.html) | [androidJvm]<br>suspend fun [setPush](set-push.html)(push: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setReminder](set-reminder.html) | [androidJvm]<br>suspend fun [setReminder](set-reminder.html)(reminder: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [context](context.html) | [androidJvm]<br>val [context](context.html): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) |
| [profile](profile.html) | [androidJvm]<br>val [profile](profile.html): Flow&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |
| [push](push.html) | [androidJvm]<br>val [push](push.html): Flow&lt;[Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)&gt; |
| [reminder](reminder.html) | [androidJvm]<br>val [reminder](reminder.html): Flow&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt; |

