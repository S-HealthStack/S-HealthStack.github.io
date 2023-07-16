---
title: Configuring the Eligibility Survey
sidebar: doc_sidebar
permalink: create-eligibility-questions.html
toc: false
---

Part of onboarding participants is asking them questions to determine if they are appropriate participants for your study. 

# All Implementations

Creating eligibility questions is not implemented in the web portal, so you create eligibility questions for all implementations by editing the app code. This example shows editing the starter-app code. Adjust the questions to meet your needs.

   > 
   > In **starter-app/app/src/main/java/com/samsung/healthstack/starter_app/OnboardingModule.kt**:
   >
   > - In `private val eligibilityQuestions`, replace the third and fourth questions with a single Galaxy Watch question:
   > 
   >   ```diff
   >   private val eligibilityQuestions: List<QuestionModel<Any>> = listOf(
   >       ChoiceQuestionModel(
   >          "age",
   >           "What's your age?",
   >          candidates = (20..50).toList(),
   >           viewType = DropMenu
   >       ),
   >       ChoiceQuestionModel(
   >           "gender",
   >           "What's your gender?",
   >           candidates = listOf("Male", "Female"),
   >       ),
   >       ChoiceQuestionModel(
   >   -        "hasCardiac",
   >   -        "Do you have any existing cardiac conditions?",
   >   -        "Examples of cardiac conditions include abnormal heart rhythms, or arrhythmias",
   >   -        candidates = listOf("Yes", "No"),
   >   -        answer = "Yes"
   >   -   ),
   >   -   ChoiceQuestionModel(
   >   -        "hasWearableDevice",
   >   -        "Do you currently own a wearable device?",
   >   -        "Examples of wearable devices include Samsung Galaxy Watch 4, Fitbit, OuraRing, etc.",
   >   +        "hasGalaxyWatch"
   >   +        "Do you have any Galaxy Watch?"
   >           candidates = listOf("Yes", "No"),
   >           answer = "Yes"
   >       )
   >   ) as List<QuestionModel<Any>>
   >   ```
