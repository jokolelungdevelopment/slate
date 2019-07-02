---
title: Elogistic API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - json

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true
---

# Introduction

Elogistic API References

All API Endpoint on this document still in development process and may still change occure

**SANDBOX**

**http://54.254.154.42**

# Authentication

## Login

This endpoint will generate access token 

### HTTP Request

`POST /api/v1/identity/login`

### Header

None

> *Request*

```json
{
	"email" : "developer@gmail.com",
	"password" : "123456",
	"fcm" : "HqCFIU4xlnu3aiENbyaUYdrQxPuEa8JaK2I7ZREaZvU3GkIgRoM6"
}
```

### Payload

Parameter | Description
--------- | -----------
email <br> <small>required</small>  | `string` valid email address
password <br> <small>required</small>  | `string` passwordPage
fcm <br> <small>optional</small>  | `string` FCM Token (Mobile App)

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-05-29T09:01:01.191+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "access_token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJkZXZlbG9wZXJAbWFpbC5jb20iLCJhdXRoIjoiU1VQRVJfQURNSU4iLCJpYXQiOjE1NTkxMjA0NjAsImV4cCI6MTU1OTcyNTI2MH0.a9kuuiJ7NqJ3rneuGXNPB8rxsqQQFjw4iUTmw8hNfuSLntbNsggR_u_euecgSEkvmNf5C1GJRRD_wXfAuFZFGQ"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T10:34:20.386+0000",
    "status": "Not Found",
    "statusCode": 404,
    "message": "Email belum terdaftar, silahkan hubungin admin",
    "data": null
}
```

>  **<span style='color:#0489B1'>*401 Unauthorized*</span>**

```json
{
    "timestamp": "2019-07-02T10:35:14.299+0000",
    "status": "Unauthorized",
    "statusCode": 401,
    "message": "Email/password anda salah",
    "data": null
}
```

>  **<span style='color:#DF0101'>*500 Internal Server Error*</span>** 

```json
{
    "timestamp": "2019-07-02T10:35:14.299+0000",
    "status": "Internal Server Error",
    "statusCode": 500,
    "message": "Telah terjadi kesalahan pada sistem",
    "data": null
}
```

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

