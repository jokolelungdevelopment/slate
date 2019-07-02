#Users

## Create user

This endpoint used for create user account

> *Request*

```json
{
    "clientId": 1,
    "email": "email@mail.com",
    "phone": "1234567890",
    "role": "ROLE",
    "imageUrl": "http://placehold.it/100",
    "username": "username"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:33:17.976+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "created",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:38:04.907+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Email sudah terdaftar",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:38:19.072+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nomor ponsel pengguna sudah terdaftar",
    "data": null
}
```
>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:39:29.523+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL tidak ditemukan",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:39:29.523+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nama pengguna sudah terdaftar",
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

`POST /api/v1/identity/users`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
clientId <br> <small>required</small>  | `long` client id
username <br> <small>required</small>  | `string` username
email <br> <small>required</small>  | `string` valid email address
role <br> <small>required</small>  | `string` user `ROLE` based on Enum
phone| `string` phone number
imageUrl| `string` image url


## Update user

This endpoint used for update user account 

> *Request*

```json
{
    "clientId": 1,
    "email": "new_email@mail.com",
    "phone": "123456789011",
    "role": "ROLE",
    "imageUrl": "http://placehold.it/100",
    "username": "new username"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:33:17.976+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "updated",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:38:04.907+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Email sudah terdaftar",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:38:19.072+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nomor ponsel pengguna sudah terdaftar",
    "data": null
}
```
>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:39:29.523+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL tidak ditemukan",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:39:29.523+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nama pengguna sudah terdaftar",
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

`PUT /api/v1/identity/users/<ID>`

### Header

`Authorization: Bearer [access_token]`

### Query Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  | `long` user id

### Payload

Parameter | Description
--------- | -----------
clientId <br> <small>required</small>  | `long` client id
username <br> <small>required</small>  | `string` username
email <br> <small>required</small>  | `string` valid email address
role <br> <small>required</small>  | `string` user `ROLE` based on Enum
phone| `string` phone number
imageUrl| `string` image url


## Delete user

This endpoint used for delete user account by id 

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:33:17.976+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "deleted",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:39:29.523+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data pengguna tidak terdaftar",
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

`DELETE /api/v1/identity/users/<ID>`

### Header

`Authorization: Bearer [access_token]`

### Query Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  | `long` user id


## Create batch user account

This endpoint used for bulk create user account

> *Request*

```json
[
    {
        "clientId": 1,
        "email": "email1@mail.com",
        "role": "ROLE"
        
    },
    {
        "clientId": 1,
        "email": "email2@mail.com",
        "role": "ROLE"
        
    }
]
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:44.196+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "created",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Email %s sudah terdaftar",
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

`POST /api/v1/identity/users/batch`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
Array of object|
clientId <br> <small>required</small>  | `string` client id
email <br> <small>required</small>  | `string` valid email address
role <br> <small>required</small>  | `string` user ROLE

## Get user specific by id

This endpoint used for get specific user detail

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:02:08.080+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "createdBy": "developer",
        "createdAt": 1562052023348,
        "id": 1,
        "username": "Shipper",
        "email": "developer@mail.com",
        "role": "SHIPPER",
        "msisdn": "",
        "activated": true,
        "imageUrl": "http://placehold.it/200",
        "averageRating": 3,
        "client": {
            "createdBy": "developer",
            "createdAt": 1562051992605,
            "id": 2,
            "name": "SHIPPER",
            "code": "S1562052367129",
            "type": "SHIPPER",
            "status": "ACTIVE",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/200"
        }
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T18:02:35.239+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data pengguna tidak terdaftar",
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

`GET /api/v1/identity/user/<ID>`

### Header

`Authorization: Bearer [access_token]`


## Filter users

This endpoint used for retrieve users by parameter

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:07:21.104+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "totalPages": 1,
        "totalElements": 2,
        "contents": [
            {
                "createdBy": "username",
                "createdAt": 1562089081844,
                "id": 10,
                "username": "username1",
                "email": "email1@mail.com",
                "role": "ROLE",
                "msisdn": "1234567890",
                "activated": false,
                "imageUrl": "http://placehold.it/100",
                "averageRating": 3,
                "client": {
                    "createdBy": "admin",
                    "createdAt": 1562052502000,
                    "id": 1,
                    "name": "client name",
                    "code": "Code",
                    "type": "TYPE",
                    "status": "ACTIVE",
                    "averageRating": 3,
                    "imageUrl": "http://placehold.it/100"
                }
            },
            {
                "createdBy": "username",
                "createdAt": 1562089120950,
                "id": 11,
                "username": "username2",
                "email": "email2@mail.com",
                "role": "ROLE",
                "msisdn": "12345678901",
                "activated": false,
                "imageUrl": "http://placehold.it/100",
                "averageRating": 3,
                "client": {
                    "createdBy": "admin",
                    "createdAt": 1562052502000,
                    "id": 1,
                    "name": "client name",
                    "code": "Code",
                    "type": "TYPE",
                    "status": "ACTIVE",
                    "averageRating": 3,
                    "imageUrl": "http://placehold.it/100"
                }
            }
        ]
    }
}
```
>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:07:21.104+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "totalPages": 0,
        "totalElements": 0,
        "contents": []
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

`GET /api/v1/identity/users/filter`

### Header

`Authorization: Bearer [access_token]`

### Query Paramater

Parameter | Description
--------- | -----------
page <br> <small>required</small>  | `long` 
size <br> <small>required</small>  | `long` 
sort | `string` 
clientId | `long` 
client | `string` 
email | `string` 
phone | `string` 


## Rate user

This endpoint used for update rating client and user

> *Request*

```json
{
	"userId" : 1,
	"clientRating" : 3.5,
	"userRating" : 4.0
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:44.196+0000",
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

`POST /api/v1/identity/users/rating`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
userId <br> <small>required</small>  | `long` user id
clientRating <br> <small>required</small>  | `float` client rating
userRating <br> <small>required</small>  | `float` user rating


## Get user list

This endpoint used for retrieve users info

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:07:21.104+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": [
        {
            "createdBy": "username",
            "createdAt": 1562089081844,
            "id": 10,
            "username": "username1",
            "email": "email1@mail.com",
            "role": "ROLE",
            "msisdn": "1234567890",
            "activated": false,
            "imageUrl": "http://placehold.it/100",
            "averageRating": 3,
            "client": {
                "createdBy": "admin",
                "createdAt": 1562052502000,
                "id": 1,
                "name": "client name",
                "code": "Code",
                "type": "TYPE",
                "status": "ACTIVE",
                "averageRating": 3,
                "imageUrl": "http://placehold.it/100"
            }
        },
        {
            "createdBy": "username",
            "createdAt": 1562089120950,
            "id": 11,
            "username": "username2",
            "email": "email2@mail.com",
            "role": "ROLE",
            "msisdn": "12345678901",
            "activated": false,
            "imageUrl": "http://placehold.it/100",
            "averageRating": 3,
            "client": {
                "createdBy": "admin",
                "createdAt": 1562052502000,
                "id": 1,
                "name": "client name",
                "code": "Code",
                "type": "TYPE",
                "status": "ACTIVE",
                "averageRating": 3,
                "imageUrl": "http://placehold.it/100"
            }
        }
    ]
}
```
>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:07:21.104+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": []
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Password lama tidak sesuai",
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

`GET /api/v1/identity/users/list`

### Header

`Authorization: Bearer [access_token]`

### Query Parameter

Parameter | Description
--------- | -----------
id <br> <small>required</small>  | `long[]` user id

