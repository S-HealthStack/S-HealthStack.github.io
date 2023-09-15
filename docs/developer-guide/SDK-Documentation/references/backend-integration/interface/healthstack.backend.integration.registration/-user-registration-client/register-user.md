
[Interface](../../../index.html) > [healthstack.backend.integration.registration](../index.html) > [UserRegistrationClient](index.html) > [registerUser](register-user.html)



# registerUser



[androidJvm]\
abstract suspend fun [registerUser](register-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), user: [User](../-user/index.html))



Used to register user's information who joined through the app to the backend.



## Parameters


androidJvm

| | |
|---|---|
| idToken | An encrypted token containing the user's information issued when the logs in to the application. |
| user | Data including profile information collected during the Eligibility Check and the basic information of user. |




