
[Kit](../../kit.html) > [healthstack.kit.ui](index.html) > [HyperLinkText](-hyper-link-text.html)



# HyperLinkText



[androidJvm]\




@Composable



fun [HyperLinkText](-hyper-link-text.html)(text: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), meta: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), action: [HyperLinkAction](-hyper-link-action/index.html) = WEB)



When clicked, it performs a specific action.



## Parameters


androidJvm

| | |
|---|---|
| text | a text to display |
| meta | property that needs to perform an action     if the action is WEB, the meta is url.     if the action is DIAL, the meta is phone number.     if the action is EMAIL, the meta is receiver's email address. |
| action | one of WEB / DIAL / EMAIL |




