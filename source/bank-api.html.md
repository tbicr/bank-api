---
title: Bank API v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2
---

# Bank API v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Bank API.

Base URLs:

* <a href="https://api.bank.by/">https://api.bank.by/</a>

* <a href="https://sandbox.nbrb.by/">https://sandbox.nbrb.by/</a>





# Authentication



- oAuth2 authentication. 

    - Flow: authorizationCode
    - Authorization URL = [https://api.bank.by/oauth2/authorize](https://api.bank.by/oauth2/authorize)
    - Token URL = [https://api.bank.by/oauth2/access_token](https://api.bank.by/oauth2/access_token)

|Scope|Scope Description|
|---|---|
|read:accounts|Grant read accounts access.|
|read:transactions|Grant read transactions access.|
|create:transactions|Grant create transactions access.|


    - Flow: implicit
    - Authorization URL = [https://api.bank.by/auth/login](https://api.bank.by/auth/login)

|Scope|Scope Description|
|---|---|
|read:accounts|Grant read accounts access.|
|read:transactions|Grant read transactions access.|
|create:transactions|Grant create transactions access.|




# Public

## GET /currencies

> Code samples

```shell
# You can also use wget
curl -X GET https://api.bank.by/currencies \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Accept: applicaiton/json'

```

```http
GET https://api.bank.by/currencies HTTP/1.1
Host: api.bank.by

Accept: applicaiton/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'applicaiton/json'

};

$.ajax({
  url: 'https://api.bank.by/currencies',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'applicaiton/json'

};

fetch('https://api.bank.by/currencies',
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
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Accept' => 'applicaiton/json'
}

result = RestClient.get 'https://api.bank.by/currencies',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Accept': 'applicaiton/json'
}

r = requests.get('https://api.bank.by/currencies', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/currencies");
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

*Currencies*

Currencies.

<h3 id="GET-/currencies-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
lang|query|string(iso-639-1)|false|Language of text data (default belarusan).


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="GET-/currencies-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of currencies.|[CurrencyRateList](#schemacurrencyratelist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="success">
This operation does not require authentication
</aside>

## GET /atms

> Code samples

```shell
# You can also use wget
curl -X GET https://api.bank.by/atms \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Accept: application/json'

```

```http
GET https://api.bank.by/atms HTTP/1.1
Host: api.bank.by

Accept: application/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://api.bank.by/atms',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'application/json'

};

fetch('https://api.bank.by/atms',
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
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.bank.by/atms',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Accept': 'application/json'
}

r = requests.get('https://api.bank.by/atms', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/atms");
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

*ATMs*

ATMs.

<h3 id="GET-/atms-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
lang|query|string(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "name": "string",
      "address": {
        "country": "string",
        "state": "string",
        "city": "string",
        "line": "string",
        "postcode": "string"
      },
      "located_at": "string",
      "location": {
        "type": "string",
        "coordinates": [
          0
        ]
      },
      "opening_hours": "string",
      "support_languages": [
        "string"
      ],
      "supported_currencies": [
        "string"
      ],
      "supported_services": [
        "string"
      ]
    }
  ]
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="GET-/atms-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of ATMs.|[ATMList](#schemaatmlist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="success">
This operation does not require authentication
</aside>

## GET /branches

> Code samples

```shell
# You can also use wget
curl -X GET https://api.bank.by/branches \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Accept: application/json'

```

```http
GET https://api.bank.by/branches HTTP/1.1
Host: api.bank.by

Accept: application/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://api.bank.by/branches',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Accept':'application/json'

};

fetch('https://api.bank.by/branches',
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
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.bank.by/branches',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Accept': 'application/json'
}

r = requests.get('https://api.bank.by/branches', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/branches");
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

*Branches*

Branches.

<h3 id="GET-/branches-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
lang|query|string(iso-639-1)(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "name": "string",
      "address": {
        "country": "string",
        "state": "string",
        "city": "string",
        "line": "string",
        "postcode": "string"
      },
      "location": {
        "type": "string",
        "coordinates": [
          0
        ]
      },
      "note": "string",
      "phone": "string",
      "opening_hours": "string",
      "supported_services": [
        "string"
      ]
    }
  ]
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="GET-/branches-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of brnaches.|[BranchList](#schemabranchlist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="success">
This operation does not require authentication
</aside>

# Account

## GET /accounts

> Code samples

```shell
# You can also use wget
curl -X GET https://api.bank.by/accounts \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys' \
  -H 'Accept: application/json'

```

```http
GET https://api.bank.by/accounts HTTP/1.1
Host: api.bank.by

Accept: application/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0
Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://api.bank.by/accounts',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept':'application/json'

};

fetch('https://api.bank.by/accounts',
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
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Authorization' => 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.bank.by/accounts',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Authorization': 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept': 'application/json'
}

r = requests.get('https://api.bank.by/accounts', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/accounts");
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

*Accounts*

List of accounts.

<h3 id="GET-/accounts-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
Authorization|header|string|true|Authorization (OAuth2 Bearer).
lang|query|string(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "iban": "string",
      "bic": "string",
      "balance": "string",
      "currency": "string"
    }
  ]
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="GET-/accounts-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of accounts.|[AccountList](#schemaaccountlist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[Error](#schemaerror)
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
oauth2 ( Scopes: read:accounts )
</aside>

## GET /account/{account_id}/transactions

> Code samples

```shell
# You can also use wget
curl -X GET https://api.bank.by/account/{account_id}/transactions \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys' \
  -H 'Accept: application/json'

```

```http
GET https://api.bank.by/account/{account_id}/transactions HTTP/1.1
Host: api.bank.by

Accept: application/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0
Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://api.bank.by/account/{account_id}/transactions',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept':'application/json'

};

fetch('https://api.bank.by/account/{account_id}/transactions',
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
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Authorization' => 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.bank.by/account/{account_id}/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Authorization': 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'Accept': 'application/json'
}

r = requests.get('https://api.bank.by/account/{account_id}/transactions', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/account/{account_id}/transactions");
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

*Operations History*

Operations history.

<h3 id="GET-/account/{account_id}/transactions-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
Authorization|header|string|true|Authorization (OAuth2 Bearer).
lang|query|string(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).
account_id|path|string(object-uuid)|true|No description


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "items": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="GET-/account/{account_id}/transactions-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of operations.|[TransactionList](#schematransactionlist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[Error](#schemaerror)
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|[Error](#schemaerror)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
oauth2 ( Scopes: read:transactions )
</aside>

# Payment

## POST /account/{account_id}/transactions

> Code samples

```shell
# You can also use wget
curl -X POST https://api.bank.by/account/{account_id}/transactions \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys' \
  -H 'X-Idempotency-Key: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.bank.by/account/{account_id}/transactions HTTP/1.1
Host: api.bank.by
Content-Type: application/json
Accept: application/json
Accept: application/json
Content-Type: application/json
X-Api-Version: 1.0.0
Authorization: Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys
X-Idempotency-Key: string

```

```javascript
var headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'X-Idempotency-Key':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://api.bank.by/account/{account_id}/transactions',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "to": null,
  "amount": "string",
  "currency": "string",
  "charge_policy": "SHARED",
  "description": "string",
  "metadata": {
    "property1": "string",
    "property2": "string"
  }
}';
const headers = {
  'Accept':'application/json',
  'Content-Type':'application/json',
  'X-Api-Version':'1.0.0',
  'Authorization':'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'X-Idempotency-Key':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://api.bank.by/account/{account_id}/transactions',
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
  'Accept' => 'application/json',
  'Content-Type' => 'application/json',
  'X-Api-Version' => '1.0.0',
  'Authorization' => 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'X-Idempotency-Key' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://api.bank.by/account/{account_id}/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Content-Type': 'application/json',
  'X-Api-Version': '1.0.0',
  'Authorization': 'Bearer wism73ydof4spe8o92x705t36wbfx41av8bltyys',
  'X-Idempotency-Key': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://api.bank.by/account/{account_id}/transactions', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.bank.by/account/{account_id}/transactions");
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

*Make Operation*

Make operation.

> Body parameter

```json
{
  "to": null,
  "amount": "string",
  "currency": "string",
  "charge_policy": "SHARED",
  "description": "string",
  "metadata": {
    "property1": "string",
    "property2": "string"
  }
}
```
<h3 id="POST-/account/{account_id}/transactions-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
Accept|header|string|false|Accept response body content type (default application/json).
Content-Type|header|string|false|Request body content type (default application/json).
X-Api-Version|header|string|false|API version (default latest).
Authorization|header|string|true|Authorization (OAuth2 Bearer).
X-Idempotency-Key|header|string|false|Idempotency key.
lang|query|string(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).
account_id|path|string(object-uuid)|true|No description
body|body|[TransactionCreate](#schematransactioncreate)|true|Make opeation.


#### Enumerated Values

|Parameter|Value|
|---|---|
Accept|application/json|
Content-Type|application/json|
lang|be|
lang|ru|
lang|en-US|

> Example responses

```json
{
  "type": "string",
  "id": "string",
  "from": null,
  "to": null,
  "amount": "string",
  "currency": "string",
  "charge_policy": "SHARED",
  "description": "string",
  "metadata": {
    "property1": "string",
    "property2": "string"
  },
  "created_at": "2017-11-26T08:05:05Z"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
}
```
<h3 id="POST-/account/{account_id}/transactions-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Operation.|[Transaction](#schematransaction)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[Error](#schemaerror)
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|[Error](#schemaerror)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
oauth2 ( Scopes: create:transactions )
</aside>

# Schemas

## PostalAddress

<a name="schemapostaladdress"></a>

```json
{
  "country": "string",
  "state": "string",
  "city": "string",
  "line": "string",
  "postcode": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
country|string(iso-3166-1)|true|Country code.
state|string|true|State (localisation).
city|string|true|City (localisation).
line|string|true|Address (localisation).
postcode|string|false|Postcode.



## GEOJsonPoint

<a name="schemageojsonpoint"></a>

```json
{
  "type": "string",
  "coordinates": [
    0
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|true|Type `Point`
coordinates|[number(float)]|false|longitude, latitude



## ATM

<a name="schemaatm"></a>

```json
{
  "type": "string",
  "id": "string",
  "name": "string",
  "address": {
    "country": "string",
    "state": "string",
    "city": "string",
    "line": "string",
    "postcode": "string"
  },
  "located_at": "string",
  "location": {
    "type": "string",
    "coordinates": [
      0
    ]
  },
  "opening_hours": "string",
  "support_languages": [
    "string"
  ],
  "supported_currencies": [
    "string"
  ],
  "supported_services": [
    "string"
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|true|Type `ATM`.
id|string|true|Unique identifier of ATM.
name|string|true|ATM name/ref (localisation).
address|[PostalAddress](#schemapostaladdress)|true|No description
» country|string(iso-3166-1)|true|Country code.
» state|string|true|State (localisation).
» city|string|true|City (localisation).
» line|string|true|Address (localisation).
» postcode|string|false|Postcode.
located_at|string|false|Additional location information (localisation).
location|[GEOJsonPoint](#schemageojsonpoint)|true|No description
» type|string|true|Type `Point`
» coordinates|[number(float)]|false|longitude, latitude
opening_hours|string(opening-hours)|true|Opening hours.
support_languages|[string(iso-639-1)]|false|Support languages.
supported_currencies|[string(iso-4217)]|false|Support currencies.
supported_services|[string]|false|Supported services.



## ATMList

<a name="schemaatmlist"></a>

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "name": "string",
      "address": {
        "country": "string",
        "state": "string",
        "city": "string",
        "line": "string",
        "postcode": "string"
      },
      "located_at": "string",
      "location": {
        "type": "string",
        "coordinates": [
          0
        ]
      },
      "opening_hours": "string",
      "support_languages": [
        "string"
      ],
      "supported_currencies": [
        "string"
      ],
      "supported_services": [
        "string"
      ]
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|[[ATM](#schemaatm)]|false|Contains the list of ATMs.
» type|string|true|Type `ATM`.
» id|string|true|Unique identifier of ATM.
» name|string|true|ATM name/ref (localisation).
» address|[PostalAddress](#schemapostaladdress)|true|No description
»» country|string(iso-3166-1)|true|Country code.
»» state|string|true|State (localisation).
»» city|string|true|City (localisation).
»» line|string|true|Address (localisation).
»» postcode|string|false|Postcode.
» located_at|string|false|Additional location information (localisation).
» location|[GEOJsonPoint](#schemageojsonpoint)|true|No description
»» type|string|true|Type `Point`
»» coordinates|[number(float)]|false|longitude, latitude
» opening_hours|string(opening-hours)|true|Opening hours.
» support_languages|[string(iso-639-1)]|false|Support languages.
» supported_currencies|[string(iso-4217)]|false|Support currencies.
» supported_services|[string]|false|Supported services.



## Branch

<a name="schemabranch"></a>

```json
{
  "type": "string",
  "id": "string",
  "name": "string",
  "address": {
    "country": "string",
    "state": "string",
    "city": "string",
    "line": "string",
    "postcode": "string"
  },
  "location": {
    "type": "string",
    "coordinates": [
      0
    ]
  },
  "note": "string",
  "phone": "string",
  "opening_hours": "string",
  "supported_services": [
    "string"
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|true|Type `Branch`.
id|string|true|Unique identifier of branch.
name|string|true|Branch name/ref (localisation).
address|[PostalAddress](#schemapostaladdress)|true|No description
» country|string(iso-3166-1)|true|Country code.
» state|string|true|State (localisation).
» city|string|true|City (localisation).
» line|string|true|Address (localisation).
» postcode|string|false|Postcode.
location|[GEOJsonPoint](#schemageojsonpoint)|true|No description
» type|string|true|Type `Point`
» coordinates|[number(float)]|false|longitude, latitude
note|string|false|Additional location and access information (localisation).
phone|string(phone)|false|Contact phone.
opening_hours|string(opening-hours)|true|Opening hours.
supported_services|[string]|false|Supported operations.



## BranchList

<a name="schemabranchlist"></a>

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "name": "string",
      "address": {
        "country": "string",
        "state": "string",
        "city": "string",
        "line": "string",
        "postcode": "string"
      },
      "location": {
        "type": "string",
        "coordinates": [
          0
        ]
      },
      "note": "string",
      "phone": "string",
      "opening_hours": "string",
      "supported_services": [
        "string"
      ]
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|[[Branch](#schemabranch)]|false|Contains the list of branches.
» type|string|true|Type `Branch`.
» id|string|true|Unique identifier of branch.
» name|string|true|Branch name/ref (localisation).
» address|[PostalAddress](#schemapostaladdress)|true|No description
»» country|string(iso-3166-1)|true|Country code.
»» state|string|true|State (localisation).
»» city|string|true|City (localisation).
»» line|string|true|Address (localisation).
»» postcode|string|false|Postcode.
» location|[GEOJsonPoint](#schemageojsonpoint)|true|No description
»» type|string|true|Type `Point`
»» coordinates|[number(float)]|false|longitude, latitude
» note|string|false|Additional location and access information (localisation).
» phone|string(phone)|false|Contact phone.
» opening_hours|string(opening-hours)|true|Opening hours.
» supported_services|[string]|false|Supported operations.



## CurrencyRate

<a name="schemacurrencyrate"></a>

```json
{
  "type": "string",
  "currency_from": "string",
  "currency_from_name": "string",
  "currency_to": "string",
  "currency_to_name": "string",
  "exchange_rate": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|true|Type `CurrencyRate`.
currency_from|string(iso-4217)|true|Currency ISO 4217 code.
currency_from_name|string|false|Currency name (localisation).
currency_to|string(iso-4217)|true|Currency ISO 4217 code.
currency_to_name|string|false|Currency name (localisation).
exchange_rate|string(decimal)|true|Currency echange rate.



## CurrencyRateList

<a name="schemacurrencyratelist"></a>

```json
{
  "items": [
    {
      "type": "string",
      "currency_from": "string",
      "currency_from_name": "string",
      "currency_to": "string",
      "currency_to_name": "string",
      "exchange_rate": "string"
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|[[CurrencyRate](#schemacurrencyrate)]|false|Contains the list of currencies.
» type|string|true|Type `CurrencyRate`.
» currency_from|string(iso-4217)|true|Currency ISO 4217 code.
» currency_from_name|string|false|Currency name (localisation).
» currency_to|string(iso-4217)|true|Currency ISO 4217 code.
» currency_to_name|string|false|Currency name (localisation).
» exchange_rate|string(decimal)|true|Currency echange rate.



## Account

<a name="schemaaccount"></a>

```json
{
  "type": "string",
  "id": "string",
  "iban": "string",
  "bic": "string",
  "balance": "string",
  "currency": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|false|Type `Account`
id|string(object-uuid)|false|Account identificator.
iban|string(iban)|false|IBAN.
bic|string(bic)|false|BIC.
balance|string(decimal)|false|Balance.
currency|string(iso-4217)|false|Currency ISO 4217 code.



## AccountList

<a name="schemaaccountlist"></a>

```json
{
  "items": [
    {
      "type": "string",
      "id": "string",
      "iban": "string",
      "bic": "string",
      "balance": "string",
      "currency": "string"
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|[[Account](#schemaaccount)]|false|Countains the list of accounts.
» type|string|false|Type `Account`
» id|string(object-uuid)|false|Account identificator.
» iban|string(iban)|false|IBAN.
» bic|string(bic)|false|BIC.
» balance|string(decimal)|false|Balance.
» currency|string(iso-4217)|false|Currency ISO 4217 code.



## TransactionSender

<a name="schematransactionsender"></a>

```json
{
  "iban": "string",
  "name": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
iban|string(iban)|false|IBAN.
name|string|false|Full name.



## TransactionRecipient

<a name="schematransactionrecipient"></a>

```json
{
  "iban": "string",
  "bic": "string",
  "name": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
iban|string(iban)|false|IBAN.
bic|string(bic)|false|BIC.
name|string|false|Full name.



## TransactionCreate

<a name="schematransactioncreate"></a>

```json
{
  "to": null,
  "amount": "string",
  "currency": "string",
  "charge_policy": "SHARED",
  "description": "string",
  "metadata": {
    "property1": "string",
    "property2": "string"
  }
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
to|#/components/schemas/TransactionRecipient|true|Recipient.
amount|string(decimal)|true|Transaction amount.
currency|string(iso-4217)|true|Currency ISO 4217 code.
charge_policy|string|false|Charge policy.
description|string|false|Description (optional).
metadata|object|false|Metadata (optional).


#### Enumerated Values

|Property|Value|
|---|---|
charge_policy|SHARED|
charge_policy|RECEIVER|
charge_policy|SENDER|


## Transaction

<a name="schematransaction"></a>

```json
{
  "type": "string",
  "id": "string",
  "from": null,
  "to": null,
  "amount": "string",
  "currency": "string",
  "charge_policy": "SHARED",
  "description": "string",
  "metadata": {
    "property1": "string",
    "property2": "string"
  },
  "created_at": "2017-11-26T08:05:05Z"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|false|Type `Transaction`
id|string(object-uuid)|false|Operation identificator.
from|#/components/schemas/TransactionSender|false|Sender.
to|#/components/schemas/TransactionRecipient|false|Recipient.
amount|string(decimal)|false|Transaction amount
currency|string(iso-4217)|false|Currency ISO 4217 code.
charge_policy|string|false|Charge policy.
description|string|false|Description.
metadata|object|false|Metadata.
created_at|string(date-time)|false|Time when transaction was created.


#### Enumerated Values

|Property|Value|
|---|---|
charge_policy|SHARED|
charge_policy|RECEIVER|
charge_policy|SENDER|


## TransactionList

<a name="schematransactionlist"></a>

```json
{
  "items": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|string|false|Countains the list of transactions.
» type|string|false|Type `Transaction`
» id|string(object-uuid)|false|Operation identificator.
» from|#/components/schemas/TransactionSender|false|Sender.
» to|#/components/schemas/TransactionRecipient|false|Recipient.
» amount|string(decimal)|false|Transaction amount
» currency|string(iso-4217)|false|Currency ISO 4217 code.
» charge_policy|string|false|Charge policy.
» description|string|false|Description.
» metadata|object|false|Metadata.
» created_at|string(date-time)|false|Time when transaction was created.


#### Enumerated Values

|Property|Value|
|---|---|
» charge_policy|SHARED|
» charge_policy|RECEIVER|
» charge_policy|SENDER|


## Error

<a name="schemaerror"></a>

```json
{
  "code": "string",
  "message": "string",
  "fields": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
code|string|false|No description
message|string|false|No description
fields|string|false|No description





