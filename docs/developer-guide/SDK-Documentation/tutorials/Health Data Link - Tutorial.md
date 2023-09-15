

# Health Data Link - Tutorial


In this tutorial, we will walk through how to use the Health Data Link package to manage health data within your application. We will cover how to set up permissions, read health data, and handle changes in the data.

## Prerequisites

- A project set up with the Health Data Link package

## Step 1: Set up permissions

To work with health data, you will first need to check if your app has the required permissions. Use the `checkPermissions` method provided by the `HealthDataLink` interface to check if all necessary permissions are granted.

```
val healthDataLink = HealthDataLinkHolder.getInstance()

if (!healthDataLink.checkPermissions()) {
    // Request permissions
}
```

If the permissions are not granted, request them using the `requestPermissions` method:

```
healthDataLink.requestPermissions()
```

## Step 2: Read health data

To read health data, use the `readHealthData` method provided by the `HealthDataLink` interface. You will need to specify the start and end times for the data range and the type of health data you want to read.

```
val startTime = // Start point of the time range
val endTime = // End point of the time range
val healthDataTypeName = // Type of health data to read (ex: BloodPressure)

val healthData: HealthData = healthDataLink.readHealthData(startTime, endTime, healthDataTypeName)
```

## Step 3: Request an initial changes token

To track changes in health data, you will need to request an initial changes token. Use the `requestInitialChangesToken` method and specify the type of health data you want to track.

```
val healthDataTypeName = // Type of health data to track (ex: BloodPressure)

val initialChangesToken: String = healthDataLink.requestInitialChangesToken(healthDataTypeName)
```

## Step 4: Read change events

After obtaining the initial changes token, you can use it to read change events using the `readChanges` method. Change events are usually categorized as Upsertion or Deletion.

```
val token = // Changes token
val healthDataTypeName = // Type of health data to read (ex: BloodPressure)

val change: Change = healthDataLink.readChanges(token, healthDataTypeName)
```

## Step 5: Check if health data type is Interval data

You may need to check if a given health data type is considered Interval data. Use the `isIntervalDataType` method to do so.

```
val healthDataTypeName = // Type of health data to check (ex: SleepSession)

val isInterval: Boolean = healthDataLink.isIntervalDataType(healthDataTypeName)
```

## Conclusion

In this tutorial, we walked through how to use the Health Data Link package to manage health data within your application. We covered how to set up permissions, read health data, and handle changes in the data. By integrating the Health Data Link package, you can streamline the process of working with health data in your application.
