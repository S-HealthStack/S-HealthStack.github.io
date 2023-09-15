



<h1 id="cloud-storage-service">Cloud Storage Service</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="cloud-storage-service-object">Object</h1>

## Retrieve a signed URL for object file upload.

> Code samples

```java
URL obj = new URL("/cloud-storage/projects/{projectId}/upload-url?object_name=string");
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

`GET /cloud-storage/projects/{projectId}/upload-url`

This endpoint provides a signed URL for uploading the specified object file.
You need to call the returned signed-url  using the "PUT" HTTP method with the file included in the request body.

<h3 id="retrieve-a-signed-url-for-object-file-upload.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|integer|true|The ID of the project to be accessed.|
|object_name|query|string|true|The name of the object file to be uploaded.|

> Example responses

> 200 Response

```
"https://example.url/ex?ex=e"
```

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="retrieve-a-signed-url-for-object-file-upload.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Operation successful.|string|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="retrieve-a-signed-url-for-object-file-upload.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Download an object file.

> Code samples

```java
URL obj = new URL("/cloud-storage/projects/{projectId}/download?object_name=string");
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

`GET /cloud-storage/projects/{projectId}/download`

This endpoint retrieves an object file from the specified project ID's folder.

<h3 id="download-an-object-file.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|integer|true|The ID of the project to be accessed.|
|object_name|query|string|true|The name of the object file to be downloaded.|

> Example responses

> 200 Response

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="download-an-object-file.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Operation successful. The response includes a binary string body.|string|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="download-an-object-file.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Retrieve a signed URL for object file download.

> Code samples

```java
URL obj = new URL("/cloud-storage/projects/{projectId}/download-url?object_name=string");
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

`GET /cloud-storage/projects/{projectId}/download-url`

This endpoint provides a signed URL for downloading the specified object file.
The returned signed URL should be invoked using the "GET" method.

<h3 id="retrieve-a-signed-url-for-object-file-download.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|integer|true|The ID of the project to be accessed.|
|object_name|query|string|true|The name of the object file to be downloaded.|
|url_duration|query|string|false|The duration for which the download URL should be valid.|

> Example responses

> 200 Response

```
"https://example.url/ex?ex=e"
```

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="retrieve-a-signed-url-for-object-file-download.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Operation successful.|string|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="retrieve-a-signed-url-for-object-file-download.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## List object attributes.

> Code samples

```java
URL obj = new URL("/cloud-storage/projects/{projectId}/list?path=string");
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

`GET /cloud-storage/projects/{projectId}/list`

This endpoint lists the attributes (name & size) of objects located at the specified path.

<h3 id="list-object-attributes.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|integer|true|The ID of the project to be accessed.|
|path|query|string|true|The path from which to retrieve objects.|

> Example responses

> 200 Response

```json
[
  {
    "name": "string",
    "size": 0
  }
]
```

<h3 id="list-object-attributes.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Operation successful.|Inline|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="list-object-attributes.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|true|none|none|
|» size|integer|true|none|none|

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## Delete an object file.

> Code samples

```java
URL obj = new URL("/cloud-storage/projects/{projectId}/delete?object_name=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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

`DELETE /cloud-storage/projects/{projectId}/delete`

This endpoint deletes the specified object file from the project ID's folder.

<h3 id="delete-an-object-file.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|integer|true|The ID of the project to be accessed.|
|object_name|query|string|true|The name of the object file to be deleted.|

> Example responses

> default Response

```json
{
  "code": "string",
  "message": "string"
}
```

<h3 id="delete-an-object-file.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Operation successful. In the absence of automatic redirection, a 307 response will be received with the signed URL located in the 'Location' header.|None|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="delete-an-object-file.-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|string|true|none|none|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

# Schemas

<h2 id="tocS_ObjectInfo">ObjectInfo</h2>

<a id="schemaobjectinfo"></a>
<a id="schema_ObjectInfo"></a>
<a id="tocSobjectinfo"></a>
<a id="tocsobjectinfo"></a>

```json
{
  "name": "string",
  "size": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|size|integer|true|none|none|

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

