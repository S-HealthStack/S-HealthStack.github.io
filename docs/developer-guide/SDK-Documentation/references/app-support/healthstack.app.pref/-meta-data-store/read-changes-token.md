
[App-Support](../../../index.html) > [healthstack.app.pref](../index.html) > [MetaDataStore](index.html) > [readChangesToken](read-changes-token.html)



# readChangesToken



[androidJvm]\
suspend fun [readChangesToken](read-changes-token.html)(healthDataTypeString: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?



Retrieves the changes token for the specified [healthDataTypeString](read-changes-token.html) from the metaDataStore.



#### Return



The changes token, or null if it is not present in the metaDataStore.



## Parameters


androidJvm

| | |
|---|---|
| healthDataTypeString | The name of the health data type for which to retrieve the changes token. |




