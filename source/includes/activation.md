# Activation

## Activate

This endpoint will ...

> *Request*

```json
{
    "email": "developer@mail.com",
    "username": "developer",
    "password": "123456",
    "fcm": "HqCFIU4xlnu3aiENbyaUYdrQxPuEa8JaK2I7ZREaZvU3GkIgRoM6"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T13:29:14.983+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "access_token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJkZXZlbG9wZXJAbWFpbC5jb20iLCJhdXRoIjoiU1VQRVJfQURNSU4iLCJhbGlhcyI6ImRldmVsb3BlciIsImlhdCI6MTU2MjA3NDE1NCwiZXhwIjoxNTYyNjc4OTU0fQ.4jb30fO9toHhvGySEsM6GklvdLx3Oremp28RGuoV1kwJjGvG8JMCreW47TY28kmTadVhmfPq8pXZwaDgh6rfRg"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:28:30.141+0000",
    "status": "Not Found",
    "statusCode": 404,
    "message": "Data pengguna tidak terdaftar",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:27:33.801+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data pengguna sudah aktif",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:29:57.005+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Perusahaan anda belum aktif",
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

`POST /api/v1/identity/activate`

### Header

None

### Payload

Parameter | Description
--------- | -----------
email <br> <small>required</small>  | `string` valid email address
username <br> <small>required</small>  | `string` usename
password <br> <small>required</small>  | `string` password
fcm <br> <small>optional</small>  | `string` FCM Token (Mobile App)



## verify

This endpoint will used to verify email address is registered or not

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:09:07.162+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": null
}
```

>  **<span style='color:#04B404'>*200 OK*</span>** <br>(Role as DRIVER)

```json
{
    "timestamp": "2019-07-02T16:09:07.162+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "username" : "Driver Name",
        "email" : "driver@mail.com"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:28:30.141+0000",
    "status": "Not Found",
    "statusCode": 404,
    "message": "Data pengguna tidak terdaftar",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:08:00.557+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Email sudah diaktivasi, silahkan melakukan login",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:27:33.801+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data pengguna sudah aktif",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T13:29:57.005+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Perusahaan anda belum aktif",
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

`GET /api/v1/identity/verify`

### Header

None

### Query Parameter

Parameter | Default | Description
--------- | ------- | -----------
email <br><small>required</small>  | `empty` | valid email address.


## Change Password

This endpoint used for update account credentials

> *Request*

```json
{
	"oldPassword" : "123456",
	"newPassword" : "0987654321"
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

`POST /api/v1/identity/change-password`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
oldPassword <br> <small>required</small>  | `string` old password
newPassword <br> <small>required</small>  | `string` new password

