
[Interface](../../../index.html) > [healthstack.backend.integration.registration](../index.html) > [UserRegistrationClient](index.html) > [updateUser](update-user.html)



# updateUser



[androidJvm]\
abstract suspend fun [updateUser](update-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userProfile: [UserProfile](../-user-profile/index.html))



Used to update user's profile who joined through the app to the backend.



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| userId | Id of the user to be updated. |
| userProfile | Data including profile information collected from the Profile View. |




