

# HealthStack Kit Tutorial


In this tutorial, we will walk through creating a custom task using the HealthStack Kit library. Our example will be a simple onboarding task with multiple steps. By the end of this tutorial, you should have a basic understanding of how to use the main objects provided in the `healthstack.kit.task.base` package.

## Prerequisites

Before we begin, ensure that you have the HealthStack Kit library integrated into your project.

## Step 1: Create a new Task

First, let's create a new task by extending the `OrderedTask` class. This class is ideal for tasks with multiple steps. Create a new file `OnboardingTask.kt` and add the following code:

```
import healthstack.kit.task.base.OrderedTask

class OnboardingTask(
    id: String,
    name: String,
    description: String
) : OrderedTask(id, name, description)
```

## Step 2: Define StepModel classes

Now, we need to define `StepModel` classes for each step in our onboarding task. For this tutorial, we will create two steps: `WelcomeStepModel` and `ProfileInfoStepModel`. Add the following code to your project:

```
import healthstack.kit.task.base.StepModel

class WelcomeStepModel : StepModel("welcome", "Welcome", R.drawable.welcome_image)
class ProfileInfoStepModel : StepModel("profile_info", "Profile Information", R.drawable.profile_info_image)
```

Replace `R.drawable.welcome_image` and `R.drawable.profile_info_image` with appropriate drawable resources.

## Step 3: Create View classes

Next, we need to create `View` classes for rendering the UI of each step. Create two new classes: `WelcomeView` and `ProfileInfoView`. These classes should extend the `View` class and implement the `Render` method:

```
import healthstack.kit.task.base.View
import androidx.compose.runtime.Composable

class WelcomeView : View<WelcomeStepModel>() {
    @Composable
    override fun Render(model: WelcomeStepModel, callbackCollection: CallbackCollection) {
        // Add UI components for the welcome step
    }
}

class ProfileInfoView : View<ProfileInfoStepModel>() {
    @Composable
    override fun Render(model: ProfileInfoStepModel, callbackCollection: CallbackCollection) {
        // Add UI components for the profile info step
    }
}
```

## Step 4: Create Step classes

Now, let's create `Step` classes for each step in our onboarding task. Create two new classes: `WelcomeStep` and `ProfileInfoStep`. These classes should extend the `Step` class and implement the required methods:

```
import healthstack.kit.task.base.Step

class WelcomeStep : Step<WelcomeStepModel, Unit>(
    id = "welcome",
    name = "Welcome",
    model = WelcomeStepModel(),
    view = WelcomeView()
) {
    override fun getResult(): Unit = Unit
}

class ProfileInfoStep : Step<ProfileInfoStepModel, Unit>(
    id = "profile_info",
    name = "Profile Information",
    model = ProfileInfoStepModel(),
    view = ProfileInfoView()
) {
    override fun getResult(): Unit = Unit
}
```

## Step 5: Add steps to the task

Finally, let's add our steps to the `OnboardingTask`:

```
import healthstack.kit.task.base.OrderedTask
import healthstack.kit.task.base.Step

class OnboardingTask(
    id: String,
    name: String,
    description: String
) : OrderedTask
(id, name, description) {
init {
| Add steps to the task
steps.add(WelcomeStep())
steps.add(ProfileInfoStep())
}
}
```

Now, your `OnboardingTask` is ready to be used in your application. When you create an instance of the `OnboardingTask`, it will contain two steps: `WelcomeStep` and `ProfileInfoStep`. You can use the `nextStep` and `previousStep` methods provided by the `OrderedTask` class to navigate between steps.

```kotlin
val onboardingTask = OnboardingTask(
    id = "onboarding_task",
    name = "Onboarding Task",
    description = "A simple onboarding task with two steps"
)

// Start the onboarding task by rendering the first step
onboardingTask.start()
```

To render the UI for each step, you need to call the `render` method of the `Step` class, which in turn calls the `Render` method of the `View` class associated with that step.

## Conclusion

In this tutorial, we've created a simple onboarding task using the HealthStack Kit library. We've learned how to create a custom `Task`, define `StepModel` classes, create `View` classes for rendering the UI, and create `Step` classes for each step in the task.

By following these steps, you can create your own custom tasks and utilize the power of the HealthStack Kit library to build complex and engaging health-related applications.
