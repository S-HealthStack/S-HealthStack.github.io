
[Kit](../../../kit.html) > [healthstack.kit.info.publication](../index.html) > [Publication](index.html)



# Publication



[androidJvm]\
abstract class [Publication](index.html)(val coverContent: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, val category: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val contents: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt;)



## Constructors


| | |
|---|---|
| [Publication](-publication.html) | [androidJvm]<br>fun [Publication](-publication.html)(coverContent: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, category: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), contents: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt;) |


## Functions


| Name | Summary |
|---|---|
| [CardView](-card-view.html) | [androidJvm]<br>@Composable<br>fun [CardView](-card-view.html)(onClick: ([Publication](index.html)?) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |
| [PreviewImage](-preview-image.html) | [androidJvm]<br>@Composable<br>abstract fun [PreviewImage](-preview-image.html)() |
| [RelatedContent](-related-content.html) | [androidJvm]<br>@Composable<br>fun [RelatedContent](-related-content.html)() |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>abstract fun [Render](-render.html)(onClick: ([Publication](index.html)?) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |


## Properties


| Name | Summary |
|---|---|
| [category](category.html) | [androidJvm]<br>val [category](category.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [contents](contents.html) | [androidJvm]<br>val [contents](contents.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt; |
| [coverContent](cover-content.html) | [androidJvm]<br>val [coverContent](cover-content.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
| [description](description.html) | [androidJvm]<br>val [description](description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [title](title.html) | [androidJvm]<br>val [title](title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |


## Inheritors


| Name |
|---|
| [PdfPublication](../-pdf-publication/index.html) |
| [TextPublication](../-text-publication/index.html) |
| [VideoPublication](../-video-publication/index.html) |

