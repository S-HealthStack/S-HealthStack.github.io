
[Kit](../../../kit.html) > [healthstack.kit.task.signup.step](../index.html) > [SignUpStep](index.html)



# SignUpStep



[androidJvm]\
open class [SignUpStep](index.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html)&gt; = SignUpView()) : [Step](../../healthstack.kit.task.base/-step/index.html)&lt;[SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html), [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)&gt;



## Constructors


| | |
|---|---|
| [SignUpStep](-sign-up-step.html) | [androidJvm]<br>fun [SignUpStep](-sign-up-step.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), model: [SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html), view: [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html)&gt; = SignUpView()) |


## Functions


| Name | Summary |
|---|---|
| [getState](../../healthstack.kit.task.base/-step/get-state.html) | [androidJvm]<br>fun [getState](../../healthstack.kit.task.base/-step/get-state.html)(): [SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html)<br>A method for getting state of Step. |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)(callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html))<br>A method for rendering UI. |


## Properties


| Name | Summary |
|---|---|
| [id](../../healthstack.kit.task.base/-step/id.html) | [androidJvm]<br>val [id](../../healthstack.kit.task.base/-step/id.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>id |
| [model](../../healthstack.kit.task.base/-step/model.html) | [androidJvm]<br>val [model](../../healthstack.kit.task.base/-step/model.html): [SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html)<br>data object for UI & state management |
| [name](../../healthstack.kit.task.base/-step/name.html) | [androidJvm]<br>val [name](../../healthstack.kit.task.base/-step/name.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>name |
| [result](../../healthstack.kit.task.base/-step/result.html) | [androidJvm]<br>var [result](../../healthstack.kit.task.base/-step/result.html): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [view](../../healthstack.kit.task.base/-step/view.html) | [androidJvm]<br>val [view](../../healthstack.kit.task.base/-step/view.html): [View](../../healthstack.kit.task.base/-view/index.html)&lt;[SignUpModel](../../healthstack.kit.task.signup.model/-sign-up-model/index.html)&gt;<br>view object holding UI method |

