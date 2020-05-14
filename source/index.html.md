---
title: Facebook API v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="facebook-api">Facebook API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is the entropy facebook api

Base URLs:

* <a href="https://pending.entropy.tech/v1">https://pending.entropy.tech/v1</a>

Email: <a href="mailto:karina@entropy.tech">Support</a> 

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="facebook-api-authorization-url">authorization-url</h1>

Authorization url for Facebook

## get__organizations_{organizationId}_authorization-url

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/authorization-url", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/authorization-url`

*Get authorizationUrl*

<h3 id="get__organizations_{organizationid}_authorization-url-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|none|

> Example responses

> 301 Response

```json
"https://www.facebook.com/v5.0/dialog/oauth?auth_type..."
```

<h3 id="get__organizations_{organizationid}_authorization-url-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|301|[Moved Permanently](https://tools.ietf.org/html/rfc7231#section-6.4.2)|Status moved permanently|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_authorization-url-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-credentials">credentials</h1>

Entropy Facebook credentials resource

## post__organizations_{organizationId}_credentials

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "code": "string",
  "state": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/credentials`

*Add credential to organization*

> Body parameter

```json
{
  "code": "string",
  "state": "string"
}
```

<h3 id="post__organizations_{organizationid}_credentials-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|body|body|object|true|none|
|» code|body|string|false|none|
|» state|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "external_id": "12341234",
  "name": "My facebook credential"
}
```

<h3 id="post__organizations_{organizationid}_credentials-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_credentials-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» external_id|string|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_credentials

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/credentials`

*Get credentials by organization*

<h3 id="get__organizations_{organizationid}_credentials-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|

> Example responses

> 200 Response

```json
[
  {
    "external_id": "12341234",
    "name": "My facebook credential",
    "provider_name": "facebook"
  }
]
```

<h3 id="get__organizations_{organizationid}_credentials-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_credentials-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» external_id|string|false|none|The credential ID.|
|» name|string|false|none|The credential name.|
|» provider_name|string|false|none|The credential provider,|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_credentials_{credentialId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/credentials/{credentialId}`

*Delete credential by id*

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|credentialId|path|string|true|none|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_credentials_{credentialId}

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "code": "string",
  "state": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/credentials/{credentialId}`

*Update organization credential*

> Body parameter

```json
{
  "code": "string",
  "state": "string"
}
```

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|credentialId|path|string|true|none|
|body|body|object|true|none|
|» code|body|string|false|none|
|» state|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "id": 1,
  "name": "My facebook credential"
}
```

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_credentials_{credentialId}_businesses

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/businesses", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/credentials/{credentialId}/businesses`

*Retrieve facebook businesses*

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_businesses-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|credentialId|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "107406950975265",
    "role": "ADMIN",
    "business": {
      "name": "My BM",
      "profile_picture_url": "string",
      "id": "103752451344000"
    }
  }
]
```

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_businesses-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_businesses-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The user scoped business id.|
|» role|string|false|none|The user role in business|
|» business|object|false|none|none|
|»» name|string|false|none|Business manager name|
|»» profile_picture_url|string|false|none|Business Manager profile picture|
|»» id|string|false|none|Business Manager ID|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_credentials_{credentialId}_adaccounts

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/adaccounts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/credentials/{credentialId}/adaccounts`

*Retrieve facebook adaccounts for credential with their linked pages and instagram accounts*

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_adaccounts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|credentialId|path|integer|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "act_123456789101112",
    "name": "Perros y Gatos Co."
  }
]
```

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_adaccounts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}_adaccounts-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The adaccount id.|
|» name|string|false|none|The adaccounts name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## post__organizations_{organizationId}_credentials_{credentialId}_facebook-locations

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations?q=mexico \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations?q=mexico HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations?q=mexico',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations',
  params: {
  'q' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations', params={
  'q': 'mexico'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations?q=mexico");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}/facebook-locations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/credentials/{credentialId}/facebook-locations`

*Search facebok locations*

<h3 id="post__organizations_{organizationid}_credentials_{credentialid}_facebook-locations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|credentialId|path|string|true|The Credential Id|
|q|query|string|true|the searched location|
|locale|query|string|false|ISO 639-1 language code|
|type|query|string|false|Searched location type. Accepts country, region, city|

> Example responses

> 200 Response

```json
[
  {
    "key": "15020915",
    "name": "Estado de México",
    "type": "city",
    "country_code": "MX",
    "country_name": "México",
    "region": "State of Mexico",
    "region_id": 2519
  }
]
```

<h3 id="post__organizations_{organizationid}_credentials_{credentialid}_facebook-locations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="post__organizations_{organizationid}_credentials_{credentialid}_facebook-locations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» key|string|false|none|none|
|» name|string|false|none|none|
|» type|string|false|none|none|
|» country_code|string|false|none|none|
|» country_name|string|false|none|none|
|» region|string|false|none|none|
|» region_id|number|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-accounts">accounts</h1>

Entropy Facebook accounts resource

## post__organizations_{organizationId}_accounts

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "extenal_id": "act_123456789101112",
  "credential_id": 1,
  "instagram_id": "1023317097692584",
  "page_id": "381490061931745"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/accounts`

*Create entropy facebook account*

> Body parameter

```json
{
  "extenal_id": "act_123456789101112",
  "credential_id": 1,
  "instagram_id": "1023317097692584",
  "page_id": "381490061931745"
}
```

<h3 id="post__organizations_{organizationid}_accounts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|body|body|object|true|none|
|» extenal_id|body|string|false|none|
|» credential_id|body|integer|false|none|
|» instagram_id|body|string|false|none|
|» page_id|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "id": 1,
  "name": "My facebook account",
  "currency": "MXN"
}
```

<h3 id="post__organizations_{organizationid}_accounts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_accounts-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The account ID.|
|» name|string|false|none|The account name.|
|» currency|string|false|none|The account currency|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_accounts

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/accounts`

<h3 id="get__organizations_{organizationid}_accounts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|

> Example responses

> 200 Response

```json
[
  {
    "id": 1,
    "name": "My facebook account",
    "currency": "MXN"
  }
]
```

<h3 id="get__organizations_{organizationid}_accounts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_accounts-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The account ID.|
|» name|string|false|none|The account name.|
|» currency|string|false|none|The adaccount currency|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_accounts_{accountId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/accounts/{accountId}`

*Delete Facebook account*

<h3 id="delete__organizations_{organizationid}_accounts_{accountid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|accountId|path|integer|true|The Account Id|

> Example responses

> 400 Response

```json
{
  "message": "Please provide a valid code."
}
```

<h3 id="delete__organizations_{organizationid}_accounts_{accountid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_accounts_{accountid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_accounts_{accountId}_pages

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/pages", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/accounts/{accountId}/pages`

*GetFacebook account*

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_pages-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|accountId|path|integer|true|The Account Id|

> Example responses

> 200 Response

```json
{
  "id": "1023317097692584",
  "name": "My Facebook Page",
  "url": "https://scontent.fmex3-1.fna.fbcdn.net/v/t1.0-1/cp0/p50x50/69990981_2541917302555666_6471452641946763264_o.jpg"
}
```

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_pages-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_pages-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The facebook page id|
|» name|string|false|none|Facebook page name|
|» url|string|false|none|The page profile picture url|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## post__organizations_{organizationId}_accounts_{accountId}_instagram

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/accounts/{accountId}/instagram`

*GetFacebook account*

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_instagram-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|accountId|path|integer|true|The Account Id|

> Example responses

> 200 Response

```json
{
  "id": "1023317097692584",
  "username": "fake_profile",
  "profile_pic": "https://scontent-qro1-1.xx.fbcdn.net/v/t51.2885-15/10358304_683009211734391_805233549_a.jpg?_nc_cat=111&_nc_sid=86c713&_nc_ohc=-BEh1CRhIDAAX_GlXcF&_nc_ht=scontent-qro1-1.xx&oh=51977412f1779267f8e6aa8b26d21bbd&oe=5EB3C9DE"
}
```

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_instagram-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_instagram-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The Instagram id|
|» username|string|false|none|Instagram username|
|» profile_pic|string|false|none|The instagram profile picture url|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_accounts_{accountId}_instagram

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/instagram", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/accounts/{accountId}/instagram`

*GetFacebook account*

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_instagram-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|accountId|path|integer|true|The Account Id|

> Example responses

> 200 Response

```json
{
  "id": "1023317097692584",
  "username": "fake_profile",
  "profile_pic": "https://scontent-qro1-1.xx.fbcdn.net/v/t51.2885-15/10358304_683009211734391_805233549_a.jpg?_nc_cat=111&_nc_sid=86c713&_nc_ohc=-BEh1CRhIDAAX_GlXcF&_nc_ht=scontent-qro1-1.xx&oh=51977412f1779267f8e6aa8b26d21bbd&oe=5EB3C9DE"
}
```

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_instagram-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_accounts_{accountid}_instagram-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The Instagram id|
|» username|string|false|none|Instagram username|
|» profile_pic|string|false|none|The instagram profile picture url|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## post__organizations_{organizationId}_accounts_{accountId}_draft-strategies

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/accounts/{accountId}/draft-strategies", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/accounts/{accountId}/draft-strategies`

*Create draft strategy*

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_draft-strategies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|accountId|path|integer|true|The Account Id|

> Example responses

> 201 Response

```json
{
  "id": "5e602dd4cf1ff689ff36d2b8"
}
```

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_draft-strategies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_accounts_{accountid}_draft-strategies-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-draft-strategies">draft strategies</h1>

Entropy Facebook draft strategies resource

## get__organizations_{organizationId}_draft-strategies

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/draft-strategies`

*Retrieve Facebook campaign draft strategy for given organziation*

<h3 id="get__organizations_{organizationid}_draft-strategies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|

> Example responses

> 200 Response

```json
{
  "account_id": 1,
  "name": "My draft strategy",
  "budget": 0,
  "created_at": "2020-03-04 16:38:12.317086461 -0600 CST m=+5532.901298845"
}
```

<h3 id="get__organizations_{organizationid}_draft-strategies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_draft-strategies-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» account_id|string|false|none|none|
|» name|string|false|none|none|
|» budget|integer|false|none|none|
|» created_at|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_draft-strategies_{draftStrategyId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/draft-strategies/{draftStrategyId}`

*Delete Facebook campaign draft strategy*

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Stratgy Id|

> Example responses

> 204 Response

```json
{
  "message": "strategy deleted"
}
```

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No content|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}-responseschema">Response Schema</h3>

Status Code **204**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-draft-ads">draft ads</h1>

Entropy Facebook Draft Strategy Ads

## post__organizations_{organizationId}_draft-strategies_{draftStrategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads`

*Delete draft ads in draft strategy*

> Body parameter

```json
{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy"
}
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|
|body|body|object|true|none|
|» name|body|string|false|The draft ad name.|
|» headline|body|string|false|The draft ad headline.|
|» primary_text|body|string|false|The draft ad primary text.|
|» description|body|string|false|The draft ad body.|
|» display_link|body|string|false|The draft ad visible link.|

> Example responses

> 200 Response

```json
[
  {
    "name": "My draft ad",
    "headline": "Lo mejor en zapatos",
    "primary_text": "Nuestros pasos bla bla bla",
    "description": "Descuentos de hasta 30%",
    "display_link": "https://entropy.tech"
  }
]
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Draft Ad Successfully Updated|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|The draft ad name.|
|» headline|string|false|none|The draft ad headline.|
|» primary_text|string|false|none|The draft ad primary text.|
|» description|string|false|none|The draft ad body.|
|» display_link|string|false|none|The draft ad visible link.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_draft-strategies_{draftStrategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads`

*Delete draft ads in draft strategy*

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|

> Example responses

> 200 Response

```json
{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy.tech"
}
```

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Draft Ad Successfully found|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|The draft ad name.|
|» headline|string|false|none|The draft ad headline.|
|» primary_text|string|false|none|The draft ad primary text.|
|» description|string|false|none|The draft ad body.|
|» display_link|string|false|none|The draft ad visible link.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_draft-strategies_{draftStrategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy.tech"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads`

*Update draft ads in draft strategy*

> Body parameter

```json
{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy.tech"
}
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|
|body|body|object|true|none|
|» name|body|string|false|The draft ad name.|
|» headline|body|string|false|The draft ad headline.|
|» primary_text|body|string|false|The draft ad primary text.|
|» description|body|string|false|The draft ad body.|
|» display_link|body|string|false|The draft ad visible link.|

> Example responses

> 200 Response

```json
{
  "name": "My draft ad",
  "headline": "Lo mejor en zapatos",
  "primary_text": "Nuestros pasos bla bla bla",
  "description": "Descuentos de hasta 30%",
  "display_link": "https://entropy.tech"
}
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Draft Ad Successfully Updated|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|The draft ad name.|
|» headline|string|false|none|The draft ad headline.|
|» primary_text|string|false|none|The draft ad primary text.|
|» description|string|false|none|The draft ad body.|
|» display_link|string|false|none|The draft ad visible link.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_draft-strategies_{draftStrategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/draft-strategies/{draftStrategyId}/ads`

*Delete draft ads in draft strategy*

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Draft Ad Successfully Deleted|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_ads-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-draft-locations">draft locations</h1>

Entropy Facebook location resource

## post__organizations_{organizationId}_draft-strategies_{draftStrategyId}_geolocations

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations`

*Create new Facebook draft strategy*

This creates a new Facebook strategy

> Body parameter

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Stratgy Id|
|body|body|object|true|none|
|» countries|body|[string]|false|none|
|» regions|body|[object]|false|none|
|»» key|body|string|false|none|
|» cities|body|[object]|false|none|
|»» key|body|string|false|none|
|»» radius|body|integer|false|none|
|»» distance_unit|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "geo_locations": {
    "countries": [
      "MX"
    ],
    "regions": [
      {
        "key": "3843"
      }
    ],
    "cities": [
      {
        "key": "2420605",
        "radius": 10,
        "distance_unit": "mile"
      }
    ]
  }
}
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» geo_locations|object|false|none|none|
|»» countries|[string]|false|none|none|
|»» regions|[object]|false|none|none|
|»»» key|string|false|none|none|
|»» cities|[object]|false|none|none|
|»»» key|string|false|none|none|
|»»» radius|integer|false|none|none|
|»»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_draft-strategies_{draftStrategyId}_geolocations

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations`

*Retrieve Facebook campaign strategy locations*

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Stratgy Id|

> Example responses

> 200 Response

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» countries|[string]|false|none|none|
|» regions|[object]|false|none|none|
|»» key|string|false|none|none|
|» cities|[object]|false|none|none|
|»» key|string|false|none|none|
|»» radius|integer|false|none|none|
|»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_draft-strategies_{draftStrategyId}_geolocations

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/draft-strategies/{draftStrategyId}/geolocations`

*Update Facebook campaign draft strategy locations*

> Body parameter

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|none|
|draftStrategyId|path|string|true|The Draft Stratgy Id|
|body|body|object|true|none|
|» countries|body|[string]|false|none|
|» regions|body|[object]|false|none|
|»» key|body|string|false|none|
|» cities|body|[object]|false|none|
|»» key|body|string|false|none|
|»» radius|body|integer|false|none|
|»» distance_unit|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_geolocations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» countries|[string]|false|none|none|
|» regions|[object]|false|none|none|
|»» key|string|false|none|none|
|» cities|[object]|false|none|none|
|»» key|string|false|none|none|
|»» radius|integer|false|none|none|
|»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-draft-creatives">draft creatives</h1>

Entropy Facebook draft creatives resource

## get__organizations_{organizationId}_draft-strategies_{draftStrategyId}_creatives

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives`

*Retrieve Facebook campaign strategy creatives*

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Stratgy Id|
|id|query|string|false|The Draft Creative Id|

> Example responses

> 200 Response

```json
[
  {
    "id": "5e7bab8b5ecb9ea374bf8a65",
    "name": "My Creative",
    "creative_uri": "images.google.com/epy/creatives/123456ffdf"
  }
]
```

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|Draft Creative id|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## post__organizations_{organizationId}_draft-strategies_{draftStrategyId}_creatives

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "creative",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf",
  "type": "video"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/draft-strategies/{draftStrategyId}/creatives`

*Create new Facebook campaign creative*

This creates a new Facebook campaign creative

> Body parameter

```json
{
  "id": "creative",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf",
  "type": "video"
}
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|
|body|body|object|true|none|
|» id|body|string|false|none|
|» name|body|string|false|none|
|» creative_uri|body|string|false|none|
|» type|body|string|false|Creative type (video, story, etc)|

> Example responses

> 201 Response

```json
{
  "id": "5e7bab8b5ecb9ea374bf8a65",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_creatives-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The draft creative Id.|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_draft-strategies_{draftStrategyId}_draft-creatives_{draftCreativeId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/draft-strategies/{draftStrategyId}/draft-creatives/{draftCreativeId}`

*Delete Facebook draft creative*

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_draft-creatives_{draftcreativeid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|
|draftCreativeId|path|string|true|The Draft Creative Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_draft-creatives_{draftcreativeid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No content|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_draft-strategies_{draftstrategyid}_draft-creatives_{draftcreativeid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-draft-campaigns">draft campaigns</h1>

Entropy Facebook draft campaigns

## post__organizations_{organizationId}_draft-strategies_{draftStrategyId}_campaigns

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '600';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns`

*Create Facebook campaign set in strategy*

> Body parameter

```json
600
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|
|body|body|number|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "5e602dd4cf1ff689ff36d2222",
    "name": "Campañas de remarketing",
    "budget": 10000,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|
|» name|string|false|none|none|
|» budget|integer|false|none|none|
|» objective|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_draft-strategies_{draftStrategyId}_campaigns

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns`

*Retrieve Facebook campaign set strategy*

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|draftStrategyId|path|string|true|The Draft Strategy Id|

> Example responses

> 200 Response

```json
[
  {
    "id": "5e602dd4cf1ff689ff36d2222",
    "name": "Campañas de remarketing",
    "budget": 10000,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|
|» name|string|false|none|none|
|» budget|integer|false|none|none|
|» objective|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_draft-strategies_{draftStrategyId}_campaigns

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '[
  {
    "id": "5e602dd4cf1ff689ff36d2222",
    "name": "Campañas de remarketing",
    "budget": 20000,
    "objective": "CONVERSIONS"
  }
]';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/draft-strategies/{draftStrategyId}/campaigns`

*Update Facebook campaign set strategy*

> Body parameter

```json
[
  {
    "id": "5e602dd4cf1ff689ff36d2222",
    "name": "Campañas de remarketing",
    "budget": 20000,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|draftStrategyId|path|string|true|The Draft Stratgy Id|
|body|body|array[object]|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": "5e602dd4cf1ff689ff36d2222",
    "name": "Campañas de remarketing",
    "country_code": "string",
    "budget": 20000,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Accepted|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_draft-strategies_{draftstrategyid}_campaigns-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|
|» name|string|false|none|none|
|» country_code|string|false|none|none|
|» budget|integer|false|none|none|
|» objective|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-strategy">strategy</h1>

Entropy Facebook strategies resource

## post__organizations_{organizationId}_strategies

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "5e7bab8b5ecb9ea374bf8a65"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/strategies`

*Create new Facebook strategy*

> Body parameter

```json
{
  "id": "5e7bab8b5ecb9ea374bf8a65"
}
```

<h3 id="post__organizations_{organizationid}_strategies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|body|body|object|true|none|
|» id|body|string|false|The Draft Strategy ID|

> Example responses

> 201 Response

```json
{
  "id": "12341234"
}
```

<h3 id="post__organizations_{organizationid}_strategies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_strategies-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies`

*Retrieve Facebook strategies*

<h3 id="get__organizations_{organizationid}_strategies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|

> Example responses

> 200 Response

```json
[
  {
    "name": "My facebook strategy",
    "id": "12341234",
    "budget": 600,
    "status": "PAUSED"
  }
]
```

<h3 id="get__organizations_{organizationid}_strategies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|none|
|» id|string|false|none|none|
|» budget|integer|false|none|none|
|» status|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_strategies_{strategyId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/strategies/{strategyId}`

*Delete  Facebook strategy*

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The strategy Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_status-paused

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-paused", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/status-paused`

*Pause Facebook campaigns set strategy*

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-paused-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The strategy Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-paused-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-paused-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_status-active

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/status-active", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/status-active`

*Pause Facebook strategy*

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-active-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The strategy Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-active-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_status-active-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-strategy-campaigns">strategy campaigns</h1>

Entropy Facebook strategy campaigns

## get__organizations_{organizationId}_strategies_{strategyId}_campaigns

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/campaigns`

*Retrieve  Facebook campaigns set strategy by id*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_campaigns-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The strategy Id|

> Example responses

> 200 Response

```json
[
  {
    "name": "Campañas de remarketing",
    "budget": 100,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_campaigns-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_campaigns-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|none|
|» budget|integer|false|none|none|
|» objective|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_campaigns

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '[
  {
    "name": "Campañas de Remarketing",
    "budget": 100,
    "objective": "CONVERSIONS"
  }
]';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/campaigns", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/campaigns`

*Update campaigns in facebook strategy*

> Body parameter

```json
[
  {
    "name": "Campañas de Remarketing",
    "budget": 100,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_campaigns-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The strategy Id|
|body|body|array[object]|true|none|

> Example responses

> 200 Response

```json
[
  {
    "name": "Campaña de remarketing",
    "budget": 100,
    "objective": "CONVERSIONS"
  }
]
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_campaigns-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_campaigns-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|none|
|» budget|integer|false|none|none|
|» objective|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-strategy-creatives">strategy creatives</h1>

## post__organizations_{organizationId}_strategies_{strategyId}_creatives

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/strategies/{strategyId}/creatives`

*Create new Facebook campaign creative*

This creates a new Facebook campaign creative

> Body parameter

```json
{
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_creatives-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|body|body|object|true|none|
|» name|body|string|false|none|
|» creative_uri|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "id": "5e602dd4cf1ff689ff36d2b8",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_creatives-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_creatives-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The creative ID.|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies_{strategyId}_creatives

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/creatives`

*Retrieve Facebook campaign strategy creatives*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The  Strategy Id|

> Example responses

> 200 Response

```json
[
  {
    "id": 1234,
    "name": "My Creative",
    "creative_uri": "images.google.com/epy/creatives/123456ffdf"
  }
]
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The creative ID.|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_creatives_{creativeId}

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "My Second Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}`

*Uploads Facebook campaign creative*

This Uploads a Facebook campaign creative

> Body parameter

```json
{
  "name": "My Second Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|creativeId|path|integer|true|The creative Id|
|body|body|object|true|none|
|» name|body|string|false|none|
|» creative_uri|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "id": "123456",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The creative ID.|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies_{strategyId}_creatives_{creativeId}

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}`

*Retrieve Facebook campaign strategy creatives*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The  Strategy Id|
|creativeId|path|string|true|The  creative Id|

> Example responses

> 200 Response

```json
{
  "id": "5e602dd4cf1ff689ff36d2b8",
  "name": "My Creative",
  "creative_uri": "images.google.com/epy/creatives/123456ffdf"
}
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|The creative ID.|
|» name|string|false|none|none|
|» creative_uri|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_strategies_{strategyId}_creatives_{creativeId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/strategies/{strategyId}/creatives/{creativeId}`

*Delete Facebook creative*

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|creativeId|path|string|true|The Creative Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Creative Successfully deleted|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_creatives_{creativeid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-strategy-ads">strategy ads</h1>

## post__organizations_{organizationId}_strategies_{strategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '[
  {
    "name": "My ad name",
    "title": "My ad title",
    "body": "Buy this product",
    "visible_uri": "https://entropy.tech",
    "creative_id": "asdfasdfasdf",
    "type": "dynamic_ad"
  }
]';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/strategies/{strategyId}/ads`

*Ads an ad in strategy*

> Body parameter

```json
[
  {
    "name": "My ad name",
    "title": "My ad title",
    "body": "Buy this product",
    "visible_uri": "https://entropy.tech",
    "creative_id": "asdfasdfasdf",
    "type": "dynamic_ad"
  }
]
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|body|body|array[object]|true|none|

> Example responses

> 200 Response

```json
[
  {
    "id": 1,
    "name": "My ad",
    "title": "My ad title",
    "body": "Buy this ad product",
    "visible_uri": "https://entropy.tech"
  }
]
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Ad Successfully Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_ads-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|Ad id.|
|» name|string|false|none|The ad name.|
|» title|string|false|none|The ad title.|
|» body|string|false|none|The ad body.|
|» visible_uri|string|false|none|The ad visible link.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies_{strategyId}_ads

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/ads`

*Retrieves ads in strategy*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|

> Example responses

> 200 Response

```json
[
  {
    "id": 1,
    "name": "My  ad",
    "title": "My title",
    "body": "Buy this product right now",
    "visible_uri": "https://entropy.tech",
    "creative_id": "asdfasdfasdf",
    "type": "dynamic_ad"
  }
]
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Ads Successfully found|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The ad id.|
|» name|string|false|none|The ad name.|
|» title|string|false|none|The ad title.|
|» body|string|false|none|The ad body.|
|» visible_uri|string|false|none|The ad visible link.|
|» creative_id|string|false|none|The ad creative id.|
|» type|string|false|none|The ad type.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies_{strategyId}_ads_{adId}

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/ads/{adId}`

*Retrieves an ad in strategy*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|adId|path|integer|true|The ad Id|

> Example responses

> 200 Response

```json
{
  "name": "My  ad",
  "title": "My title",
  "body": "Buy this product right now",
  "visible_uri": "https://entropy.tech",
  "creative_id": "asdfasdfasdf",
  "type": "dynamic_ad"
}
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Ad Successfully found|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|The ad name.|
|» title|string|false|none|The ad title.|
|» body|string|false|none|The ad body.|
|» visible_uri|string|false|none|The ad visible link.|
|» creative_id|string|false|none|Ad creative id.|
|» type|string|false|none|Ad type|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_ads_{adId}

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "My ad name",
  "title": "My ad title",
  "body": "Buy this product",
  "visible_uri": "https://entropy.tech",
  "creative_id": "asdfasdfasdf",
  "type": "asdfasdfasdf"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/ads/{adId}`

*Updates an ad in strategy*

> Body parameter

```json
{
  "name": "My ad name",
  "title": "My ad title",
  "body": "Buy this product",
  "visible_uri": "https://entropy.tech",
  "creative_id": "asdfasdfasdf",
  "type": "asdfasdfasdf"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|adId|path|string|true|The ad Id|
|body|body|object|true|none|
|» name|body|string|false|The ad name.|
|» title|body|string|false|The ad title.|
|» body|body|string|false|The ad body.|
|» visible_uri|body|string|false|The ad visible link.|
|» creative_id|body|string|false|The ad creative id|
|» type|body|string|false|The ad type|

> Example responses

> 200 Response

```json
{
  "name": "My ad",
  "title": "My ad title",
  "body": "Buy this ad product",
  "visible_uri": "https://entropy.tech",
  "creative_id": "string"
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Ad Successfully Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» name|string|false|none|The ad name.|
|» title|string|false|none|The ad title.|
|» body|string|false|none|The ad body.|
|» visible_uri|string|false|none|The ad visible link.|
|» creative_id|string|false|none|The ad creative id.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_strategies_{strategyId}_ads_{adId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/ads/{adId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/strategies/{strategyId}/ads/{adId}`

*Deletes an ad in strategy*

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|adId|path|string|true|The ad Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Ad Successfully deleted|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_ads_{adid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

<h1 id="facebook-api-strategy-locations">strategy locations</h1>

## post__organizations_{organizationId}_strategies_{strategyId}_locations

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/strategies/{strategyId}/locations`

*Creates locations in strategy*

> Body parameter

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_locations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|body|body|object|true|none|
|» countries|body|[string]|false|none|
|» regions|body|[object]|false|none|
|»» key|body|string|false|none|
|» cities|body|[object]|false|none|
|»» key|body|string|false|none|
|»» radius|body|integer|false|none|
|»» distance_unit|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_locations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Locations Successfully Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="post__organizations_{organizationid}_strategies_{strategyid}_locations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» countries|[string]|false|none|none|
|» regions|[object]|false|none|none|
|»» key|string|false|none|none|
|» cities|[object]|false|none|none|
|»» key|string|false|none|none|
|»» radius|integer|false|none|none|
|»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## get__organizations_{organizationId}_strategies_{strategyId}_locations

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/strategies/{strategyId}/locations`

*Retrieves locations in strategy*

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_locations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|

> Example responses

> 200 Response

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_locations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|locations found|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="get__organizations_{organizationid}_strategies_{strategyid}_locations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» countries|[string]|false|none|none|
|» regions|[object]|false|none|none|
|»» key|string|false|none|none|
|» cities|[object]|false|none|none|
|»» key|string|false|none|none|
|»» radius|integer|false|none|none|
|»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## put__organizations_{organizationId}_strategies_{strategyId}_locations

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/strategies/{strategyId}/locations`

*Updates locations in strategy*

> Body parameter

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_locations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|
|body|body|object|true|none|
|» countries|body|[string]|false|none|
|» regions|body|[object]|false|none|
|»» key|body|string|false|none|
|» cities|body|[object]|false|none|
|»» key|body|string|false|none|
|»» radius|body|integer|false|none|
|»» distance_unit|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "countries": [
    "MX"
  ],
  "regions": [
    {
      "key": "3843"
    }
  ],
  "cities": [
    {
      "key": "2420605",
      "radius": 10,
      "distance_unit": "mile"
    }
  ]
}
```

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_locations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|locations successfully updates|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="put__organizations_{organizationid}_strategies_{strategyid}_locations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» countries|[string]|false|none|none|
|» regions|[object]|false|none|none|
|»» key|string|false|none|none|
|» cities|[object]|false|none|none|
|»» key|string|false|none|none|
|»» radius|integer|false|none|none|
|»» distance_unit|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

## delete__organizations_{organizationId}_strategies_{strategyId}_locations

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/strategies/{strategyId}/locations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/strategies/{strategyId}/locations`

*Deletes locations in strategy*

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_locations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The Organization Id|
|strategyId|path|string|true|The Strategy Id|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_locations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|locations deleted|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|408|[Request Timeout](https://tools.ietf.org/html/rfc7231#section-6.5.7)|Request Time Out|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server error|Inline|

<h3 id="delete__organizations_{organizationid}_strategies_{strategyid}_locations-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **408**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearerAuth
</aside>

