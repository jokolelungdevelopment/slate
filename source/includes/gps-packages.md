#GPS Packages

## Create gps package

This endpoint used for create gps package

> *Request*

```json
{
	"packageName" : "com.domain.package"
}
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
    "message": "Data aplikasi Fake GPS sudah terdaftar",
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

`POST /api/v1/identity/gps-package`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
packageName <br> <small>required</small>  | `string` package name


## Update gps package

This endpoint used for update gps package

> *Request*

```json
{
	"packageName" : "com.domain.new.package"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:44.196+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "updated",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data aplikasi Fake GPS sudah terdaftar",
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

`PUT /api/v1/identity/gps-package/<ID>`

### Header

`Authorization: Bearer [access_token]`

### URL Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  |  package id

### Payload

Parameter | Description
--------- | -----------
packageName <br> <small>required</small>  | `string` package name



## Delete gps package

This endpoint used for delete gps package

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:44.196+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "deleted",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data aplikasi Fake GPS tidak terdaftar",
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

`DELETE /api/v1/identity/gps-package/<ID>`

### Header

`Authorization: Bearer [access_token]`

### URL Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  |  package id


## Get a specific gps package

This endpoint used for get a specific gps package

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:35:55.526+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "createdBy": "username",
        "createdAt": 1562051992605,
        "id": 1,
        "packageName": "com.package.name"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data aplikasi Fake GPS tidak terdaftar",
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

`GET /api/v1/identity/gps-package/<ID>`

### Header

`Authorization: Bearer [access_token]`

### URL Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  |  package id


## Get list gps package

This endpoint used for get a list gps package

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:35:55.526+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": [
        {
            "createdBy": "username",
            "createdAt": 1562051992605,
            "id": 1,
            "packageName": "com.package.name1"
        },
        {
            "createdBy": "username",
            "createdAt": 1562051992605,
            "id": 2,
            "packageName": "com.package.name2"
        },
        {
            "createdBy": "username",
            "createdAt": 1562051992605,
            "id": 3,
            "packageName": "com.package.name3"
        }
    ]
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:23:27.680+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data aplikasi Fake GPS tidak terdaftar",
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

`GET /api/v1/identity/gps-package`

### Header

`Authorization: Bearer [access_token]`

### Query Parameter

Parameter | Description
--------- | -----------
dateFrom <br> <small>required</small>  |  `long` from date
