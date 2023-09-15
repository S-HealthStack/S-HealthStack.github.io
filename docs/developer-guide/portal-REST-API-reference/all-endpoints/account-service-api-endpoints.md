
# Account Service v0.7.0



<h1 id="account-service">Account Service v0.7.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="account-service-invitation">Invitation</h1>

## Invites a new user to a specific project

> Code samples

```java
URL obj = new URL("/account-service/invitations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/invitations`

This operation invites a new user to a specific project. The platform sends an invitation email with an invitation link to the provided email address.

> Body parameter

```json
[
  {
    "email": "cubist@samsung.com",
    "roles": [
      "project_sample:research-assistant"
    ]
  }
]
```

<h3 id="invites-a-new-user-to-a-specific-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]|true|none|

> Example responses

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="invites-a-new-user-to-a-specific-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|A new account has been created with the provided email.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="invites-a-new-user-to-a-specific-project-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="account-service-researchassistant">ResearchAssistant</h1>

## Verifies the provided email and sends a reset password email

> Code samples

```java
URL obj = new URL("/account-service/user/password/forgot");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/user/password/forgot`

This operation accepts an email address. If the provided email address is registered, the server sends a password reset email. If not, it returns a 404 response.

> Body parameter

```json
{
  "email": "string"
}
```

<h3 id="verifies-the-provided-email-and-sends-a-reset-password-email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

<h3 id="verifies-the-provided-email-and-sends-a-reset-password-email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|The provided email is malformed.|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The email is not registered.|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Resets the password

> Code samples

```java
URL obj = new URL("/account-service/user/password/reset");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/user/password/reset`

This operation resets the user's password. The "profile" field is optional. If no value is set for this field, the server doesn't change the user's profile.

> Body parameter

```json
{
  "resetToken": "aadfad...badfdfad",
  "password": "string",
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}
```

<h3 id="resets-the-password-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> 200 Response

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}
```

<h3 id="resets-the-password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="resets-the-password-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» email|string(email)|true|none|none|
|» id|string|true|none|none|
|» jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|» refreshToken|string|true|none|none|
|» roles|[string]|true|none|none|
|» profile|object|true|none|Account information in JSON without pre-defined fields.|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Signs in a user with an email and password

> Code samples

```java
URL obj = new URL("/account-service/signin");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/signin`

> Body parameter

```json
{
  "email": "cubist@samsung.com",
  "password": "string"
}
```

<h3 id="signs-in-a-user-with-an-email-and-password-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> 200 Response

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}
```

<h3 id="signs-in-a-user-with-an-email-and-password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="signs-in-a-user-with-an-email-and-password-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» email|string(email)|true|none|none|
|» id|string|true|none|none|
|» jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|» refreshToken|string|true|none|none|
|» roles|[string]|true|none|none|
|» profile|object|true|none|Account information in JSON without pre-defined fields.|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Signs up a new user

> Code samples

```java
URL obj = new URL("/account-service/signup");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/signup`

This operation signs up a new user. Afterwards, the server sends a verification link to the provided email address.

> Body parameter

```json
{
  "email": "cubist@samsung.com",
  "password": "string",
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}
```

<h3 id="signs-up-a-new-user-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="signs-up-a-new-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|A new account has been created.|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|The provided email is already registered.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="signs-up-a-new-user-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Refreshes the access token

> Code samples

```java
URL obj = new URL("/account-service/token/refresh");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/token/refresh`

This operation requests a new token by sending a pair of JWT (accessToken) and refreshToken.

> Body parameter

```json
{
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad"
}
```

<h3 id="refreshes-the-access-token-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> 200 Response

```json
{
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad"
}
```

<h3 id="refreshes-the-access-token-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="refreshes-the-access-token-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|» refreshToken|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="account-service-role">Role</h1>

## Assigns roles to a user

> Code samples

```java
URL obj = new URL("/account-service/user/roles");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`PUT /account-service/user/roles`

> Body parameter

```json
{
  "accountId": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "roles": [
    "project_sample:research-assistant"
  ]
}
```

<h3 id="assigns-roles-to-a-user-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="assigns-roles-to-a-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="assigns-roles-to-a-user-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Removes roles from a user

> Code samples

```java
URL obj = new URL("/account-service/user/roles/remove");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/user/roles/remove`

> Body parameter

```json
{
  "accountId": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "roles": [
    "project_sample:research-assistant"
  ]
}
```

<h3 id="removes-roles-from-a-user-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="removes-roles-from-a-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="removes-roles-from-a-user-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="account-service-user">User</h1>

## Retrieves a list of users

> Code samples

```java
URL obj = new URL("/account-service/users?projectId=100");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`GET /account-service/users`

<h3 id="retrieves-a-list-of-users-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|query|string|true|The ID of the specific project for which to retrieve users|

> Example responses

> 200 Response

```json
[
  {
    "email": "cubist@samsung.com",
    "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
    "roles": [
      "project_sample:research-assistant"
    ],
    "profile": {
      "name": "david.lee",
      "status": "active"
    }
  }
]
```

<h3 id="retrieves-a-list-of-users-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieves-a-list-of-users-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» email|string(email)|true|none|none|
|» id|string|true|none|none|
|» roles|[string]|false|none|none|
|» profile|object|false|none|Account information in JSON without pre-defined fields.|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="account-service-email-verification">Email Verification</h1>

## Verifies the email with a token

> Code samples

```java
URL obj = new URL("/account-service/user/email/verify");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/user/email/verify`

> Body parameter

```json
{
  "token": "aadfad...badfdfad"
}
```

<h3 id="verifies-the-email-with-a-token-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> 200 Response

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}
```

<h3 id="verifies-the-email-with-a-token-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The token is invalid.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="verifies-the-email-with-a-token-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» email|string(email)|true|none|none|
|» id|string|true|none|none|
|» jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|» refreshToken|string|true|none|none|
|» roles|[string]|true|none|none|
|» profile|object|true|none|Account information in JSON without pre-defined fields.|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Resends a verification email

> Code samples

```java
URL obj = new URL("/account-service/verification");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /account-service/verification`

This operation resends a verification link to the provided email address.

> Body parameter

```json
{
  "email": "cubist@samsung.com"
}
```

<h3 id="resends-a-verification-email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|

> Example responses

> 500 Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="resends-a-verification-email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The operation was successful.|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|The request is bad.|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|The email has already been verified.|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An unexpected error has occurred.|Inline|

<h3 id="resends-a-verification-email-responseschema">Response Schema</h3>

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_InvitationReq">InvitationReq</h2>

<a id="schemainvitationreq"></a>
<a id="schema_InvitationReq"></a>
<a id="tocSinvitationreq"></a>
<a id="tocsinvitationreq"></a>

```json
[
  {
    "email": "cubist@samsung.com",
    "roles": [
      "project_sample:research-assistant"
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|roles|[string]|true|none|none|

<h2 id="tocS_Invitation">Invitation</h2>

<a id="schemainvitation"></a>
<a id="schema_Invitation"></a>
<a id="tocSinvitation"></a>
<a id="tocsinvitation"></a>

```json
{
  "email": "cubist@samsung.com",
  "roles": [
    "project_sample:research-assistant"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|roles|[string]|true|none|none|

<h2 id="tocS_Roles">Roles</h2>

<a id="schemaroles"></a>
<a id="schema_Roles"></a>
<a id="tocSroles"></a>
<a id="tocsroles"></a>

```json
[
  "project_sample:research-assistant"
]

```

### Properties

*None*

<h2 id="tocS_Role">Role</h2>

<a id="schemarole"></a>
<a id="schema_Role"></a>
<a id="tocSrole"></a>
<a id="tocsrole"></a>

```json
"project_sample:research-assistant"

```

A role is either system role or project role.
Researchers must have project roles to access specific project.
- The format of project role is as follow: $project_id:$role_name

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|A role is either system role or project role.<br>Researchers must have project roles to access specific project.<br>- The format of project role is as follow: $project_id:$role_name|

<h2 id="tocS_ForgotPasswordReq">ForgotPasswordReq</h2>

<a id="schemaforgotpasswordreq"></a>
<a id="schema_ForgotPasswordReq"></a>
<a id="tocSforgotpasswordreq"></a>
<a id="tocsforgotpasswordreq"></a>

```json
{
  "email": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|none|

<h2 id="tocS_ResetPasswordReq">ResetPasswordReq</h2>

<a id="schemaresetpasswordreq"></a>
<a id="schema_ResetPasswordReq"></a>
<a id="tocSresetpasswordreq"></a>
<a id="tocsresetpasswordreq"></a>

```json
{
  "resetToken": "aadfad...badfdfad",
  "password": "string",
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|resetToken|string|true|none|none|
|password|string|true|none|none|
|profile|object|false|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_ResetPasswordResponse">ResetPasswordResponse</h2>

<a id="schemaresetpasswordresponse"></a>
<a id="schema_ResetPasswordResponse"></a>
<a id="tocSresetpasswordresponse"></a>
<a id="tocsresetpasswordresponse"></a>

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|id|string|true|none|none|
|jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|refreshToken|string|true|none|none|
|roles|[string]|true|none|none|
|profile|object|true|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_SignInReq">SignInReq</h2>

<a id="schemasigninreq"></a>
<a id="schema_SignInReq"></a>
<a id="tocSsigninreq"></a>
<a id="tocssigninreq"></a>

```json
{
  "email": "cubist@samsung.com",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|password|string|true|none|none|

<h2 id="tocS_SignInResponse">SignInResponse</h2>

<a id="schemasigninresponse"></a>
<a id="schema_SignInResponse"></a>
<a id="tocSsigninresponse"></a>
<a id="tocssigninresponse"></a>

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|id|string|true|none|none|
|jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|refreshToken|string|true|none|none|
|roles|[string]|true|none|none|
|profile|object|true|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_SignUpReq">SignUpReq</h2>

<a id="schemasignupreq"></a>
<a id="schema_SignUpReq"></a>
<a id="tocSsignupreq"></a>
<a id="tocssignupreq"></a>

```json
{
  "email": "cubist@samsung.com",
  "password": "string",
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|password|string|true|none|none|
|profile|object|true|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_RoleReq">RoleReq</h2>

<a id="schemarolereq"></a>
<a id="schema_RoleReq"></a>
<a id="tocSrolereq"></a>
<a id="tocsrolereq"></a>

```json
{
  "accountId": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "roles": [
    "project_sample:research-assistant"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accountId|string|true|none|none|
|roles|[string]|true|none|none|

<h2 id="tocS_RefreshReq">RefreshReq</h2>

<a id="schemarefreshreq"></a>
<a id="schema_RefreshReq"></a>
<a id="tocSrefreshreq"></a>
<a id="tocsrefreshreq"></a>

```json
{
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|refreshToken|string|true|none|none|

<h2 id="tocS_RefreshResponse">RefreshResponse</h2>

<a id="schemarefreshresponse"></a>
<a id="schema_RefreshResponse"></a>
<a id="tocSrefreshresponse"></a>
<a id="tocsrefreshresponse"></a>

```json
{
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|refreshToken|string|true|none|none|

<h2 id="tocS_VerifyEmailReq">VerifyEmailReq</h2>

<a id="schemaverifyemailreq"></a>
<a id="schema_VerifyEmailReq"></a>
<a id="tocSverifyemailreq"></a>
<a id="tocsverifyemailreq"></a>

```json
{
  "token": "aadfad...badfdfad"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|token|string|true|none|none|

<h2 id="tocS_VerifyEmailResponse">VerifyEmailResponse</h2>

<a id="schemaverifyemailresponse"></a>
<a id="schema_VerifyEmailResponse"></a>
<a id="tocSverifyemailresponse"></a>
<a id="tocsverifyemailresponse"></a>

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "jwt": "eyJhbGc...ssw5c",
  "refreshToken": "aadfad...badfdfad",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|id|string|true|none|none|
|jwt|string|true|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|
|refreshToken|string|true|none|none|
|roles|[string]|true|none|none|
|profile|object|true|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_VerificationReq">VerificationReq</h2>

<a id="schemaverificationreq"></a>
<a id="schema_VerificationReq"></a>
<a id="tocSverificationreq"></a>
<a id="tocsverificationreq"></a>

```json
{
  "email": "cubist@samsung.com"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|

<h2 id="tocS_Users">Users</h2>

<a id="schemausers"></a>
<a id="schema_Users"></a>
<a id="tocSusers"></a>
<a id="tocsusers"></a>

```json
[
  {
    "email": "cubist@samsung.com",
    "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
    "roles": [
      "project_sample:research-assistant"
    ],
    "profile": {
      "name": "david.lee",
      "status": "active"
    }
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|id|string|true|none|none|
|roles|[string]|false|none|none|
|profile|object|false|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_User">User</h2>

<a id="schemauser"></a>
<a id="schema_User"></a>
<a id="tocSuser"></a>
<a id="tocsuser"></a>

```json
{
  "email": "cubist@samsung.com",
  "id": "7d08351b-85b6-488e-a8a2-b8653defb865",
  "roles": [
    "project_sample:research-assistant"
  ],
  "profile": {
    "name": "david.lee",
    "status": "active"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|id|string|true|none|none|
|roles|[string]|false|none|none|
|profile|object|false|none|Account information in JSON without pre-defined fields.|

<h2 id="tocS_Profile">Profile</h2>

<a id="schemaprofile"></a>
<a id="schema_Profile"></a>
<a id="tocSprofile"></a>
<a id="tocsprofile"></a>

```json
{
  "name": "david.lee",
  "status": "active"
}

```

Account information in JSON without pre-defined fields.

### Properties

*None*

<h2 id="tocS_Token">Token</h2>

<a id="schematoken"></a>
<a id="schema_Token"></a>
<a id="tocStoken"></a>
<a id="tocstoken"></a>

```json
"eyJhbGc...ssw5c"

```

Signed Json Web Token payload is as below.
{
  "email": "cubist@samsung.com",
  "roles": ["study_1:study-creator", "study_2:research-assistant"],
  "iss": "https://research-hub.io/",
  "exp": 1660377937,
  "iat": 1660291536
}

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|Signed Json Web Token payload is as below.<br>{<br>  "email": "cubist@samsung.com",<br>  "roles": ["study_1:study-creator", "study_2:research-assistant"],<br>  "iss": "https://research-hub.io/",<br>  "exp": 1660377937,<br>  "iat": 1660291536<br>}|

<h2 id="tocS_Email">Email</h2>

<a id="schemaemail"></a>
<a id="schema_Email"></a>
<a id="tocSemail"></a>
<a id="tocsemail"></a>

```json
"cubist@samsung.com"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string(email)|false|none|none|

<h2 id="tocS_AccountId">AccountId</h2>

<a id="schemaaccountid"></a>
<a id="schema_AccountId"></a>
<a id="tocSaccountid"></a>
<a id="tocsaccountid"></a>

```json
"7d08351b-85b6-488e-a8a2-b8653defb865"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_ProjectId">ProjectId</h2>

<a id="schemaprojectid"></a>
<a id="schema_ProjectId"></a>
<a id="tocSprojectid"></a>
<a id="tocsprojectid"></a>

```json
100

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_ResetToken">ResetToken</h2>

<a id="schemaresettoken"></a>
<a id="schema_ResetToken"></a>
<a id="tocSresettoken"></a>
<a id="tocsresettoken"></a>

```json
"aadfad...badfdfad"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_RefreshToken">RefreshToken</h2>

<a id="schemarefreshtoken"></a>
<a id="schema_RefreshToken"></a>
<a id="tocSrefreshtoken"></a>
<a id="tocsrefreshtoken"></a>

```json
"aadfad...badfdfad"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_VerifyEmailToken">VerifyEmailToken</h2>

<a id="schemaverifyemailtoken"></a>
<a id="schema_VerifyEmailToken"></a>
<a id="tocSverifyemailtoken"></a>
<a id="tocsverifyemailtoken"></a>

```json
"aadfad...badfdfad"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_Error">Error</h2>

<a id="schemaerror"></a>
<a id="schema_Error"></a>
<a id="tocSerror"></a>
<a id="tocserror"></a>

```json
{
  "code": "string",
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|none|
|message|string|true|none|none|

