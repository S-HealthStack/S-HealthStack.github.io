

# HealthStack Backend Integration Tutorial


In this tutorial, we will learn how to integrate the HealthStack Backend with your application using the provided classes and interfaces. The backend integration package is designed to help you easily manage user registration, health data synchronization, and task management.

## Overview

The HealthStack Backend Integration package contains the following components:

1. `BackendFacade`: Facade that collects the interface required for integrating with the backend that stores health data.
2. `BackendFacadeHolder`: Singleton holder for the `BackendFacade` instance.
3. `RegisterException` and `UserAlreadyExistsException`: Exception classes for handling registration-related errors.
4. `HealthDataSyncClient`: Interface for syncing health data with the backend.
5. `UserRegistrationClient`: Interface for registering users with the backend.
6. `TaskClient`: Interface for managing tasks from the backend.

Additionally, there are multiple classes for representing user and task data:

- `User`
- `ItemResult`
- `TaskResult`
- `TaskSpec`

## Setup

First, ensure that the HealthStack Backend Integration package is imported into your project. Add the following dependencies in your `build.gradle` file:

```
implementation 'healthstack.backend.integration:interface:VERSION'
```

Replace `VERSION` with the latest available version of the package. We currently have two versions available: ***0.9a***, our alpha, and 0.9b, our beta. Find more information about the beta version here: https://central.sonatype.com/artifact/io.s-healthstack/backend-integration/0.9b.

## Using BackendFacade

`BackendFacade` is the main entry point for working with the backend. It implements the following interfaces:

- `HealthDataSyncClient`
- `UserRegistrationClient`
- `TaskClient`

Create an instance of `BackendFacade` by using the singleton instance provided by `BackendFacadeHolder`:

```
val backendFacade = BackendFacadeHolder.instance
```

You can now use the `backendFacade` instance to access methods for user registration, health data synchronization, and task management.

## User Registration

To register a new user with the backend, use the `registerUser` method of the `UserRegistrationClient` interface:

```
val idToken = "idToken"
val user = User(userId = "userId", profile = "profile")

try {
    backendFacade.registerUser(idToken, user)
} catch (e: UserAlreadyExistsException) {
    // Handle the case when the user already exists
} catch (e: RegisterException) {
    // Handle other registration errors
}
```

Replace `"idToken"` with a valid ID token obtained during user authentication, and provide the user's profile information as required.

## Health Data Synchronization

To synchronize health data with the backend, use the `syncHealthData` method of the `HealthDataSyncClient` interface:

```
val idToken = "idToken"
val healthData = "healthData"

backendFacade.syncHealthData(idToken, healthData)
```

Replace `"healthData"` with the actual health data collected through the HealthStack HealthDataLink.

## Task Management

To retrieve tasks from the backend, use the `getTasks` method of the `TaskClient` interface:

```
val idToken = "idToken"
val lastSyncTime = "lastSyncTime"
val endTime = "endTime"

val tasks = backendFacade.getTasks(idToken, lastSyncTime, endTime)
```

To upload a user's task execution result to the backend, use the `uploadTaskResult` method of the `TaskClient` interface:

```
val idToken = "idToken"
val taskResult = TaskResult(
    userId = "userId",
    taskId = "taskId",
    revisionId = "revisionId",
    startedAt = "startedAt",
    submittedAt = "submittedAt",
    itemResults = listOf(ItemResult("itemName", "result"))
)

backendFacade.uploadTaskResult(idToken, taskResult)
```

Replace the placeholders with actual data from the task execution.

## Working with TaskSpec and TaskResult

`TaskSpec` is a data class that represents the task received from the backend. It contains information about the task, its items, and the contents of each item. To create a `TaskSpec` instance, you can use the data received from the `getTasks` method:

```kotlin
val taskSpec = TaskSpec(
    revisionId = "revisionId",
    taskId = "taskId",
    title = "title",
    description = "description",
    schedule = "schedule",
    startTime = "startTime",
    endTime = "endTime",
    validTime = "validTime",
    items = listOf(/* ... */)
)
```

Replace the placeholders with actual data from the backend.

`TaskResult` is a data class that represents the result of a task. It contains information about the user, the completed task, and the results of each item in the task. To create a `TaskResult` instance, you can use the data from the task execution:

```
val taskResult = TaskResult(
    userId = "userId",
    taskId = "taskId",
    revisionId = "revisionId",
    startedAt = "startedAt",
    submittedAt = "submittedAt",
    itemResults = listOf(ItemResult("itemName", "result"))
)
```

Replace the placeholders with actual data from the task execution.

## Conclusion

In this tutorial, we've covered how to integrate the HealthStack Backend with your application using the provided classes and interfaces. By following these steps, you can easily manage user registration, health data synchronization, and task management in your application.
