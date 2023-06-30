---


title: Data Query ServicAPI Endpoints
sidebar: dev_doc_sidebar
permalink: data-query-service-api-endpoints.html
toc: false


---


# Data Query Service
## Version: 0.5.0

You can also find more interactive document here: [SwaggerHub-Data_Query_Service/0.5.0](https://app.swaggerhub.com/apis/zainalisamsung/data-query_service/0.5.0)

### /sql

#### POST
##### Summary

Search Health Data by executing the given SQL statement.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| projectId | path | The id of the project to retrieve. | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Expected response to a valid request. |
| default | Unexpected Error |

### Models

#### Error

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | Yes |
| message | string |  | Yes |
