# Authentication

## Login

This endpoint will generate access token 

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
password <br> <small>required</small>  | `string` password
fcm <br> <small>optional</small>  | `string` FCM Token (Mobile App)



##  Logout

This endpoint will invoke access token database 

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T13:10:04.724+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": null
}
```

>  **<span style='color:#0489B1'>*401 Unauthorized*</span>**

```json
{
    "timestamp": "2019-07-02T10:35:14.299+0000",
    "status": "Unauthorized",
    "statusCode": 401,
    "message": "Expired JWT token",
    "data": null
}
```

>  **<span style='color:#0489B1'>*401 Unauthorized*</span>**

```json
{
    "timestamp": "2019-07-02T13:12:00.096+0000",
    "status": "Unauthorized",
    "statusCode": 401,
    "message": "Invalid JWT token.",
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

### HTTP Request

`POST /api/v1/identity/logout`

### Header

`Authorization: Bearer [access_token]`

> *Request*

### Payload

None



## Who Am I

This endpoint will get user info based access token

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T13:20:24.367+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "createdBy": "admin",
        "createdAt": 1562052023000,
        "id": 1,
        "username": "developer",
        "email": "developer@mail.com",
        "role": "SUPER_ADMIN",
        "msisdn": "0987654321",
        "activated": true,
        "imageUrl": "http://placehold.it/100",
        "averageRating": 0,
        "client": {
            "createdBy": "admin",
            "createdAt": 1562052502000,
            "id": 1,
            "name": "Developer",
            "code": "Developer",
            "type": "DEVELOPER",
            "status": "active",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/100"
        }
    }
}
```

>  **<span style='color:#0489B1'>*401 Unauthorized*</span>**

```json
{
    "timestamp": "2019-07-02T10:35:14.299+0000",
    "status": "Unauthorized",
    "statusCode": 401,
    "message": "Expired JWT token",
    "data": null
}
```

>  **<span style='color:#0489B1'>*401 Unauthorized*</span>**

```json
{
    "timestamp": "2019-07-02T13:12:00.096+0000",
    "status": "Unauthorized",
    "statusCode": 401,
    "message": "Invalid JWT token.",
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

### HTTP Request

`GET /api/v1/identity/whoami`

### Header

`Authorization: Bearer [access_token]`

### Payload

None


