
[App-Support](../../../index.html) > [healthstack.app.pref](../index.html) > [MetaDataStore](index.html)



# MetaDataStore



[androidJvm]\
class [MetaDataStore](index.html)(val context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html))

A class that provides access to the meta data stored in the metaDataStore.



## Constructors


| | |
|---|---|
| [MetaDataStore](-meta-data-store.html) | [androidJvm]<br>fun [MetaDataStore](-meta-data-store.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |


## Functions


| Name | Summary |
|---|---|
| [clearDataStore](clear-data-store.html) | [androidJvm]<br>suspend fun [clearDataStore](clear-data-store.html)()<br>Clears all data from the metaDataStore. |
| [readChangesToken](read-changes-token.html) | [androidJvm]<br>suspend fun [readChangesToken](read-changes-token.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?<br>Retrieves the changes token for the specified [healthDataTypeString](read-changes-token.html) from the metaDataStore. |
| [saveChangesToken](save-changes-token.html) | [androidJvm]<br>suspend fun [saveChangesToken](save-changes-token.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), changesToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))<br>Saves the changes token for the specified [healthDataTypeString](save-changes-token.html) to the metaDataStore. |


## Properties


| Name | Summary |
|---|---|
| [context](context.html) | [androidJvm]<br>val [context](context.html): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)<br>The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) used to access the metaDataStore. |

