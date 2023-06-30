---


title: Account Service API Endpoints
sidebar: dev_doc_sidebar
permalink: account-service-api-endpoints.html
toc: false


---


# Account Service
## Version: 0.7.0

You can also find more interactive document here: [SwaggerHub-Account_Service/0.7.0](https://app.swaggerhub.com/apis-docs/zainalisamsung/account-service/0.7.0)

### /account-service/invitations

#### POST
##### Summary

Invite a new user for specific project.

##### Description

When someone is invited, platform will send a invitation mail with invitation-link to given email address.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | A new account was created with given email. |
| default | unexpected error |

### /account-service/user/password/reset

#### POST
##### Summary

Reset password

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | unexpected error |

### /account-service/signin

#### POST
##### Summary

Sign in a user with email and password

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | unexpected error |

### /account-service/signup

#### POST
##### Summary

Sign up a new user

##### Description

Sign up a new user. The server will then send a verification link to the given email address.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | A new account was created. |
| 409 | Given email was already registered. |
| default | unexpected error |

### /account-service/user/roles

#### PUT
##### Summary

Assign roles to user

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | unexpected error |

### /account-service/user/roles/remove

#### POST
##### Summary

Remove roles from user

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | unexpected error |

### /account-service/users

#### GET
##### Summary

Get user list

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | query | Specific project id to retrieve users | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | Unexpected Error |

### /account-service/token/refresh

#### POST
##### Summary

Refresh Access Token.

##### Description

Request new token by sending pair of jwt(accessToken) and refreshToken.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| default | unexpected error |

### /account-service/user/email/verify

#### POST
##### Summary

Verify email with token.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| 401 | Invalid token error |
| default | unexpected error |

### /account-service/verification

#### POST
##### Summary

Resend a verification mail.

##### Description

The server will resend a verification link to the given email address.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | The operation was successful. |
| 400 | bad request |
| 409 | The email was already verified. |
| 500 | unexpected error |

### Models

#### InvitationReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| InvitationReq | array |  |  |

#### Invitation

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| roles | [ string ] |  | Yes |

#### Roles

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Roles | array |  |  |

#### Role

A role is either system role or project role.
Researchers must have project roles to access specific project.

- The format of project role is as follow: $project_id:$role_name

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Role | string | A role is either system role or project role. Researchers must have project roles to access specific project. - The format of project role is as follow: $project_id:$role_name  |  |

**Example**
<pre>project_sample:researcher</pre>

#### ResetPasswordReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| resetToken | string | _Example:_ `"aadfad...badfdfad"` | Yes |
| password | string |  | Yes |
| profile | object | Account information in JSON without pre-defined fields<br>_Example:_ `{"name":"david.lee","status":"active"}` | No |

#### SignInReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| password | string |  | Yes |

#### SignInResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| id | string | _Example:_ `"7d08351b-85b6-488e-a8a2-b8653defb865"` | Yes |
| jwt | string | Signed Json Web Token. payload is as below. {   "email": "cubist@samsung.com",   "roles": ["study_1:owner", "study_2:research"],   "iss": "https://research-hub.io/",   "exp": 1660377937,   "iat": 1660291536 } <br>_Example:_ `"eyJhbGc...ssw5c"` | Yes |
| refreshToken | string | _Example:_ `"aadfad...badfdfad"` | Yes |
| roles | [ string ] |  | Yes |
| profile | object | Account information in JSON without pre-defined fields<br>_Example:_ `{"name":"david.lee","status":"active"}` | Yes |

#### SignUpReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| password | string |  | Yes |
| profile | object | Account information in JSON without pre-defined fields<br>_Example:_ `{"name":"david.lee","status":"active"}` | Yes |

#### RoleReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| accountId | string | _Example:_ `"7d08351b-85b6-488e-a8a2-b8653defb865"` | Yes |
| roles | [ string ] |  | Yes |

#### RefreshReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| jwt | string | Signed Json Web Token. payload is as below. {   "email": "cubist@samsung.com",   "roles": ["study_1:owner", "study_2:research"],   "iss": "https://research-hub.io/",   "exp": 1660377937,   "iat": 1660291536 } <br>_Example:_ `"eyJhbGc...ssw5c"` | Yes |
| refreshToken | string | _Example:_ `"aadfad...badfdfad"` | Yes |

#### RefreshResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| jwt | string | Signed Json Web Token. payload is as below. {   "email": "cubist@samsung.com",   "roles": ["study_1:owner", "study_2:research"],   "iss": "https://research-hub.io/",   "exp": 1660377937,   "iat": 1660291536 } <br>_Example:_ `"eyJhbGc...ssw5c"` | Yes |
| refreshToken | string | _Example:_ `"aadfad...badfdfad"` | Yes |

#### VerifyEmailReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| token | string | _Example:_ `"aadfad...badfdfad"` | Yes |

#### VerifyEmailResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| id | string | _Example:_ `"7d08351b-85b6-488e-a8a2-b8653defb865"` | Yes |
| jwt | string | Signed Json Web Token. payload is as below. {   "email": "cubist@samsung.com",   "roles": ["study_1:owner", "study_2:research"],   "iss": "https://research-hub.io/",   "exp": 1660377937,   "iat": 1660291536 } <br>_Example:_ `"eyJhbGc...ssw5c"` | Yes |
| refreshToken | string | _Example:_ `"aadfad...badfdfad"` | Yes |
| roles | [ string ] |  | Yes |
| profile | object | Account information in JSON without pre-defined fields<br>_Example:_ `{"name":"david.lee","status":"active"}` | Yes |

#### VerificationReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |

#### Users

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Users | array |  |  |

#### User

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string (email) | _Example:_ `"cubist@samsung.com"` | Yes |
| id | string | _Example:_ `"7d08351b-85b6-488e-a8a2-b8653defb865"` | Yes |
| roles | [ string ] |  | No |
| profile | object | Account information in JSON without pre-defined fields<br>_Example:_ `{"name":"david.lee","status":"active"}` | No |

#### Profile

Account information in JSON without pre-defined fields

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Profile | object | Account information in JSON without pre-defined fields |  |

**Example**
<pre>{
  "name": "david.lee",
  "status": "active"
}</pre>

#### Token

Signed Json Web Token.
payload is as below.
{
  "email": "cubist@samsung.com",
  "roles": ["study_1:owner", "study_2:research"],
  "iss": "https://research-hub.io/",
  "exp": 1660377937,
  "iat": 1660291536
}

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Token | string | Signed Json Web Token. payload is as below. {   "email": "cubist@samsung.com",   "roles": ["study_1:owner", "study_2:research"],   "iss": "https://research-hub.io/",   "exp": 1660377937,   "iat": 1660291536 }  |  |

**Example**
<pre>eyJhbGc...ssw5c</pre>

#### Email

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Email | string |  |  |

**Example**
<pre>cubist@samsung.com</pre>

#### AccountId

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| AccountId | string |  |  |

**Example**
<pre>7d08351b-85b6-488e-a8a2-b8653defb865</pre>

#### ProjectId

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ProjectId | string |  |  |

**Example**
<pre>100</pre>

#### ResetToken

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ResetToken | string |  |  |

**Example**
<pre>aadfad...badfdfad</pre>

#### RefreshToken

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| RefreshToken | string |  |  |

**Example**
<pre>aadfad...badfdfad</pre>

#### VerifyEmailToken

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| VerifyEmailToken | string |  |  |

**Example**
<pre>aadfad...badfdfad</pre>

#### Error

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | string |  | Yes |
| message | string |  | Yes |
