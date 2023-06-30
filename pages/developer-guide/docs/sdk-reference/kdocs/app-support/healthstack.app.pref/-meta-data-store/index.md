---



title: MetaDataStore
permalink: /app-support/healthstack.app.pref/-meta-data-store/index.html



sidebar: dev_doc_sidebar


---



//[app-support](/app-support.html)/[healthstack.app.pref](../index.html)/[MetaDataStore](index.html)



# MetaDataStore



[androidJvm]\
class [MetaDataStore](index.html)(val context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html))



## Constructors


| | |
|---|---|
| [MetaDataStore](-meta-data-store.html) | [androidJvm]<br>fun [MetaDataStore](-meta-data-store.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |


## Functions


| Name | Summary |
|---|---|
| [clearDataStore](clear-data-store.html) | [androidJvm]<br>suspend fun [clearDataStore](clear-data-store.html)() |
| [readChangesToken](read-changes-token.html) | [androidJvm]<br>suspend fun [readChangesToken](read-changes-token.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
| [saveChangesToken](save-changes-token.html) | [androidJvm]<br>suspend fun [saveChangesToken](save-changes-token.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), changesToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [context](context.html) | [androidJvm]<br>val [context](context.html): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) |



