---
title: MobileSpirometryActivityTask
permalink: /kit/healthstack.kit.task.activity.predefined/-mobile-spirometry-activity-task/-mobile-spirometry-activity-task.html

sidebar: dev_doc_sidebar
---
//[kit](../../../kit.html)/[healthstack.kit.task.activity.predefined](../index.html)/[MobileSpirometryActivityTask](index.html)/[MobileSpirometryActivityTask](-mobile-spirometry-activity-task.html)



# MobileSpirometryActivityTask



[androidJvm]\
fun [MobileSpirometryActivityTask](-mobile-spirometry-activity-task.html)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), taskId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), name: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), description: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionTitle: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), completionDescription: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)&gt;?, steps: [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)&lt;[Step](../../healthstack.kit.task.base/-step/index.html)&lt;out [StepModel](../../healthstack.kit.task.base/-step-model/index.html), *&gt;&gt; = listOf(
        SimpleAudioActivityStep(
            id, name, MobileSpirometryIntroModel(id, name)
        ),
        MobileSpirometryMeasureStep(
            id, name, MobileSpirometryMeasureModel(id, name)
        ),
        SimpleViewActivityStep(
            id, name, MobileSpirometryResultModel(id, name, header = completionTitle, body = completionDescription)
        ),
    ), isCompleted: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = false, isActive: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) = true)




