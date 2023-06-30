---
title: Full-Stack Tutorial
sidebar: doc_sidebar
permalink: tutorial.html
toc: true
---

{% include warning.html title="Warning" content="Documentation for v1.0 official release is currently under construction. Note that the information on this page may be outdated." %}

This getting started tutorial describes the steps you need to be up and running with your own study using the full Samsung Health Stack. The best way to explain the steps is to walk through a simple example, which was presented at the Samsung Developer Conference (SDC2022). Follow these steps to get started with .

## Set up your environment

The stack consists of three pieces, which you install separately:

1. [Install the backend services and data engine.](../installation/install-backend.md)
2. [Install the app software development kit (SDK).](../installation/install-sdk.md)
3. [Install the web portal.](../installation/install-portal.md)

## Set up a study

In this fictitious scenario, we've noticed that people with supernatural physical abilities have begun to appear all over the world. We call this phenomenon *Syndrome X*. We hypothesize that Syndrome X is related to specific vital signs and symptoms, such as heart rate, blood pressure, and headaches. So, we design a study to gather participants who have experienced extraordinary powers, ask them survey questions, and collect their vital signs and any symptoms. We've decided to call it the Mutant Gene (MG) study. We will collect vital signs using the Galaxy Watch 4 and symptoms using a participant survey.

Studies are managed from the Samsung Health Stack web portal.

> As of this writing, Chrome is the only browser supported for accessing the web portal.

Follow these steps to set up managing the MG study:

1. [Create a new study](../../portal-guide/study-management/creating-a-study.md) in the web portal.
    > Because this is the first time logging in to the portal, the **Create a study** page automatically appears. Enter these parameters:
    >
    > - Study Name: `MG Study`
    > - Study Logo: whichever color you prefer

2. [Invite members and assign their roles](../../portal-guide/study-management/portal-manage-members.md) to help conduct the study.

    > Creating the initial study automatically prompts you to invite members. Let's invite Dr. McCoy as a principal investigator. Enter these parameters:
    >
    > - Email: `daniel.mccoy@researchuniversity.org`
    > - Role: `Principal Investigator`

3. [Create a participant survey](../../portal-guide/content-creation/creating-a-survey.md).

    > From the **Study Management** page, click **Create survey** and enter these parameters:
    > - Title: Daily Symptom Report
    > - Question 1: `How intense were your headaches yesterday?`
    >   - Type: `Slider scale`
    >   - Scale: `0 (None) to 10 (Almost dying)`
    > - Question 2: `Which symptom did you experience yesterday?`
    >   - Type: `Single-selection`
    >   - Options: `Nothing, Mind reading, Laser vision, Levitation`

4. [Schedule and publish the survey.](../../portal-guide/content-creation/publishing-a-survey.md)
    > From the **Create survey** page, click **Publish** and enter these parameters:
    > - Frequency: `Daily`
    > - Survey occurrence: Relevant publish time and duration. 

## Build the mobile app

For our study, participants wear the Samsung Galaxy Watch 4 and use an Android mobile app to collect the data. Follow these steps to use the Samsung Health Stack app SDK to create and customize the app:

1. If you are not already familiar with developing code in Android Studio, take a look at [https://developer.android.com/studio/intro](https://developer.android.com/studio/intro){:target="_blank"}.

2. In Android Studio, clone the [starter-app GitHub repository](https://github.com/S-HealthStack/starter-app){:target="_blank"} to retrieve the app starter code.

   > `git clone https://github.com/S-HealthStack/starter-app`

3. Edit the code in the `main` branch to customize it for our study.

   > In **starter-app/app/src/main/java/com/samsung/healthstack/starter_app/MainActivity.kt**:
   >
   > - In `override fun onCreate`, add a line to capture blood pressure data:
   >
   >   ```diff
   >   override fun onCreate(savedInstanceState: Bundle?) {
   >       super.onCreate(savedInstanceState)
   >                                                                             
   >       val healthDataRequired = listOf("HeartRate", "Steps", "SleepSession")
   >       val healthDataToDisplay = listOf(HEART_RATE, SLEEP_SESSION, TASK_DATA_TYPE)
   >       val healthDataSyncSpecs = listOf(
   >           SyncManager.HealthDataSyncSpec("HeartRate", 15, TimeUnit.MINUTES),
   >           SyncManager.HealthDataSyncSpec("Steps", 1, TimeUnit.DAYS),
   >   -       SyncManager.HealthDataSyncSpec("SleepSession", 1, TimeUnit.DAYS)
   >   +       SyncManager.HealthDataSyncSpec("SleepSession", 1, TimeUnit.DAYS),
   >   +       SyncManager.HealthDataSyncSpec("BloodPressure", 2, TimeUnit.HOURS)
   >       )
   >   ```
   > 
   > In **starter-app/app/src/main/java/com/samsung/healthstack/starter_app/OnboardingModule.kt**:
   > 
   > - In `private fun intro`, change the study title and intro description:
   > 
   >   ```diff
   >   private fun intro(@ApplicationContext context: Context) = IntroModel(
   >       id = "intro",
   >   -   title = "CardioFlow",
   >   +   title = "MG Study",
   >       drawableId = R.drawable.sample_image_alpha4,
   >       logoDrawableId = R.drawable.ic_launcher,
   >       summaries = listOf(
   >           R.drawable.ic_watch to "Wear your\nwatch",
   >           R.drawable.ic_alert to "10 min\na day",
   >           R.drawable.ic_home_task to "2 surveys\na week"
   >       ),
   >       sections = listOf(
   >           IntroSection(
   >               "Overview",
   >   -           "CardioFlow is a study developed by the University of California, San Francisco.\n\n" +
   >   -               "Through this study, we identify and measure the data of your vital signs and symptom reports.\n\n" +
   >   -               "With your help, we could test our algorithms and develop technology that contributes to preventing cardiovascular diseases in the U.S.",
   >   +           "There is a Syndrome called "X" and it suddenly gives some people special power.\n\n" +
   >   +           "We hypothesize that Syndrome X is related to specific vital signs and symptoms.\n\n" +
   >   +           "So we are doing this mutant gene (MG) study to prove our hypothesis.",
   >          ),
   >           IntroSection(
   >               "How to participate",
   >               "Wear the watch as much as possible and take active measurements 3 times a day when notified."
   >           )
   >       )
   >   )
   >   ```
   > 
   > - In `private fun signUp`, change the study title:
   > 
   >   ```diff
   >   private fun signUp() = SignUpModel(
   >       id = "sign-up-model",
   >   -   title = "CardioFlow",
   >   +   title = "MG Study",
   >       listOf(Basic, Google),
   >       description = "Thanks for joining the study!\nNow please create an account to keep track\nof your data and keep it safe.",
   >       drawableId = R.drawable.ic_launcher
   >   )
   >   ```
   > 
   > - In `private fun registrationCompleted`, change the title reference in the description:
   > 
   >   ```diff
   >   private fun registrationCompleted() =
   >       RegistrationCompletedModel(
   >           id = "registration-completed-model",
   >          title = "You are done!",
   >           buttonText = "Continue",
   >   -       description = "Congratulations! Everything is all set for you. Now please tap on the button below to start your CardioFlow journey!",
   >   +       description = "Congratulations! Everything is all set for you. Now please tap on the button below to start your MG Study journey!",
   >           drawableId = R.drawable.sample_image_alpha1
   >       )
   >   ```
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

4. Register your app with [the Firebase project you created](../installation/install-sdk.md#vii-create-a-firebase-project) during app SDK installation and update the **starter-app/app/google-service.json** configuration file.

   > Refer to [https://firebase.google.com/docs/android/setup](https://firebase.google.com/docs/android/setup){:target="_blank"} for details.

5. Associate your app with the backend system and portal study.
   > In **starter-app/app/src/main/res/values/strings.xml**, update the lines at the bottom of the file that specify your backend system's endpoint and your study's project ID, for example:
   > ```
   >   <string name="research_platform_endpoint">https://shs.dev.ai-service.io</string>
   >   <string name="research_project_id">1</string>
   > ```
   > Note: The project ID of your study is contained in the JSON response of a `POST /api/projects` request.

6. Build the app and test.

   > Due to the lack of mature libraries for wearables, testing with the Android Studio emulator is quite limited. At this point in time, most of the testing needs to happen in the live app.

7. Make your app available for downloading by study participants.

## Onboard the participants

The first step of onboarding is to onboard yourself to live test the app. Follow these participant onboarding steps:

1. Download the app to your phone.
2. Open the app and step through the prompts that you set up while building the app to determine eligibility, request consent, and register those who are eligible.
3. If not already previously done, install the [Health Connect](https://play.google.com/store/apps/details?id=com.google.android.apps.healthdata){:target="_blank"} app on your phone.
4. If not already previously done, pair your phone and the Samsung Galaxy Watch 4.

Once you've tested the app to your satisfaction, invite prospective participants to complete the participant onboarding steps and join the study.

## Run the study to collect the data

In a real-world situation, the study would run until the scheduled end date you specified during survey. For this tutorial, have each participant (including yourself):

- Wear the watch to generate some data.
- Open the app and complete the daily survey.

- Use the app to see the data visualizations available to participants.


## Analyze the results

Now, return to the web portal to analyze the results. Results are available for each participant separately and for the study as a whole. You can:

- [View various graphs](../../portal-guide/results-analysis/viewing-graphs.md).

- [View individual participant results](../../portal-guide/results-analysis/viewing-individual-results.md).

- [Run queries](../../portal-guide/results-analysis/running-a-query.md).
  
   > From the **Data Insights** page, in the **Data Query** section, enter these parameters to list people who have experienced any symptoms of Syndrome X:
   > - Table: `item_results`
   > - Query:
   > ```
   >   `SELECT up.user_id, json_extract_scalar(up.profile, '$.email') AS email, result 
   >   FROM item_results ir JOIN user_profiles up ON up.user_id = ir.user_id 
   >   WHERE item_name='Question1' AND result !='Nothing' 
   >   GROUP BY up.user_id, json_extract_scalar(up.profile, '$.email'), result `
   > ```
   > 
   > Next, enter these parameters to compare the vital signs of those people and the people who have symptoms:
   > - Table: `item_results`
   > - Query:
   > ```
   >   `SELECT CASE WHEN hr.user_id IN 
   >       (
   >       /    SELECT user_id 
   >           FROM item_results 
   >           WHERE item_name='Question1' AND result !='Nothing' 
   >           GROUP BY user_id 
   >       ) THEN 'syndromeX' 
   >       ELSE 'normal human' 
   >       END AS result1, 
   >       AVG(hr.bpm) AS bpm, AVG(CAST(ir.result AS INT)) AS intensity 
   >   FROM  heartrates hr, item_results ir 
   >   WHERE ir.user_id=hr.user_id AND hr.user_id=ir.user_id AND ir.item_name='Question0' 
   >   GROUP BY CASE WHEN hr.user_id IN 
   >       ( 
   >           SELECT user_id 
   >           FROM item_results 
   >           WHERE item_name='Question1' AND result !='Nothing' 
   >           GROUP BY user_id 
   >       ) THEN 'syndromeX' 
   >       ELSE 'normal human'
   >       END `
   > ```
   > 
   > Due to the limited data sample size, you'll likely see no meaningful difference between the two groups.
   
- [Export the data for external analysis](../../portal-guide/results-analysis/exporting-data.md).
  
   > In the **Query Results** table, click **Export .csv**.
