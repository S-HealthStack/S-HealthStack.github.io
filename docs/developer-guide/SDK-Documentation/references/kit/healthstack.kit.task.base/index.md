
[Kit](../../kit.html) > [healthstack.kit.task.base](index.html)



# Package healthstack.kit.task.base



## Types


| Name | Summary |
|---|---|
| [CallbackCollection](-callback-collection/index.html) | [androidJvm]<br>open class [CallbackCollection](-callback-collection/index.html)<br>A object holding callback functions. |
| [ImageArticleModel](-image-article-model/index.html) | [androidJvm]<br>class [ImageArticleModel](-image-article-model/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?) : [StepModel](-step-model/index.html)<br>A [StepModel](-step-model/index.html) with image. |
| [OrderedTask](-ordered-task/index.html) | [androidJvm]<br>open class [OrderedTask](-ordered-task/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](-step/index.html)&lt;out [StepModel](-step-model/index.html), *&gt;&gt;) : [Task](-task/index.html)<br>[Task](-task/index.html) with multiple [Step](-step/index.html)s OnboardingTask is an example of OrderedTask |
| [Step](-step/index.html) | [androidJvm]<br>abstract class [Step](-step/index.html)&lt;[T](-step/index.html) : [StepModel](-step-model/index.html), [R](-step/index.html)&gt;(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val model: [T](-step/index.html), val view: [View](-view/index.html)&lt;[T](-step/index.html)&gt;, getResult: () -&gt; [R](-step/index.html))<br>An object representing an action(=a single page) such as Intro page. |
| [StepModel](-step-model/index.html) | [androidJvm]<br>abstract class [StepModel](-step-model/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val drawableId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)?)<br>A data object for [Step](-step/index.html). |
| [Task](-task/index.html) | [androidJvm]<br>abstract class [Task](-task/index.html)(val id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))<br>An object representing a flow of actions(= a list of pages) such as survey flow or onBoarding flow. |
| [View](-view/index.html) | [androidJvm]<br>abstract class [View](-view/index.html)&lt;[T](-view/index.html) : [StepModel](-step-model/index.html)&gt;<br>A UI rendering object for [Step](-step/index.html). |

