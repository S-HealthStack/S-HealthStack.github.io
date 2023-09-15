
[Kit](../../../kit.html) > [healthstack.kit.info.publication](../index.html) > [VideoPublication](index.html)



# VideoPublication



[androidJvm]\
class [VideoPublication](index.html)(val coverContent: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, val category: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), val contents: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt;) : [Publication](../-publication/index.html)



## Constructors


| | |
|---|---|
| [VideoPublication](-video-publication.html) | [androidJvm]<br>fun [VideoPublication](-video-publication.html)(coverContent: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?, category: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), contents: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt;) |


## Functions


| Name | Summary |
|---|---|
| [CardView](../-publication/-card-view.html) | [androidJvm]<br>@Composable<br>fun [CardView](../-publication/-card-view.html)(onClick: ([Publication](../-publication/index.html)?) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |
| [CustomControls](-custom-controls.html) | [androidJvm]<br>@Composable<br>fun [CustomControls](-custom-controls.html)(modifier: Modifier = Modifier, isVisible: () -&gt; [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), isPlaying: () -&gt; [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), onPauseToggle: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), isMute: () -&gt; [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), onMuteToggle: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html), totalDuration: () -&gt; [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), currentTime: () -&gt; [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), bufferedPercentage: () -&gt; [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), onSeekChanged: (timeMs: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |
| [PreviewImage](-preview-image.html) | [androidJvm]<br>@Composable<br>open override fun [PreviewImage](-preview-image.html)() |
| [RelatedContent](../-publication/-related-content.html) | [androidJvm]<br>@Composable<br>fun [RelatedContent](../-publication/-related-content.html)() |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)(onClick: ([Publication](../-publication/index.html)?) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |
| [VideoPlayer](-video-player.html) | [androidJvm]<br>@Composable<br>fun [VideoPlayer](-video-player.html)(modifier: Modifier = Modifier, uri: [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html), lifecycle: [Lifecycle.Event](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.Event.html)) |


## Properties


| Name | Summary |
|---|---|
| [category](../-publication/category.html) | [androidJvm]<br>val [category](../-publication/category.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [contents](../-publication/contents.html) | [androidJvm]<br>val [contents](../-publication/contents.html): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[ContentBlock](../../healthstack.kit.info.publication.content/-content-block/index.html)&gt; |
| [coverContent](../-publication/cover-content.html) | [androidJvm]<br>val [coverContent](../-publication/cover-content.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
| [description](../-publication/description.html) | [androidJvm]<br>val [description](../-publication/description.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [title](../-publication/title.html) | [androidJvm]<br>val [title](../-publication/title.html): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

