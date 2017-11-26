---
title: NBRB API v1.0.0
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

# NBRB API v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

NBRB API.

Base URLs:

* <a href="https://api.nbrb.by/">https://api.nbrb.by/</a>

* <a href="https://sandbox.nbrb.by/">https://sandbox.nbrb.by/</a>





# Public

## GET /banks

> Code samples

```shell
# You can also use wget
curl -X GET https://api.nbrb.by/banks \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Accept: application/json'

```

```http
GET https://api.nbrb.by/banks HTTP/1.1
Host: api.nbrb.by

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
  url: 'https://api.nbrb.by/banks',
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

fetch('https://api.nbrb.by/banks',
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

result = RestClient.get 'https://api.nbrb.by/banks',
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

r = requests.get('https://api.nbrb.by/banks', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.nbrb.by/banks");
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

*Banks*

Bank.

<h3 id="GET-/banks-parameters">Parameters</h3>

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
  "items": [
    {
      "type": "string",
      "handle": "string",
      "name": "string",
      "full_name": "string",
      "bic": "string",
      "unp": "string",
      "okpo": "string",
      "swift": "string",
      "adress": "string",
      "phone": "string",
      "fax": "string",
      "telex": "string",
      "email": "user@example.com",
      "website": "http://example.com",
      "presedent": "string",
      "registration_number": "string",
      "registration_date": null
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
<h3 id="GET-/banks-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|An array of banks.|[BankList](#schemabanklist)
400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[Error](#schemaerror)
429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|Too Many Requests|[Error](#schemaerror)
default|Default|Unexpected error|[Error](#schemaerror)

<aside class="success">
This operation does not require authentication
</aside>

## GET /currencies

> Code samples

```shell
# You can also use wget
curl -X GET https://api.nbrb.by/currencies \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Version: 1.0.0' \
  -H 'Accept: application/json'

```

```http
GET https://api.nbrb.by/currencies HTTP/1.1
Host: api.nbrb.by

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
  url: 'https://api.nbrb.by/currencies',
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

fetch('https://api.nbrb.by/currencies',
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

result = RestClient.get 'https://api.nbrb.by/currencies',
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

r = requests.get('https://api.nbrb.by/currencies', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("https://api.nbrb.by/currencies");
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
lang|query|string(iso-639-1)(iso-639-1)|false|Language of text data (default belarusan).
at|query|dateTime|false|Currancy rate at specific date. Current time used by default.


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
      "currency_from": "string",
      "currency_from_name": "string",
      "currency_to": "string",
      "currency_to_name": "string",
      "exchange_rate": "string"
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

# Schemas

## Bank

<a name="schemabank"></a>

```json
{
  "type": "string",
  "handle": "string",
  "name": "string",
  "full_name": "string",
  "bic": "string",
  "unp": "string",
  "okpo": "string",
  "swift": "string",
  "adress": "string",
  "phone": "string",
  "fax": "string",
  "telex": "string",
  "email": "user@example.com",
  "website": "http://example.com",
  "presedent": "string",
  "registration_number": "string",
  "registration_date": null
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
type|string|false|Type `Bank`.
handle|string|false|Unique identifier of bank.
name|string|false|Short bank name (localisation).
full_name|string|false|Full bank name (localisation).
bic|string|false|Bank BIC
unp|string|false|Bank UNP
okpo|string|false|Bank OKPO
swift|string|false|Bank S.W.I.F.T.
adress|string|false|Bank adress (localisation).
phone|string(phone)|false|Bank phone.
fax|string(phone)|false|Bank fax.
telex|string|false|Bank telex.
email|string(email)|false|Bank email.
website|string(uri)|false|Bank web site (localisation).
presedent|string|false|Bank president (localisation).
registration_number|string|false|Registration number.
registration_date|date|false|Registration date.



## BankList

<a name="schemabanklist"></a>

```json
{
  "items": [
    {
      "type": "string",
      "handle": "string",
      "name": "string",
      "full_name": "string",
      "bic": "string",
      "unp": "string",
      "okpo": "string",
      "swift": "string",
      "adress": "string",
      "phone": "string",
      "fax": "string",
      "telex": "string",
      "email": "user@example.com",
      "website": "http://example.com",
      "presedent": "string",
      "registration_number": "string",
      "registration_date": null
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
items|[[Bank](#schemabank)]|false|Contains the list of banks.
» type|string|false|Type `Bank`.
» handle|string|false|Unique identifier of bank.
» name|string|false|Short bank name (localisation).
» full_name|string|false|Full bank name (localisation).
» bic|string|false|Bank BIC
» unp|string|false|Bank UNP
» okpo|string|false|Bank OKPO
» swift|string|false|Bank S.W.I.F.T.
» adress|string|false|Bank adress (localisation).
» phone|string(phone)|false|Bank phone.
» fax|string(phone)|false|Bank fax.
» telex|string|false|Bank telex.
» email|string(email)|false|Bank email.
» website|string(uri)|false|Bank web site (localisation).
» presedent|string|false|Bank president (localisation).
» registration_number|string|false|Registration number.
» registration_date|date|false|Registration date.



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
type|string|false|Type `CurrencyRate`.
currency_from|string(iso-4217)|false|Currency ISO 4217 code.
currency_from_name|string|false|Currency name (localisation).
currency_to|string(iso-4217)|false|Currency ISO 4217 code.
currency_to_name|string|false|Currency name (localisation).
exchange_rate|string(decimal)|false|Currency echange rate.



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
» type|string|false|Type `CurrencyRate`.
» currency_from|string(iso-4217)|false|Currency ISO 4217 code.
» currency_from_name|string|false|Currency name (localisation).
» currency_to|string(iso-4217)|false|Currency ISO 4217 code.
» currency_to_name|string|false|Currency name (localisation).
» exchange_rate|string(decimal)|false|Currency echange rate.



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





