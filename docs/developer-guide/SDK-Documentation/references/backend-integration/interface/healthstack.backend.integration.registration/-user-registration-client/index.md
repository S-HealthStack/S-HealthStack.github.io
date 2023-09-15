
[Interface](../../../index.html) > [healthstack.backend.integration.registration](../index.html) > [UserRegistrationClient](index.html)



# UserRegistrationClient



[androidJvm]\
interface [UserRegistrationClient](index.html)

Interface for registering users who joined through the app to the backend.



## Functions


| Name | Summary |
|---|---|
| [registerUser](register-user.html) | [androidJvm]<br>abstract suspend fun [registerUser](register-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), user: [User](../-user/index.html))<br>Used to register user's information who joined through the app to the backend. |
| [updateUser](update-user.html) | [androidJvm]<br>abstract suspend fun [updateUser](update-user.html)(idToken: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userId: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), userProfile: [UserProfile](../-user-profile/index.html))<br>Used to update user's profile who joined through the app to the backend. |


## Inheritors


| Name |
|---|
| [BackendFacade](../../healthstack.backend.integration/-backend-facade/index.html) |

