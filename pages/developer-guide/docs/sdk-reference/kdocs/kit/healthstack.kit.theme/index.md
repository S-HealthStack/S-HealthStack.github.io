---



title: healthstack.kit.theme
permalink: /kit/healthstack.kit.theme/index.html



sidebar: dev_doc_sidebar


---



//[kit](/kit.html)/[healthstack.kit.theme](index.html)



# Package healthstack.kit.theme



## Types


| Name | Summary |
|---|---|
| [AppColors](-app-colors/index.html) | [androidJvm]<br>class [AppColors](-app-colors/index.html)(primary: Color, primaryVariant: Color, background: Color, surface: Color, onPrimary: Color, onBackground: Color, onSurface: Color, onSurfaceVariant: Color, error: Color, errorVariant: Color, onError: Color, disabled: Color, onDisabled: Color, disabled2: Color, onDisabled2: Color, dataVisualization1: Color, dataVisualization1Variant: Color, dataVisualization2: Color, dataVisualization2Variant: Color, dataVisualization3: Color, dataVisualization3Variant: Color, dataVisualization4: Color, dataVisualization4Variant: Color, dataVisualization5: Color, dataVisualization5Variant: Color, success: Color, successVariant: Color, warning: Color, warningVariant: Color, isLight: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [AppTheme](-app-theme/index.html) | [androidJvm]<br>object [AppTheme](-app-theme/index.html) |
| [AppTypography](-app-typography/index.html) | [androidJvm]<br>data class [AppTypography](-app-typography/index.html)(val headline1: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 40.sp,         lineHeight = 52.sp     ), val headline2: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 32.sp,         lineHeight = 41.6.sp     ), val headline3: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 20.sp,         lineHeight = 26.sp     ), val headline4: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 16.sp,         lineHeight = 20.8.sp     ), val title1: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 18.sp,         lineHeight = 23.4.sp     ), val title2: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 16.sp,         lineHeight = 20.8.sp     ), val title3: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 14.sp,         lineHeight = 18.2.sp     ), val subtitle1: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 18.sp,         lineHeight = 23.4.sp     ), val subtitle2: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 16.sp,         lineHeight = 20.8.sp     ), val subtitle3: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 14.sp,         lineHeight = 18.2.sp     ), val body1: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 16.sp,         lineHeight = 20.8.sp     ), val body2: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 14.sp,         lineHeight = 18.2.sp     ), val body3: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 12.sp,         lineHeight = 15.6.sp     ), val caption: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 12.sp,         lineHeight = 15.6.sp     ), val overline1: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W400,         fontSize = 10.sp,         lineHeight = 13.sp     ), val overline2: TextStyle = TextStyle(         fontFamily = Inter,         fontWeight = FontWeight.W600,         fontSize = 10.sp,         lineHeight = 13.sp     )) |


## Functions


| Name | Summary |
|---|---|
| [AppTheme](-app-theme.html) | [androidJvm]<br>@Composable<br>fun [AppTheme](-app-theme.html)(colors: [AppColors](-app-colors/index.html) = AppTheme.colors, typography: [AppTypography](-app-typography/index.html) = AppTheme.typography, shapes: Shapes = MaterialTheme.shapes, content: @Composable() -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)) |
| [mainLightColors](main-light-colors.html) | [androidJvm]<br>fun [mainLightColors](main-light-colors.html)(primary: Color = Color(0xFF4475E3), primaryVariant: Color = Color(0xFFDAE3F9), background: Color = Color(0xFFFBFBFB), surface: Color = Color(0xFFFFFFFF), onPrimary: Color = Color(0xFFFFFFFF), onBackground: Color = Color(0xFF000000), onSurface: Color = Color(0xFF000000), onSurfaceVariant: Color = Color(0xFF4475E3), error: Color = Color(0xFFFF3333), errorVariant: Color = Color(0xFFD14343), onError: Color = Color(0xFFFFFFFF), disabled: Color = Color(0xFFD7D7D7), onDisabled: Color = Color(0xFFFFFFFF), disabled2: Color = Color(0xFFF8F8F8), onDisabled2: Color = Color(0xFF9A9A9A), dataVisualization1: Color = Color(0xFF944ED7), dataVisualization1Variant: Color = Color(0xFF751EC7), dataVisualization2: Color = Color(0xFFF39C18), dataVisualization2Variant: Color = Color(0xFFC17A0D), dataVisualization3: Color = Color(0xFF00B0D7), dataVisualization3Variant: Color = Color(0xFF0D7491), dataVisualization4: Color = Color(0xFF1AD598), dataVisualization4Variant: Color = Color(0xFF00A670), dataVisualization5: Color = Color(0xFFFA5F4F), dataVisualization5Variant: Color = Color(0xFFCC4E40), success: Color = Color(0xFF2DC008), successVariant: Color = Color(0xFF00825D), warning: Color = Color(0xFFF5BF00), warningVariant: Color = Color(0xFFA36400), isLight: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true): [AppColors](-app-colors/index.html) |


## Properties


| Name | Summary |
|---|---|
| [Inter](-inter.html) | [androidJvm]<br>val [Inter](-inter.html): FontFamily |
| [OpenSans](-open-sans.html) | [androidJvm]<br>val [OpenSans](-open-sans.html): FontFamily |



