
[Kit](../../../kit.html) > [healthstack.kit.auth](../index.html) > [FirebaseGoogleAuthContract](index.html)



# FirebaseGoogleAuthContract



[androidJvm]\
class [FirebaseGoogleAuthContract](index.html)(authCallback: [AuthCallback](../-auth-callback/index.html)) : [ActivityResultContract](https://developer.android.com/reference/kotlin/androidx/activity/result/contract/ActivityResultContract.html)&lt;[Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), FirebaseUser?&gt;



## Constructors


| | |
|---|---|
| [FirebaseGoogleAuthContract](-firebase-google-auth-contract.html) | [androidJvm]<br>fun [FirebaseGoogleAuthContract](-firebase-google-auth-contract.html)(authCallback: [AuthCallback](../-auth-callback/index.html)) |


## Functions


| Name | Summary |
|---|---|
| [createIntent](create-intent.html) | [androidJvm]<br>open override fun [createIntent](create-intent.html)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), input: [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)): [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html) |
| [getSynchronousResult](index.html#-1622969577%2FFunctions%2F-106109196) | [androidJvm]<br>open fun [getSynchronousResult](index.html#-1622969577%2FFunctions%2F-106109196)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), input: [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)): [ActivityResultContract.SynchronousResult](https://developer.android.com/reference/kotlin/androidx/activity/result/contract/ActivityResultContract.SynchronousResult.html)&lt;FirebaseUser?&gt;? |
| [parseResult](parse-result.html) | [androidJvm]<br>open override fun [parseResult](parse-result.html)(resultCode: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), intent: [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html)?): FirebaseUser? |

