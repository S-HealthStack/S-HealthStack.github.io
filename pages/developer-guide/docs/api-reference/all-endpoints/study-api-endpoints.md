---


title: Study API Endpoints
sidebar: dev_doc_sidebar
permalink: study-api-endpoints.html
toc: false


---


## Version: 0.9

You can also find more interactive document here: [SwaggerHub-Study_API/0.9.0](https://app.swaggerhub.com/apis-docs/zainalisamsung/Study_API/0.9.0)

### /projects

#### GET
##### Summary

Get all project lists.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | List of projects |
| default | Unexpected Error |

#### POST
##### Summary

Create a new study project for healthcare research.

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Null response |
| default | unexpected error |

### /projects/{projectId}

#### GET
##### Summary

Info for a specific project

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the pet to retrieve | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Expected response to a valid request |
| default | unexpected error |

### /projects/{projectId}/users

#### POST
##### Summary

Register user as a participant of project

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to register user | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Null response |
| default | unexpected error |

### /projects/{projectId}/tasks

#### GET
##### Summary

Retrieve a list of tasks

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |
| start_time | query | If not exists, retrieves all tasks created after start_time | No | dateTime |
| end_time | query | If not exists, retrieves all tasks created before end_time | No | dateTime |
| last_sync_time | query | (called from mobile application) Get tasks that published after last_sync_time | No | dateTime |
| status | query | If not exists, retrieves all tasks regardless of status | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| default | unexpected error |

#### POST
##### Summary

Create task

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | OK |
| default | unexpected error |

#### PATCH
##### Summary

Upload results of task.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | OK |
| default | unexpected error |

### /projects/{projectId}/tasks/{taskId}

#### GET
##### Summary

Retrieve tasks with a specific task_id

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |
| taskId | path | The id of the task | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| default | unexpected error |

#### PUT
##### Summary

Create revision of a task.

##### Description

Revision Id will be updated.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |
| taskId | path | The id of the task | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | OK |
| default | unexpected error |

#### PATCH
##### Summary

Edit a specific task

##### Description

A task only in DRAFT status can be updated. This is for auto-save or status change

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |
| taskId | path | The id of the task | Yes | string |
| revision_id | query |  | Yes | integer |

##### Responses

| Code | Description |
| ---- | ----------- |
| 204 | No Content |
| default | unexpected error |

#### DELETE
##### Summary

Delete task.

##### Description

Delete all tasks with id

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve | Yes | string |
| taskId | path | The id of the task | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 204 | OK |
| default | unexpected error |

### Models

#### Id

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| value | integer |  | Yes |

#### BaseTime

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| createdAt | dateTime |  | No |
| deletedAt | dateTime |  | No |

#### Project

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| isOpen | boolean |  | No |
| info | object |  | No |

#### ProjectRes

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ProjectRes |  |  |  |

#### ProjectsRes

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ProjectsRes | array |  |  |

#### Projects

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Projects | array |  |  |

#### Participant

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| userId | string | Unique id of user (generated by firebase)<br>_Example:_ `"1cUoc4KcejOY89f2PzDc9Z8Fyf53"` | Yes |
| profile | object | Participant information in JSON with no pre-defined fields<br>_Example:_ `{"birth":"1992-02-24","gender":"female"}` | No |

#### Participants

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Participants | array |  |  |

#### ChoiceQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | Only one option can be chosen for radio, dropdown. Multiple options can be chosen for checkbox.<br>_Enum:_ `"RADIO"`, `"CHECKBOX"`, `"DROPDOWN"` | Yes |
| options | [  ] |  | Yes |

#### TextQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | developers can change this value..<br>_Enum:_ `"LONG"`, `"SHORT"` | Yes |

#### ScaleQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | developers can change this value..<br>_Enum:_ `"SLIDER"` | Yes |
| low | integer | min value of scale | Yes |
| high | integer | max value of scale | Yes |
| lowLabel | string | label of min value<br>_Example:_ `"Somewhat disagree"` | No |
| highLabel | string | label of max value<br>_Example:_ `"Strongly agree"` | No |

#### DateQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | developers can change this value.. | Yes |
| includeTime | boolean |  | No |
| includeYear | boolean |  | No |

#### TimeQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | developers can change this value.. | Yes |
| duration | boolean |  | Yes |

#### FrequencyQuestion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| tag | string | developers can change this value..<br>_Enum:_ `"WEEKLY"`, `"MONTHLY"`, `"YEARLY"` | Yes |

#### Question

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| title | string | same with query | Yes |
| explanation | string |  | No |
| required | boolean |  | No |
| type | string | _Enum:_ `"CHOICE"`, `"TEXT"`, `"SCALE"`, `"DATE"`, `"TIME"`, `"FREQUENCY"` | Yes |
| properties | object | It depends on the value of 'type' | Yes |

#### Questions

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Questions | array |  |  |

#### Row

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| title | string | same with query | Yes |
| explanation | string |  | No |

#### Item

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| type | string | Type of Item (Question & Row will be implemented for v0.9)<br>_Enum:_ `"QUESTION"`, `"ROW"`, `"IMAGE"`, `"ACTIVITY"` | Yes |
| contents |  | According to the type, it will be changed. | Yes |
| sequence | integer | sequence of this item in a task | Yes |

#### Items

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Items | array |  |  |

#### ItemReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type | string | Type of Item (Question & Row will be implemented for v0.9)<br>_Enum:_ `"QUESTION"`, `"ROW"`, `"IMAGE"`, `"ACTIVITY"` | Yes |
| contents |  | According to the type, it will be changed. | Yes |
| sequence | integer | sequence of this item in a task | Yes |

#### ItemsReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ItemsReq | array |  |  |

#### TaskId

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| revisionId | integer |  | Yes |
| id | string |  | Yes |

#### Task

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| revisionId | integer |  | Yes |
| id | string |  | Yes |
| title | string |  | Yes |
| description | string |  | No |
| condition | object |  | No |
| schedule | string | in cronQuartz format<br>_Example:_ `"0 0/1 * 1/1 * ? *"` | Yes |
| startTime | dateTime |  | Yes |
| endTime | dateTime | if not exists, there's no expiration. | No |
| validTime | integer | valid time of each task (minute-based). | Yes |
| status | string | _Enum:_ `"DRAFT"`, `"PUBLISHED"`, `"COMPLETED"`, `"STOPPED"` | Yes |
| items | [  ] |  | Yes |

#### TaskReq

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| title | string |  | Yes |
| description | string |  | No |
| schedule | string | in cronQuartz format<br>_Example:_ `"0 0/1 * 1/1 * ? *"` | Yes |
| startTime | dateTime |  | Yes |
| endTime | dateTime | if not exists, there's no expiration. | No |
| validTime | integer | valid time of each task (minute-based). | Yes |
| status | string | _Enum:_ `"DRAFT"`, `"PUBLISHED"`, `"COMPLETED"`, `"STOPPED"` | Yes |
| items | [  ] |  | Yes |
| condition | object |  | No |

#### Tasks

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| Tasks | array |  |  |

#### TaskResult

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| revisionId | integer |  | No |
| taskId | string |  | No |
| userId | string |  | No |
| startedAt | dateTime |  | No |
| submittedAt | dateTime |  | No |
| itemResults | [  ] |  | No |

#### TaskResults

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| TaskResults | array |  |  |

#### ItemResult

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| itemName | string |  | No |
| result | string |  | No |

#### Error

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | Yes |
| message | string |  | Yes |

#### IntegerValue

At least one of properties should be set.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| min | integer |  | No |
| max | integer |  | No |

#### StringValue

At least one of properties should be set.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| pattern | string |  | No |

#### DateValue

At least one of properties should be set.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| from | date |  | No |
| to | date |  | No |

#### Statement

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| target | string |  | Yes |
| type | string | _Enum:_ `"integer"`, `"string"`, `"date"` | Yes |
| value | object | It depends on the value of 'type' | Yes |

#### Condition

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| criteria | string | _Enum:_ `"oneOf"`, `"anyOf"`, `"allOf"`, `"not"` | Yes |
| statements | [ object ] |  | Yes |
