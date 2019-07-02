#Role

## Get Roles

This endpoint used for retrieve roles

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T18:20:25.478+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": [
        "SHIPPER",
        "TRANSPORTER",
        "DRIVER",
        "SUPER_ADMIN",
        "ADMIN",
        "MONITORING"
    ]
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

`GET /api/v1/identity/roles`

### Header

`Authorization: Bearer [access_token]`

