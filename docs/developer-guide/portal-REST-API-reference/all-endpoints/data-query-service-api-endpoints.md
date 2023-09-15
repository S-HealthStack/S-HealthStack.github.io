
# Data Query Service v0.5.0



<h1 id="data-query-service">Data Query Service v0.5.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://localhost:3030/api/projects/{projectId}">http://localhost:3030/api/projects/{projectId}</a>

    * **projectId** - This is the ID of the project. Default: 0

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="data-query-service-default">Default</h1>

## Search health data by executing the provided SQL statement.

> Code samples

```java
URL obj = new URL("http://localhost:3030/api/projects/{projectId}/sql");
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

`POST /sql`

> Body parameter

```json
{
  "sql": "select * from heartrates where user_id='u1'"
}
```

<h3 id="search-health-data-by-executing-the-provided-sql-statement.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|projectId|path|string|true|This is the ID of the project that needs to be retrieved.|
|body|body|object|true|An SQL statement. This is only allowed to retrieve data.|

> Example responses

> 200 Response

```json
{
  "metadata": {
    "columns": [
      "user_id",
      "..."
    ],
    "count": 8
  },
  "data": [
    {
      "id": "1",
      "user_id": "u1",
      "time": "2019-05-21T00:00:00.000Z",
      "bpm": 120
    },
    {
      "id": "2",
      "user_id": "u1",
      "time": "2019-05-22T00:00:00.000Z",
      "bpm": 108
    }
  ]
}
```

<h3 id="search-health-data-by-executing-the-provided-sql-statement.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|This is the expected response to a valid request.|Inline|
|default|Default|An unexpected error occurred.|Inline|

<h3 id="search-health-data-by-executing-the-provided-sql-statement.-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» metadata|any|false|none|none|
|» data|[object]|true|none|none|

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

