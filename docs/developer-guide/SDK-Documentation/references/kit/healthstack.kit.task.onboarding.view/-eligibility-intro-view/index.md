
[Kit](../../../kit.html) > [healthstack.kit.task.onboarding.view](../index.html) > [EligibilityIntroView](index.html)



# EligibilityIntroView



[androidJvm]\
class [EligibilityIntroView](index.html) : [View](../../healthstack.kit.task.base/-view/index.html)&lt;[EligibilityIntroModel](../../healthstack.kit.task.onboarding.model/-eligibility-intro-model/index.html)&gt;



## Constructors


| | |
|---|---|
| [EligibilityIntroView](-eligibility-intro-view.html) | [androidJvm]<br>fun [EligibilityIntroView](-eligibility-intro-view.html)() |


## Functions


| Name | Summary |
|---|---|
| [EligibilityOverviewCard](-eligibility-overview-card.html) | [androidJvm]<br>@Composable<br>fun [EligibilityOverviewCard](-eligibility-overview-card.html)(onClick: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = {}, modifier: Modifier = Modifier, imageId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = R.drawable.card_sample_image_alpha, content: [EligibilityIntroModel.EligibilityCondition](../../healthstack.kit.task.onboarding.model/-eligibility-intro-model/-eligibility-condition/index.html), backgroundColor: Color = AppTheme.colors.background) |
| [EligibilityOverviewCards](-eligibility-overview-cards.html) | [androidJvm]<br>@Composable<br>fun [EligibilityOverviewCards](-eligibility-overview-cards.html)(modifier: Modifier = Modifier, pagerState: PagerState = rememberPagerState(), contents: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[EligibilityIntroModel.EligibilityCondition](../../healthstack.kit.task.onboarding.model/-eligibility-intro-model/-eligibility-condition/index.html)&gt;, contentPadding: PaddingValues = PaddingValues(horizontal = 50.dp), startScale: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) = 1.0f, startAlpha: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) = 1.0f, backgroundColor: Color = AppTheme.colors.background) |
| [OverviewTab](-overview-tab.html) | [androidJvm]<br>@Composable<br>fun [OverviewTab](-overview-tab.html)(modifier: Modifier = Modifier, unselectedTabIcon: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = R.drawable.tab_icon_unselected, selectedTabIcon: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = R.drawable.tab_icon_selected, conditions: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[EligibilityIntroModel.EligibilityCondition](../../healthstack.kit.task.onboarding.model/-eligibility-intro-model/-eligibility-condition/index.html)&gt;, contentPadding: PaddingValues = PaddingValues(horizontal = 50.dp), startScale: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) = 1.0f, startAlpha: [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) = 1.0f, backgroundColor: Color = AppTheme.colors.background) |
| [Render](-render.html) | [androidJvm]<br>@Composable<br>open override fun [Render](-render.html)(model: [EligibilityIntroModel](../../healthstack.kit.task.onboarding.model/-eligibility-intro-model/index.html), callbackCollection: [CallbackCollection](../../healthstack.kit.task.base/-callback-collection/index.html), holder: [SubStepHolder](../../healthstack.kit.task.survey.question/-sub-step-holder/index.html)?)<br>A method rendering UI. |

