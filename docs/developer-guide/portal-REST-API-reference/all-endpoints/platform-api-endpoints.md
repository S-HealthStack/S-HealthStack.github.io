
# Healthcare Research Platform



<h1 id="healthcare-research-platform">Healthcare Research Platform</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://localhost:3030/api">http://localhost:3030/api</a>

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="healthcare-research-platform-project">Project</h1>

## Retrieve all project lists.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects");
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

`GET /projects`

> Example responses

> 200 Response

```json
[
  {
    "id": {
      "value": 0
    },
    "name": "string",
    "isOpen": true,
    "info": {
      "property1": {},
      "property2": {}
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "deletedAt": "2019-08-24T14:15:22Z"
  }
]
```

<h3 id="retrieve-all-project-lists.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|A list of projects is returned.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-all-project-lists.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Create a new project for healthcare research.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects");
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

`POST /projects`

> Body parameter

```json
{
  "name": "string",
  "isOpen": true,
  "info": {
    "property1": {},
    "property2": {}
  }
}
```

<h3 id="create-a-new-project-for-healthcare-research.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Provide project details.|

> Example responses

> default Response

```json
{
  "code": 0,
  "message": "string"
}
```

<h3 id="create-a-new-project-for-healthcare-research.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Project created successfully.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="create-a-new-project-for-healthcare-research.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve information for a specific project.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}");
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

`GET /projects/{projectId}`

<h3 id="retrieve-information-for-a-specific-project.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|string|true|Provide the id of the project to retrieve.|

> Example responses

> 200 Response

```json
{
  "id": {
    "value": 0
  },
  "name": "string",
  "isOpen": true,
  "info": {
    "property1": {},
    "property2": {}
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "deletedAt": "2019-08-24T14:15:22Z"
}
```

<h3 id="retrieve-information-for-a-specific-project.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Specific project information returned.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-information-for-a-specific-project.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Register a user as a participant of the project.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/users");
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

`POST /projects/{projectId}/users`

> Body parameter

```json
{
  "userId": "1cUoc4KcejOY89f2PzDc9Z8Fyf53",
  "profile": {
    "birth": "1992-02-24",
    "gender": "female"
  }
}
```

<h3 id="register-a-user-as-a-participant-of-the-project.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Provide participant details.|
|projectId|path|string|true|Provide the id of the project for user registration.|
|id-token|header|string|true|Provide the unique user token (generated by firebase).|

> Example responses

> default Response

```json
{
  "code": 0,
  "message": "string"
}
```

<h3 id="register-a-user-as-a-participant-of-the-project.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Participant registered successfully.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="register-a-user-as-a-participant-of-the-project.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Update the profile of the user.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/users/{userId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

`PATCH /projects/{projectId}/users/{userId}`

> Body parameter

```json
{
  "profile": {
    "birth": "1992-02-24",
    "gender": "female"
  }
}
```

<h3 id="update-the-profile-of-the-user.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Provide updated participant details.|
|projectId|path|string|true|Provide the id of the project for user registration.|
|userId|path|string|true|Provide the id of the user to be updated.|
|id-token|header|string|true|Provide the unique user token (generated by firebase).|

> Example responses

> default Response

```json
{
  "code": 0,
  "message": "string"
}
```

<h3 id="update-the-profile-of-the-user.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User profile updated successfully.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="update-the-profile-of-the-user.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve a list of tasks.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/tasks");
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

`GET /projects/{projectId}/tasks`

<h3 id="retrieve-a-list-of-tasks.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|start_time|query|string(date-time)|false|If not provided, retrieves all tasks created after start_time.|
|end_time|query|string(date-time)|false|If not provided, retrieves all tasks created before end_time.|
|last_sync_time|query|string(date-time)|false|(For mobile application) Retrieve tasks that were published after last_sync_time.|
|status|query|string|false|If not provided, retrieves all tasks regardless of status.|
|type|query|string|false|If not provided, retrieves all tasks regardless of type.|
|projectId|path|string|true|Provide the id of the project to retrieve.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|

> Example responses

> 200 Response

```json
[
  {
    "revisionId": 0,
    "id": "string",
    "title": "string",
    "description": "string",
    "schedule": "0 0/1 * 1/1 * ? *",
    "startTime": "2019-08-24T14:15:22Z",
    "endTime": "2019-08-24T14:15:22Z",
    "validTime": 0,
    "status": "DRAFT",
    "type": "SURVEY",
    "items": [
      {
        "name": "string",
        "type": "QUESTION",
        "contents": {
          "title": "string",
          "explanation": "string",
          "required": true,
          "type": "CHOICE",
          "properties": {
            "tag": "RADIO",
            "options": [
              {
                "value": "string",
                "label": "string"
              }
            ],
            "display_logic": {},
            "skip_logic": [
              {
                "condition": "Or contains val4 1 notcontains val4 2",
                "goToAction": null,
                "goToItemSequence": 3
              }
            ]
          }
        },
        "sequence": 0
      }
    ]
  }
]
```

<h3 id="retrieve-a-list-of-tasks.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of tasks retrieved successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-a-list-of-tasks.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» revisionId|integer|true|none|none|
|» id|string|true|none|none|
|» title|string|true|none|none|
|» description|string|false|none|none|
|» schedule|string|false|none|in cronQuartz format|
|» startTime|string(date-time)|false|none|none|
|» endTime|string(date-time)|false|none|If not exists, there's no expiration.|
|» validTime|integer|false|none|Valid time of each task (minute-based).|
|» status|string|true|none|none|
|» type|string|true|none|none|
|» items|[any]|true|none|none|
|»» name|string|true|none|none|
|»» type|string|true|none|Type of Item|
|»» contents|any|true|none|According to the type, it will be changed.|

*oneOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» title|string|true|none|Same with query.|
|»»»» explanation|string|false|none|none|
|»»»» required|boolean|false|none|none|
|»»»» type|string|true|none|none|
|»»»» properties|object|true|none|It depends on the value of 'type'.|

*oneOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»»»» options|[any]|true|none|none|
|»»»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»»»» skip_logic|[any]|false|none|none|
|»»»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» options|[any]|true|none|none|
|»»»»»»» value|string|true|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» low|integer|true|none|Min value of scale.|
|»»»»»» high|integer|true|none|Max value of scale.|
|»»»»»» lowLabel|string|false|none|Label of min value.|
|»»»»»» highLabel|string|false|none|Label of max value.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»»» isRange|boolean|false|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» title|string|false|none|Same with query.|
|»»»» properties|object|false|none|none|
|»»»»» display_logic|object|false|none|Not used in v1.0.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» completionTitle|string|true|none|Title of completion message.|
|»»»» completionDescription|string|false|none|none|
|»»»» required|boolean|false|none|none|
|»»»» type|string|true|none|none|
|»»»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

*continued*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Create a new task.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/tasks");
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

`POST /projects/{projectId}/tasks`

> Body parameter

```json
{
  "type": "SURVEY"
}
```

<h3 id="create-a-new-task.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Provide task details.|
|projectId|path|string|true|Provide the id of the project to retrieve.|

> Example responses

> 201 Response

```json
{
  "revisionId": 0,
  "id": "string"
}
```

<h3 id="create-a-new-task.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Task created successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="create-a-new-task.-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» revisionId|integer|true|none|none|
|» id|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Upload task results.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/tasks");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

`PATCH /projects/{projectId}/tasks`

> Body parameter

```json
[
  {
    "revisionId": 0,
    "taskId": "string",
    "userId": "string",
    "startedAt": "2019-08-24T14:15:22Z",
    "submittedAt": "2019-08-24T14:15:22Z",
    "itemResults": [
      {
        "itemName": "string",
        "result": "string"
      }
    ]
  }
]
```

<h3 id="upload-task-results.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]|true|none|
|projectId|path|string|true|Provide the id of the project to retrieve.|

> Example responses

> default Response

```json
{
  "code": 0,
  "message": "string"
}
```

<h3 id="upload-task-results.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Task results uploaded successfully.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="upload-task-results.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve tasks with a specific task_id.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/tasks/{taskId}");
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

`GET /projects/{projectId}/tasks/{taskId}`

<h3 id="retrieve-tasks-with-a-specific-task_id.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|string|true|Provide the id of the project to retrieve.|
|taskId|path|string|true|Provide the id of the task.|

> Example responses

> 200 Response

```json
[
  {
    "revisionId": 0,
    "id": "string",
    "title": "string",
    "description": "string",
    "schedule": "0 0/1 * 1/1 * ? *",
    "startTime": "2019-08-24T14:15:22Z",
    "endTime": "2019-08-24T14:15:22Z",
    "validTime": 0,
    "status": "DRAFT",
    "type": "SURVEY",
    "items": [
      {
        "name": "string",
        "type": "QUESTION",
        "contents": {
          "title": "string",
          "explanation": "string",
          "required": true,
          "type": "CHOICE",
          "properties": {
            "tag": "RADIO",
            "options": [
              {
                "value": "string",
                "label": "string"
              }
            ],
            "display_logic": {},
            "skip_logic": [
              {
                "condition": "Or contains val4 1 notcontains val4 2",
                "goToAction": null,
                "goToItemSequence": 3
              }
            ]
          }
        },
        "sequence": 0
      }
    ]
  }
]
```

<h3 id="retrieve-tasks-with-a-specific-task_id.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Task details retrieved successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-tasks-with-a-specific-task_id.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» revisionId|integer|true|none|none|
|» id|string|true|none|none|
|» title|string|true|none|none|
|» description|string|false|none|none|
|» schedule|string|false|none|in cronQuartz format|
|» startTime|string(date-time)|false|none|none|
|» endTime|string(date-time)|false|none|If not exists, there's no expiration.|
|» validTime|integer|false|none|Valid time of each task (minute-based).|
|» status|string|true|none|none|
|» type|string|true|none|none|
|» items|[any]|true|none|none|
|»» name|string|true|none|none|
|»» type|string|true|none|Type of Item|
|»» contents|any|true|none|According to the type, it will be changed.|

*oneOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» title|string|true|none|Same with query.|
|»»»» explanation|string|false|none|none|
|»»»» required|boolean|false|none|none|
|»»»» type|string|true|none|none|
|»»»» properties|object|true|none|It depends on the value of 'type'.|

*oneOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»»»» options|[any]|true|none|none|
|»»»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»»»» skip_logic|[any]|false|none|none|
|»»»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» options|[any]|true|none|none|
|»»»»»»» value|string|true|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» low|integer|true|none|Min value of scale.|
|»»»»»» high|integer|true|none|Max value of scale.|
|»»»»»» lowLabel|string|false|none|Label of min value.|
|»»»»»» highLabel|string|false|none|Label of max value.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»»» *anonymous*|object|false|none|none|
|»»»»»» tag|string|true|none|none|
|»»»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»»» isRange|boolean|false|none|none|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» title|string|false|none|Same with query.|
|»»»» properties|object|false|none|none|
|»»»»» display_logic|object|false|none|Not used in v1.0.|

*xor*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» completionTitle|string|true|none|Title of completion message.|
|»»»» completionDescription|string|false|none|none|
|»»»» required|boolean|false|none|none|
|»»»» type|string|true|none|none|
|»»»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

*continued*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Update a specific task.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/tasks/{taskId}?revision_id=0");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

`PATCH /projects/{projectId}/tasks/{taskId}`

Only tasks in DRAFT status can be updated. This is intended for auto-save or status changes.

> Body parameter

```json
{
  "title": "string",
  "description": "string",
  "schedule": "0 0/1 * 1/1 * ? *",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "validTime": 0,
  "status": "DRAFT",
  "type": "SURVEY",
  "items": [
    {
      "type": "QUESTION",
      "contents": {
        "title": "string",
        "explanation": "string",
        "required": true,
        "type": "CHOICE",
        "properties": {
          "tag": "RADIO",
          "options": [
            {
              "value": "string",
              "label": "string"
            }
          ],
          "display_logic": {},
          "skip_logic": [
            {
              "condition": "Or contains val4 1 notcontains val4 2",
              "goToAction": null,
              "goToItemSequence": 3
            }
          ]
        }
      },
      "sequence": 0
    }
  ]
}
```

<h3 id="update-a-specific-task.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|revision_id|query|integer|true|none|
|body|body|object|true|none|
|projectId|path|string|true|Provide the id of the project to retrieve.|
|taskId|path|string|true|Provide the id of the task.|

> Example responses

> default Response

```json
{
  "code": 0,
  "message": "string"
}
```

<h3 id="update-a-specific-task.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Task updated successfully.|None|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="update-a-specific-task.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Create in-lab visit data.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/in-lab-visits");
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

`POST /projects/{projectId}/in-lab-visits`

> Body parameter

```json
{
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string"
}
```

<h3 id="create-in-lab-visit-data.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|projectId|path|string|true|Provide the id of the project to retrieve.|

> Example responses

> 201 Response

```json
{
  "id": 0,
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string",
  "filesPath": "in-lab-visit/u1234"
}
```

<h3 id="create-in-lab-visit-data.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|In-lab visit data created successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="create-in-lab-visit-data.-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|true|none|none|
|» userId|string|true|none|none|
|» checkedInBy|string|true|none|none|
|» startTime|string(date-time)|true|none|none|
|» endTime|string(date-time)|true|none|none|
|» notes|string|true|none|none|
|» filesPath|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve a list of in-lab visits.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/in-lab-visits");
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

`GET /projects/{projectId}/in-lab-visits`

<h3 id="retrieve-a-list-of-in-lab-visits.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|string|true|Provide the id of the project to retrieve.|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "userId": "string",
    "checkedInBy": "string",
    "startTime": "2019-08-24T14:15:22Z",
    "endTime": "2019-08-24T14:15:22Z",
    "notes": "string",
    "filesPath": "in-lab-visit/u1234"
  }
]
```

<h3 id="retrieve-a-list-of-in-lab-visits.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of in-lab visits retrieved successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-a-list-of-in-lab-visits.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|true|none|none|
|» userId|string|true|none|none|
|» checkedInBy|string|true|none|none|
|» startTime|string(date-time)|true|none|none|
|» endTime|string(date-time)|true|none|none|
|» notes|string|true|none|none|
|» filesPath|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve in-lab visits with a specific inLabVisitId.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/in-lab-visits/{inLabVisitId}");
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

`GET /projects/{projectId}/in-lab-visits/{inLabVisitId}`

<h3 id="retrieve-in-lab-visits-with-a-specific-inlabvisitid.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|string|true|Provide the id of the project to retrieve.|
|inLabVisitId|path|string|true|Provide the id of the in-lab visit data.|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string",
  "filesPath": "in-lab-visit/u1234"
}
```

<h3 id="retrieve-in-lab-visits-with-a-specific-inlabvisitid.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|In-lab visit data retrieved successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="retrieve-in-lab-visits-with-a-specific-inlabvisitid.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|true|none|none|
|» userId|string|true|none|none|
|» checkedInBy|string|true|none|none|
|» startTime|string(date-time)|true|none|none|
|» endTime|string(date-time)|true|none|none|
|» notes|string|true|none|none|
|» filesPath|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Update in-lab visit data with a specific inLabVisitId.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/in-lab-visits/{inLabVisitId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

`PATCH /projects/{projectId}/in-lab-visits/{inLabVisitId}`

> Body parameter

```json
{
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string"
}
```

<h3 id="update-in-lab-visit-data-with-a-specific-inlabvisitid.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|projectId|path|string|true|Provide the id of the project to retrieve.|
|inLabVisitId|path|string|true|Provide the id of the in-lab visit data.|

> Example responses

> 200 Response

```json
{
  "id": 0,
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string",
  "filesPath": "in-lab-visit/u1234"
}
```

<h3 id="update-in-lab-visit-data-with-a-specific-inlabvisitid.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|In-lab visit data updated successfully.|Inline|
|default|Default|An unexpected error has occurred.|Inline|

<h3 id="update-in-lab-visit-data-with-a-specific-inlabvisitid.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|true|none|none|
|» userId|string|true|none|none|
|» checkedInBy|string|true|none|none|
|» startTime|string(date-time)|true|none|none|
|» endTime|string(date-time)|true|none|none|
|» notes|string|true|none|none|
|» filesPath|string|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer(int32)|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

# Schemas

<h2 id="tocS_Id">Id</h2>

<a id="schemaid"></a>
<a id="schema_Id"></a>
<a id="tocSid"></a>
<a id="tocsid"></a>

```json
{
  "value": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|value|integer|true|none|none|

<h2 id="tocS_BaseTime">BaseTime</h2>

<a id="schemabasetime"></a>
<a id="schema_BaseTime"></a>
<a id="tocSbasetime"></a>
<a id="tocsbasetime"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "deletedAt": "2019-08-24T14:15:22Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|createdAt|string(date-time)|false|none|none|
|deletedAt|string(date-time)|false|none|none|

<h2 id="tocS_Project">Project</h2>

<a id="schemaproject"></a>
<a id="schema_Project"></a>
<a id="tocSproject"></a>
<a id="tocsproject"></a>

```json
{
  "name": "string",
  "isOpen": true,
  "info": {
    "property1": {},
    "property2": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|isOpen|boolean|false|none|none|
|info|object|false|none|none|
|» **additionalProperties**|object|false|none|none|

<h2 id="tocS_ProjectRes">ProjectRes</h2>

<a id="schemaprojectres"></a>
<a id="schema_ProjectRes"></a>
<a id="tocSprojectres"></a>
<a id="tocsprojectres"></a>

```json
{
  "id": {
    "value": 0
  },
  "name": "string",
  "isOpen": true,
  "info": {
    "property1": {},
    "property2": {}
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "deletedAt": "2019-08-24T14:15:22Z"
}

```

### Properties

allOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» id|object|false|none|none|
|»» value|integer|true|none|none|

and

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» name|string|true|none|none|
|» isOpen|boolean|false|none|none|
|» info|object|false|none|none|
|»» **additionalProperties**|object|false|none|none|

and

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» createdAt|string(date-time)|false|none|none|
|» deletedAt|string(date-time)|false|none|none|

<h2 id="tocS_ProjectsRes">ProjectsRes</h2>

<a id="schemaprojectsres"></a>
<a id="schema_ProjectsRes"></a>
<a id="tocSprojectsres"></a>
<a id="tocsprojectsres"></a>

```json
[
  {
    "id": {
      "value": 0
    },
    "name": "string",
    "isOpen": true,
    "info": {
      "property1": {},
      "property2": {}
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "deletedAt": "2019-08-24T14:15:22Z"
  }
]

```

### Properties

allOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» id|object|false|none|none|
|»» value|integer|true|none|none|

and

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» name|string|true|none|none|
|» isOpen|boolean|false|none|none|
|» info|object|false|none|none|
|»» **additionalProperties**|object|false|none|none|

and

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» createdAt|string(date-time)|false|none|none|
|» deletedAt|string(date-time)|false|none|none|

<h2 id="tocS_Projects">Projects</h2>

<a id="schemaprojects"></a>
<a id="schema_Projects"></a>
<a id="tocSprojects"></a>
<a id="tocsprojects"></a>

```json
[
  {
    "name": "string",
    "isOpen": true,
    "info": {
      "property1": {},
      "property2": {}
    }
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|isOpen|boolean|false|none|none|
|info|object|false|none|none|
|» **additionalProperties**|object|false|none|none|

<h2 id="tocS_Participant">Participant</h2>

<a id="schemaparticipant"></a>
<a id="schema_Participant"></a>
<a id="tocSparticipant"></a>
<a id="tocsparticipant"></a>

```json
{
  "userId": "1cUoc4KcejOY89f2PzDc9Z8Fyf53",
  "profile": {
    "birth": "1992-02-24",
    "gender": "female"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userId|string|true|none|Unique id of user (generated by Firebase).|
|profile|object|false|none|Participant information in JSON with no pre-defined fields.|

<h2 id="tocS_ParticipantUpdate">ParticipantUpdate</h2>

<a id="schemaparticipantupdate"></a>
<a id="schema_ParticipantUpdate"></a>
<a id="tocSparticipantupdate"></a>
<a id="tocsparticipantupdate"></a>

```json
{
  "profile": {
    "birth": "1992-02-24",
    "gender": "female"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|profile|object|true|none|Participant information in JSON with no pre-defined fields.|

<h2 id="tocS_Participants">Participants</h2>

<a id="schemaparticipants"></a>
<a id="schema_Participants"></a>
<a id="tocSparticipants"></a>
<a id="tocsparticipants"></a>

```json
[
  {
    "userId": "1cUoc4KcejOY89f2PzDc9Z8Fyf53",
    "profile": {
      "birth": "1992-02-24",
      "gender": "female"
    }
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userId|string|true|none|Unique id of user (generated by Firebase).|
|profile|object|false|none|Participant information in JSON with no pre-defined fields.|

<h2 id="tocS_TextQuestion">TextQuestion</h2>

<a id="schematextquestion"></a>
<a id="schema_TextQuestion"></a>
<a id="tocStextquestion"></a>
<a id="tocstextquestion"></a>

```json
{
  "tag": "TEXT"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tag|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|tag|TEXT|

<h2 id="tocS_ChoiceQuestion">ChoiceQuestion</h2>

<a id="schemachoicequestion"></a>
<a id="schema_ChoiceQuestion"></a>
<a id="tocSchoicequestion"></a>
<a id="tocschoicequestion"></a>

```json
{
  "tag": "RADIO",
  "options": [
    {
      "value": "string",
      "label": "string"
    }
  ],
  "display_logic": {},
  "skip_logic": [
    {
      "condition": "Or contains val4 1 notcontains val4 2",
      "goToAction": null,
      "goToItemSequence": 3
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|options|[any]|true|none|none|
|» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|display_logic|object|false|none|Not used in v1.0.|
|skip_logic|[any]|false|none|none|
|» condition|string|false|none|Expression that match BranchRule.|
|» goToAction|string|false|none|Not used in v1.0.|
|» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

#### Enumerated Values

|Property|Value|
|---|---|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|

<h2 id="tocS_RankQuestion">RankQuestion</h2>

<a id="schemarankquestion"></a>
<a id="schema_RankQuestion"></a>
<a id="tocSrankquestion"></a>
<a id="tocsrankquestion"></a>

```json
{
  "tag": "RANK",
  "options": [
    {
      "value": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tag|string|true|none|none|
|options|[any]|true|none|none|
|» value|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|tag|RANK|

<h2 id="tocS_ScaleQuestion">ScaleQuestion</h2>

<a id="schemascalequestion"></a>
<a id="schema_ScaleQuestion"></a>
<a id="tocSscalequestion"></a>
<a id="tocsscalequestion"></a>

```json
{
  "tag": "SLIDER",
  "low": 0,
  "high": 0,
  "lowLabel": "Somewhat disagree.",
  "highLabel": "Strongly agree"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tag|string|true|none|none|
|low|integer|true|none|Min value of scale.|
|high|integer|true|none|Max value of scale.|
|lowLabel|string|false|none|Label of min value.|
|highLabel|string|false|none|Label of max value.|

#### Enumerated Values

|Property|Value|
|---|---|
|tag|SLIDER|

<h2 id="tocS_DateTimeQuestion">DateTimeQuestion</h2>

<a id="schemadatetimequestion"></a>
<a id="schema_DateTimeQuestion"></a>
<a id="tocSdatetimequestion"></a>
<a id="tocsdatetimequestion"></a>

```json
{
  "tag": "DATETIME",
  "isTime": true,
  "isDate": true,
  "isRange": false
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|tag|string|true|none|none|
|isTime|boolean|false|none|Either isTime or isDate has to be true.|
|isDate|boolean|false|none|Either isTime or isDate has to be true.|
|isRange|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|tag|DATETIME|

<h2 id="tocS_Question">Question</h2>

<a id="schemaquestion"></a>
<a id="schema_Question"></a>
<a id="tocSquestion"></a>
<a id="tocsquestion"></a>

```json
{
  "title": "string",
  "explanation": "string",
  "required": true,
  "type": "CHOICE",
  "properties": {
    "tag": "RADIO",
    "options": [
      {
        "value": "string",
        "label": "string"
      }
    ],
    "display_logic": {},
    "skip_logic": [
      {
        "condition": "Or contains val4 1 notcontains val4 2",
        "goToAction": null,
        "goToItemSequence": 3
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|title|string|true|none|Same with query.|
|explanation|string|false|none|none|
|required|boolean|false|none|none|
|type|string|true|none|none|
|properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»» options|[any]|true|none|none|
|»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»» display_logic|object|false|none|Not used in v1.0.|
|»» skip_logic|[any]|false|none|none|
|»»» condition|string|false|none|Expression that match BranchRule.|
|»»» goToAction|string|false|none|Not used in v1.0.|
|»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» tag|string|true|none|none|
|»» options|[any]|true|none|none|
|»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» tag|string|true|none|none|
|»» low|integer|true|none|Min value of scale.|
|»» high|integer|true|none|Max value of scale.|
|»» lowLabel|string|false|none|Label of min value.|
|»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» tag|string|true|none|none|
|»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»» isRange|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|

<h2 id="tocS_Section">Section</h2>

<a id="schemasection"></a>
<a id="schema_Section"></a>
<a id="tocSsection"></a>
<a id="tocssection"></a>

```json
{
  "title": "string",
  "properties": {
    "display_logic": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|title|string|false|none|Same with query.|
|properties|object|false|none|none|
|» display_logic|object|false|none|Not used in v1.0.|

<h2 id="tocS_Activity">Activity</h2>

<a id="schemaactivity"></a>
<a id="schema_Activity"></a>
<a id="tocSactivity"></a>
<a id="tocsactivity"></a>

```json
{
  "completionTitle": "string",
  "completionDescription": "string",
  "required": true,
  "type": "TAPPING_SPEED",
  "properties": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|completionTitle|string|true|none|Title of completion message.|
|completionDescription|string|false|none|none|
|required|boolean|false|none|none|
|type|string|true|none|none|
|properties|object|false|none|Field for configurable values. This is not used for v1.0.|

#### Enumerated Values

|Property|Value|
|---|---|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_Item">Item</h2>

<a id="schemaitem"></a>
<a id="schema_Item"></a>
<a id="tocSitem"></a>
<a id="tocsitem"></a>

```json
{
  "name": "string",
  "type": "QUESTION",
  "contents": {
    "title": "string",
    "explanation": "string",
    "required": true,
    "type": "CHOICE",
    "properties": {
      "tag": "RADIO",
      "options": [
        {
          "value": "string",
          "label": "string"
        }
      ],
      "display_logic": {},
      "skip_logic": [
        {
          "condition": "Or contains val4 1 notcontains val4 2",
          "goToAction": null,
          "goToItemSequence": 3
        }
      ]
    }
  },
  "sequence": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|type|string|true|none|Type of Item|
|contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|true|none|Same with query.|
|»» explanation|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»» skip_logic|[any]|false|none|none|
|»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» low|integer|true|none|Min value of scale.|
|»»»» high|integer|true|none|Max value of scale.|
|»»»» lowLabel|string|false|none|Label of min value.|
|»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|false|none|Same with query.|
|»» properties|object|false|none|none|
|»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» completionTitle|string|true|none|Title of completion message.|
|»» completionDescription|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_Items">Items</h2>

<a id="schemaitems"></a>
<a id="schema_Items"></a>
<a id="tocSitems"></a>
<a id="tocsitems"></a>

```json
[
  {
    "name": "string",
    "type": "QUESTION",
    "contents": {
      "title": "string",
      "explanation": "string",
      "required": true,
      "type": "CHOICE",
      "properties": {
        "tag": "RADIO",
        "options": [
          {
            "value": "string",
            "label": "string"
          }
        ],
        "display_logic": {},
        "skip_logic": [
          {
            "condition": "Or contains val4 1 notcontains val4 2",
            "goToAction": null,
            "goToItemSequence": 3
          }
        ]
      }
    },
    "sequence": 0
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|type|string|true|none|Type of Item|
|contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|true|none|Same with query.|
|»» explanation|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»» skip_logic|[any]|false|none|none|
|»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» low|integer|true|none|Min value of scale.|
|»»»» high|integer|true|none|Max value of scale.|
|»»»» lowLabel|string|false|none|Label of min value.|
|»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|false|none|Same with query.|
|»» properties|object|false|none|none|
|»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» completionTitle|string|true|none|Title of completion message.|
|»» completionDescription|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_ItemReq">ItemReq</h2>

<a id="schemaitemreq"></a>
<a id="schema_ItemReq"></a>
<a id="tocSitemreq"></a>
<a id="tocsitemreq"></a>

```json
{
  "type": "QUESTION",
  "contents": {
    "title": "string",
    "explanation": "string",
    "required": true,
    "type": "CHOICE",
    "properties": {
      "tag": "RADIO",
      "options": [
        {
          "value": "string",
          "label": "string"
        }
      ],
      "display_logic": {},
      "skip_logic": [
        {
          "condition": "Or contains val4 1 notcontains val4 2",
          "goToAction": null,
          "goToItemSequence": 3
        }
      ]
    }
  },
  "sequence": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|Type of Item|
|contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|true|none|Same with query.|
|»» explanation|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»» skip_logic|[any]|false|none|none|
|»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» low|integer|true|none|Min value of scale.|
|»»»» high|integer|true|none|Max value of scale.|
|»»»» lowLabel|string|false|none|Label of min value.|
|»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|false|none|Same with query.|
|»» properties|object|false|none|none|
|»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» completionTitle|string|true|none|Title of completion message.|
|»» completionDescription|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_ItemsReq">ItemsReq</h2>

<a id="schemaitemsreq"></a>
<a id="schema_ItemsReq"></a>
<a id="tocSitemsreq"></a>
<a id="tocsitemsreq"></a>

```json
[
  {
    "type": "QUESTION",
    "contents": {
      "title": "string",
      "explanation": "string",
      "required": true,
      "type": "CHOICE",
      "properties": {
        "tag": "RADIO",
        "options": [
          {
            "value": "string",
            "label": "string"
          }
        ],
        "display_logic": {},
        "skip_logic": [
          {
            "condition": "Or contains val4 1 notcontains val4 2",
            "goToAction": null,
            "goToItemSequence": 3
          }
        ]
      }
    },
    "sequence": 0
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|Type of Item|
|contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|true|none|Same with query.|
|»» explanation|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»» skip_logic|[any]|false|none|none|
|»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» options|[any]|true|none|none|
|»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» low|integer|true|none|Min value of scale.|
|»»»» high|integer|true|none|Max value of scale.|
|»»»» lowLabel|string|false|none|Label of min value.|
|»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»» *anonymous*|object|false|none|none|
|»»»» tag|string|true|none|none|
|»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» title|string|false|none|Same with query.|
|»» properties|object|false|none|none|
|»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|object|false|none|none|
|»» completionTitle|string|true|none|Title of completion message.|
|»» completionDescription|string|false|none|none|
|»» required|boolean|false|none|none|
|»» type|string|true|none|none|
|»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_TaskId">TaskId</h2>

<a id="schemataskid"></a>
<a id="schema_TaskId"></a>
<a id="tocStaskid"></a>
<a id="tocstaskid"></a>

```json
{
  "revisionId": 0,
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|revisionId|integer|true|none|none|
|id|string|true|none|none|

<h2 id="tocS_TaskType">TaskType</h2>

<a id="schematasktype"></a>
<a id="schema_TaskType"></a>
<a id="tocStasktype"></a>
<a id="tocstasktype"></a>

```json
{
  "type": "SURVEY"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|SURVEY|
|type|ACTIVITY|

<h2 id="tocS_Task">Task</h2>

<a id="schematask"></a>
<a id="schema_Task"></a>
<a id="tocStask"></a>
<a id="tocstask"></a>

```json
{
  "revisionId": 0,
  "id": "string",
  "title": "string",
  "description": "string",
  "schedule": "0 0/1 * 1/1 * ? *",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "validTime": 0,
  "status": "DRAFT",
  "type": "SURVEY",
  "items": [
    {
      "name": "string",
      "type": "QUESTION",
      "contents": {
        "title": "string",
        "explanation": "string",
        "required": true,
        "type": "CHOICE",
        "properties": {
          "tag": "RADIO",
          "options": [
            {
              "value": "string",
              "label": "string"
            }
          ],
          "display_logic": {},
          "skip_logic": [
            {
              "condition": "Or contains val4 1 notcontains val4 2",
              "goToAction": null,
              "goToItemSequence": 3
            }
          ]
        }
      },
      "sequence": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|revisionId|integer|true|none|none|
|id|string|true|none|none|
|title|string|true|none|none|
|description|string|false|none|none|
|schedule|string|false|none|in cronQuartz format|
|startTime|string(date-time)|false|none|none|
|endTime|string(date-time)|false|none|If not exists, there's no expiration.|
|validTime|integer|false|none|Valid time of each task (minute-based).|
|status|string|true|none|none|
|type|string|true|none|none|
|items|[any]|true|none|none|
|» name|string|true|none|none|
|» type|string|true|none|Type of Item|
|» contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|true|none|Same with query.|
|»»» explanation|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»»» skip_logic|[any]|false|none|none|
|»»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» low|integer|true|none|Min value of scale.|
|»»»»» high|integer|true|none|Max value of scale.|
|»»»»» lowLabel|string|false|none|Label of min value.|
|»»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|false|none|Same with query.|
|»»» properties|object|false|none|none|
|»»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» completionTitle|string|true|none|Title of completion message.|
|»»» completionDescription|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_TaskReq">TaskReq</h2>

<a id="schemataskreq"></a>
<a id="schema_TaskReq"></a>
<a id="tocStaskreq"></a>
<a id="tocstaskreq"></a>

```json
{
  "title": "string",
  "description": "string",
  "schedule": "0 0/1 * 1/1 * ? *",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "validTime": 0,
  "status": "DRAFT",
  "type": "SURVEY",
  "items": [
    {
      "type": "QUESTION",
      "contents": {
        "title": "string",
        "explanation": "string",
        "required": true,
        "type": "CHOICE",
        "properties": {
          "tag": "RADIO",
          "options": [
            {
              "value": "string",
              "label": "string"
            }
          ],
          "display_logic": {},
          "skip_logic": [
            {
              "condition": "Or contains val4 1 notcontains val4 2",
              "goToAction": null,
              "goToItemSequence": 3
            }
          ]
        }
      },
      "sequence": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|title|string|true|none|none|
|description|string|false|none|none|
|schedule|string|false|none|cronQuartz format. This is required if status is PUBLISHED.|
|startTime|string(date-time)|false|none|This is required if status is PUBLISHED.|
|endTime|string(date-time)|false|none|If not exists, there's no expiration.|
|validTime|integer|false|none|Valid time of each task (minute-based). This is required if status is PUBLISHED.|
|status|string|true|none|none|
|type|string|true|none|none|
|items|[any]|true|none|none|
|» type|string|true|none|Type of Item|
|» contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|true|none|Same with query.|
|»»» explanation|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»»» skip_logic|[any]|false|none|none|
|»»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» low|integer|true|none|Min value of scale.|
|»»»»» high|integer|true|none|Max value of scale.|
|»»»»» lowLabel|string|false|none|Label of min value.|
|»»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|false|none|Same with query.|
|»»» properties|object|false|none|none|
|»»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» completionTitle|string|true|none|Title of completion message.|
|»»» completionDescription|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_Tasks">Tasks</h2>

<a id="schematasks"></a>
<a id="schema_Tasks"></a>
<a id="tocStasks"></a>
<a id="tocstasks"></a>

```json
[
  {
    "revisionId": 0,
    "id": "string",
    "title": "string",
    "description": "string",
    "schedule": "0 0/1 * 1/1 * ? *",
    "startTime": "2019-08-24T14:15:22Z",
    "endTime": "2019-08-24T14:15:22Z",
    "validTime": 0,
    "status": "DRAFT",
    "type": "SURVEY",
    "items": [
      {
        "name": "string",
        "type": "QUESTION",
        "contents": {
          "title": "string",
          "explanation": "string",
          "required": true,
          "type": "CHOICE",
          "properties": {
            "tag": "RADIO",
            "options": [
              {
                "value": "string",
                "label": "string"
              }
            ],
            "display_logic": {},
            "skip_logic": [
              {
                "condition": "Or contains val4 1 notcontains val4 2",
                "goToAction": null,
                "goToItemSequence": 3
              }
            ]
          }
        },
        "sequence": 0
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|revisionId|integer|true|none|none|
|id|string|true|none|none|
|title|string|true|none|none|
|description|string|false|none|none|
|schedule|string|false|none|in cronQuartz format|
|startTime|string(date-time)|false|none|none|
|endTime|string(date-time)|false|none|If not exists, there's no expiration.|
|validTime|integer|false|none|Valid time of each task (minute-based).|
|status|string|true|none|none|
|type|string|true|none|none|
|items|[any]|true|none|none|
|» name|string|true|none|none|
|» type|string|true|none|Type of Item|
|» contents|any|true|none|According to the type, it will be changed.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|true|none|Same with query.|
|»»» explanation|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|true|none|It depends on the value of 'type'.|

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|Only one option can be chosen for radio, dropdown, image. Multiple options can be chosen for checkbox, multi-image.|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|For Image Question, you have to put link of Image in this field.|
|»»»»»» label|string|false|none|This field can be used when type is IMAGE to generate Image Question with label. Also, if you want to create Image Question with label, all options have to include their own labels.|
|»»»»» display_logic|object|false|none|Not used in v1.0.|
|»»»»» skip_logic|[any]|false|none|none|
|»»»»»» condition|string|false|none|Expression that match BranchRule.|
|»»»»»» goToAction|string|false|none|Not used in v1.0.|
|»»»»»» goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» options|[any]|true|none|none|
|»»»»»» value|string|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» low|integer|true|none|Min value of scale.|
|»»»»» high|integer|true|none|Max value of scale.|
|»»»»» lowLabel|string|false|none|Label of min value.|
|»»»»» highLabel|string|false|none|Label of max value.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»»»» *anonymous*|object|false|none|none|
|»»»»» tag|string|true|none|none|
|»»»»» isTime|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isDate|boolean|false|none|Either isTime or isDate has to be true.|
|»»»»» isRange|boolean|false|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» title|string|false|none|Same with query.|
|»»» properties|object|false|none|none|
|»»»» display_logic|object|false|none|Not used in v1.0.|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|»» *anonymous*|object|false|none|none|
|»»» completionTitle|string|true|none|Title of completion message.|
|»»» completionDescription|string|false|none|none|
|»»» required|boolean|false|none|none|
|»»» type|string|true|none|none|
|»»» properties|object|false|none|Field for configurable values. This is not used for v1.0.|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» sequence|integer|true|none|Sequence of this item in a task.|

#### Enumerated Values

|Property|Value|
|---|---|
|status|DRAFT|
|status|PUBLISHED|
|type|SURVEY|
|type|ACTIVITY|
|type|QUESTION|
|type|SECTION|
|type|ACTIVITY|
|type|CHOICE|
|type|TEXT|
|type|RANK|
|type|SCALE|
|type|DATETIME|
|tag|RADIO|
|tag|CHECKBOX|
|tag|DROPDOWN|
|tag|MULTIIMAGE|
|tag|IMAGE|
|tag|TEXT|
|tag|RANK|
|tag|SLIDER|
|tag|DATETIME|
|type|TAPPING_SPEED|
|type|REACTION_TIME|
|type|RANGE_OF_MOTION|
|type|GAIT_AND_BALANCE|
|type|GUIDED_BREATHING|
|type|STROOP_TEST|
|type|SPEECH_RECOGNITION|
|type|MOBILE_SPIROMETRY|
|type|SUSTAINED_PHONATION|

<h2 id="tocS_TaskResult">TaskResult</h2>

<a id="schemataskresult"></a>
<a id="schema_TaskResult"></a>
<a id="tocStaskresult"></a>
<a id="tocstaskresult"></a>

```json
{
  "revisionId": 0,
  "taskId": "string",
  "userId": "string",
  "startedAt": "2019-08-24T14:15:22Z",
  "submittedAt": "2019-08-24T14:15:22Z",
  "itemResults": [
    {
      "itemName": "string",
      "result": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|revisionId|integer|false|none|none|
|taskId|string|false|none|none|
|userId|string|false|none|none|
|startedAt|string(date-time)|false|none|none|
|submittedAt|string(date-time)|false|none|none|
|itemResults|[any]|false|none|none|
|» itemName|string|false|none|none|
|» result|string|false|none|none|

<h2 id="tocS_TaskResults">TaskResults</h2>

<a id="schemataskresults"></a>
<a id="schema_TaskResults"></a>
<a id="tocStaskresults"></a>
<a id="tocstaskresults"></a>

```json
[
  {
    "revisionId": 0,
    "taskId": "string",
    "userId": "string",
    "startedAt": "2019-08-24T14:15:22Z",
    "submittedAt": "2019-08-24T14:15:22Z",
    "itemResults": [
      {
        "itemName": "string",
        "result": "string"
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|revisionId|integer|false|none|none|
|taskId|string|false|none|none|
|userId|string|false|none|none|
|startedAt|string(date-time)|false|none|none|
|submittedAt|string(date-time)|false|none|none|
|itemResults|[any]|false|none|none|
|» itemName|string|false|none|none|
|» result|string|false|none|none|

<h2 id="tocS_ItemResult">ItemResult</h2>

<a id="schemaitemresult"></a>
<a id="schema_ItemResult"></a>
<a id="tocSitemresult"></a>
<a id="tocsitemresult"></a>

```json
{
  "itemName": "string",
  "result": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemName|string|false|none|none|
|result|string|false|none|none|

<h2 id="tocS_SkipLogic">SkipLogic</h2>

<a id="schemaskiplogic"></a>
<a id="schema_SkipLogic"></a>
<a id="tocSskiplogic"></a>
<a id="tocsskiplogic"></a>

```json
{
  "condition": "Or contains val4 1 notcontains val4 2",
  "goToAction": null,
  "goToItemSequence": 3
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|condition|string|false|none|Expression that match BranchRule.|
|goToAction|string|false|none|Not used in v1.0.|
|goToItemSequence|integer|false|none|If condition holds, then skip to sequence $goToItemSequence.|

<h2 id="tocS_InLabVisitReq">InLabVisitReq</h2>

<a id="schemainlabvisitreq"></a>
<a id="schema_InLabVisitReq"></a>
<a id="tocSinlabvisitreq"></a>
<a id="tocsinlabvisitreq"></a>

```json
{
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userId|string|true|none|none|
|checkedInBy|string|true|none|none|
|startTime|string(date-time)|true|none|none|
|endTime|string(date-time)|true|none|none|
|notes|string|false|none|none|

<h2 id="tocS_InLabVisitUpdateReq">InLabVisitUpdateReq</h2>

<a id="schemainlabvisitupdatereq"></a>
<a id="schema_InLabVisitUpdateReq"></a>
<a id="tocSinlabvisitupdatereq"></a>
<a id="tocsinlabvisitupdatereq"></a>

```json
{
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userId|string|true|none|none|
|checkedInBy|string|true|none|none|
|startTime|string(date-time)|true|none|none|
|endTime|string(date-time)|true|none|none|
|notes|string|false|none|none|

<h2 id="tocS_InLabVisitRes">InLabVisitRes</h2>

<a id="schemainlabvisitres"></a>
<a id="schema_InLabVisitRes"></a>
<a id="tocSinlabvisitres"></a>
<a id="tocsinlabvisitres"></a>

```json
{
  "id": 0,
  "userId": "string",
  "checkedInBy": "string",
  "startTime": "2019-08-24T14:15:22Z",
  "endTime": "2019-08-24T14:15:22Z",
  "notes": "string",
  "filesPath": "in-lab-visit/u1234"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|true|none|none|
|userId|string|true|none|none|
|checkedInBy|string|true|none|none|
|startTime|string(date-time)|true|none|none|
|endTime|string(date-time)|true|none|none|
|notes|string|true|none|none|
|filesPath|string|true|none|none|

<h2 id="tocS_Error">Error</h2>

<a id="schemaerror"></a>
<a id="schema_Error"></a>
<a id="tocSerror"></a>
<a id="tocserror"></a>

```json
{
  "code": 0,
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|true|none|none|
|message|string|true|none|none|

