# Clients

## Create Client Detail

This endpoint used for create client detail

> *Request*

```json
{
    "clientType": "SHIPPER",
    "clientName": "NAMA PERUSAHAAN",
    "address1": "ALAMAT PERUSAHAAN 1",
    "address2": "ALAMAT PERUSAHAAN 2",
    "addressUrbanVillage": "KELURAHAAN",
    "addressSubDistrict": "KECAMATAN",
    "addressDistrict": "KODYA/KAB",
    "addressCity": "KOTA",
    "addressProvince": "PROVINSI",
    "addressPostalCode": "KODE POS",
    "billingAddress1": "ALAMAT PENAGIHAN 1",
    "billingAddress2": "ALAMAT PENAGIHAN 2",
    "billingUrbanVillage": "KELURAHAAN PENAGIHAN",
    "billingSubDistrict": "KECAMATAN PENAGIHAN",
    "billingDistrict": "KODYA/KAB PENAGIHAN",
    "billingCity": "KOTA PENAGIHAN",
    "billingProvince": "PROVINSI PENAGIHAN",
    "billingPostalCode": "KODE POS PENAGIHAN",
    "phoneNo": "KANTOR TELEPON",
    "faxNo": "KANTOR FAX",
    "npwpNo": "NO NPWP",
    "pkpNo": "NO PKP",
    "presidentDirector": "NAMA PIMPINAN",
    "companyService": "PRODUK / JASA PERUSAHAAN",
    "siupNo": "NO SIUP",
    "tdpNo": "NO TDP",
    "establishDate": "01-05-2019",
    "imageUrl": "http://placehold.it/200"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:30:05.646+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "clientId": 5,
        "clientCode": "S1562085005580",
        "clientType": "SHIPPER",
        "clientName": "NAMA PERUSAHAAN",
        "address1": "ALAMAT PERUSAHAAN 1",
        "address2": "ALAMAT PERUSAHAAN 2",
        "addressUrbanVillage": "KELURAHAAN",
        "addressSubDistrict": "KECAMATAN",
        "addressDistrict": "KODYA/KAB",
        "addressCity": "KOTA",
        "addressProvince": "PROVINSI",
        "addressPostalCode": "KODE POS",
        "billingAddress1": "ALAMAT PENAGIHAN 1",
        "billingAddress2": "ALAMAT PENAGIHAN 2",
        "billingUrbanVillage": "KELURAHAAN PENAGIHAN",
        "billingSubDistrict": "KECAMATAN PENAGIHAN",
        "billingDistrict": "KODYA/KAB PENAGIHAN",
        "billingCity": "KOTA PENAGIHAN",
        "billingProvince": "PROVINSI PENAGIHAN",
        "billingPostalCode": "KODE POS PENAGIHAN",
        "phoneNo": "KANTOR TELEPON",
        "faxNo": "KANTOR FAX",
        "npwpNo": "NO NPWP",
        "pkpNo": "NO PKP",
        "presidentDirector": "NAMA PIMPINAN",
        "companyService": "PRODUK / JASA PERUSAHAAN",
        "siupNo": "NO SIUP",
        "tdpNo": "NO TDP",
        "establishDate": "01-05-2019",
        "imageUrl": "http://placehold.it/200",
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:30:21.657+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nama customer/rekanan 3PL sudah terdaftar",
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

`POST /api/v1/identity/clients/detail`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
clientType<br> <small>required</small>  | `string`
clientName<br> <small>required</small>  | `string`
address1<br> <small>required</small>  | `string`
address2<br> <small>required</small>  | `string`
addressUrbanVillage<br> <small>required</small>  | `string`
addressSubDistrict<br> <small>required</small>  | `string`
addressDistrict<br> <small>required</small>  | `string`
addressCity<br> <small>required</small>  | `string`
addressProvince<br> <small>required</small>  | `string`
addressPostalCode<br> <small>required</small>  | `string`
billingAddress1<br> <small>required</small>  | `string`
billingAddress2<br> <small>required</small>  | `string`
billingUrbanVillage<br> <small>required</small>  | `string`
billingSubDistrict<br> <small>required</small>  | `string`
billingDistrict<br> <small>required</small>  | `string`
billingCity<br> <small>required</small>  | `string`
billingProvince<br> <small>required</small>  | `string`
billingPostalCode<br> <small>required</small>  | `string`
phoneNo| `string`
faxNo| `string`
npwpNo| `string`
pkpNo| `string`
presidentDirector| `string`
companyService| `string`
siupNo| `string`
tdpNo| `string`
establishDate| `string`
imageUrl| `string`


## Update Client Detail

This endpoint used for update client detail

> *Request*

```json
{
    "clientId": 5,
    "clientType": "SHIPPER",
    "clientName": "NAMA PERUSAHAAN",
    "address1": "ALAMAT PERUSAHAAN 1",
    "address2": "ALAMAT PERUSAHAAN 2",
    "addressUrbanVillage": "KELURAHAAN",
    "addressSubDistrict": "KECAMATAN",
    "addressDistrict": "KODYA/KAB",
    "addressCity": "KOTA",
    "addressProvince": "PROVINSI",
    "addressPostalCode": "KODE POS",
    "billingAddress1": "ALAMAT PENAGIHAN 1",
    "billingAddress2": "ALAMAT PENAGIHAN 2",
    "billingUrbanVillage": "KELURAHAAN PENAGIHAN",
    "billingSubDistrict": "KECAMATAN PENAGIHAN",
    "billingDistrict": "KODYA/KAB PENAGIHAN",
    "billingCity": "KOTA PENAGIHAN",
    "billingProvince": "PROVINSI PENAGIHAN",
    "billingPostalCode": "KODE POS PENAGIHAN",
    "phoneNo": "KANTOR TELEPON",
    "faxNo": "KANTOR FAX",
    "npwpNo": "NO NPWP",
    "pkpNo": "NO PKP",
    "presidentDirector": "NAMA PIMPINAN",
    "companyService": "PRODUK / JASA PERUSAHAAN",
    "siupNo": "NO SIUP",
    "tdpNo": "NO TDP",
    "establishDate": "01-05-2019",
    "imageUrl": "http://placehold.it/200"
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:30:05.646+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "clientId": 5,
        "clientCode": "S1562085005580",
        "clientType": "SHIPPER",
        "clientName": "NAMA PERUSAHAAN",
        "address1": "ALAMAT PERUSAHAAN 1",
        "address2": "ALAMAT PERUSAHAAN 2",
        "addressUrbanVillage": "KELURAHAAN",
        "addressSubDistrict": "KECAMATAN",
        "addressDistrict": "KODYA/KAB",
        "addressCity": "KOTA",
        "addressProvince": "PROVINSI",
        "addressPostalCode": "KODE POS",
        "billingAddress1": "ALAMAT PENAGIHAN 1",
        "billingAddress2": "ALAMAT PENAGIHAN 2",
        "billingUrbanVillage": "KELURAHAAN PENAGIHAN",
        "billingSubDistrict": "KECAMATAN PENAGIHAN",
        "billingDistrict": "KODYA/KAB PENAGIHAN",
        "billingCity": "KOTA PENAGIHAN",
        "billingProvince": "PROVINSI PENAGIHAN",
        "billingPostalCode": "KODE POS PENAGIHAN",
        "phoneNo": "KANTOR TELEPON",
        "faxNo": "KANTOR FAX",
        "npwpNo": "NO NPWP",
        "pkpNo": "NO PKP",
        "presidentDirector": "NAMA PIMPINAN",
        "companyService": "PRODUK / JASA PERUSAHAAN",
        "siupNo": "NO SIUP",
        "tdpNo": "NO TDP",
        "establishDate": "01-05-2019",
        "imageUrl": "http://placehold.it/200",
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:30:21.657+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Nama customer/rekanan 3PL sudah terdaftar",
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

`PUT /api/v1/identity/clients/detail`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
clientId<br> <small>required</small>  | `long`
clientType<br> <small>required</small>  | `string`
clientName<br> <small>required</small>  | `string`
address1<br> <small>required</small>  | `string`
address2<br> <small>required</small>  | `string`
addressUrbanVillage<br> <small>required</small>  | `string`
addressSubDistrict<br> <small>required</small>  | `string`
addressDistrict<br> <small>required</small>  | `string`
addressCity<br> <small>required</small>  | `string`
addressProvince<br> <small>required</small>  | `string`
addressPostalCode<br> <small>required</small>  | `string`
billingAddress1<br> <small>required</small>  | `string`
billingAddress2<br> <small>required</small>  | `string`
billingUrbanVillage<br> <small>required</small>  | `string`
billingSubDistrict<br> <small>required</small>  | `string`
billingDistrict<br> <small>required</small>  | `string`
billingCity<br> <small>required</small>  | `string`
billingProvince<br> <small>required</small>  | `string`
billingPostalCode<br> <small>required</small>  | `string`
phoneNo| `string`
faxNo| `string`
npwpNo| `string`
pkpNo| `string`
presidentDirector| `string`
companyService| `string`
siupNo| `string`
tdpNo| `string`
establishDate| `string`
imageUrl| `string`



## Create Client Contract

This endpoint used for create client contract

> *Request*

```json
{
    "clientId": 5,
    "startDate": "01-01-2019",
    "endDate": "31-12-2019",
    "termOfPayment": "TERM OF PAYMENT",
    "paymentMethod": "TRANSFER",
    "paymentPIC": "NAMA PIC PEMBAYARAN",
    "paymentPICNo": "NO TELPON PIC PEMBAYARAN",
    "operationalPIC": "NAMA PIC OPERATIONAL",
    "operationalPICNo": "NO TELPON PIC OPERATIONAL",
    "insurance": "YES",
    "isAuditedByKAP": "YES",
    "averageValueShipment": "AVERAGE VALUE PER SHIPMENT",
    "totalAsset": "TOTAL ASSET",
    "ventureCapital": "MODAL USAHA",
    "totalSales": "TOTAL ASSET",
    "shareholder": "PEMEGANG SAHAM",
    "bankName": "NAMA BANK",
    "bankAccountName": "NAMA PEMILIK REKENING",
    "bankAccountNo": "NOMOR REKENING",
    "typeOfServiceUsed": [
        "FLI INTEGRATED SERVICE",
        "FLI TRANSPORTATION",
        "FLI WAREHOUSING",
        "OTHERS"
    ]
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

`POST /api/v1/identity/clients/contract`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
clientId <br> <small>required</small>  | `long` 
startDate <br> <small>required</small>  | `string` 
endDate <br> <small>required</small>  | `string`
termOfPayment <br> <small>required</small>  | `string`
paymentMethod| `string`
paymentPIC| `string`
paymentPICNo| `string`
operationalPIC| `string`
operationalPICNo| `string`
insurance| `string` YES;NO
isAuditedByKAP| `string` YES;NO
averageValueShipment| `string`
totalAsset| `string`
ventureCapital| `string`
totalSales| `string`
shareholder| `string`
bankName| `string`
bankAccountName| `string` 
bankAccountNo| `string` 
typeOfServiceUsed| `string` 



## Update Client Contract

This endpoint used for update client contract

> *Request*

```json
{
    "clientId": 5,
    "startDate": "01-01-2019",
    "endDate": "31-12-2019",
    "termOfPayment": "TERM OF PAYMENT",
    "paymentMethod": "TRANSFER",
    "paymentPIC": "NAMA PIC PEMBAYARAN",
    "paymentPICNo": "NO TELPON PIC PEMBAYARAN",
    "operationalPIC": "NAMA PIC OPERATIONAL",
    "operationalPICNo": "NO TELPON PIC OPERATIONAL",
    "insurance": "YES",
    "isAuditedByKAP": "YES",
    "averageValueShipment": "AVERAGE VALUE PER SHIPMENT",
    "totalAsset": "TOTAL ASSET",
    "ventureCapital": "MODAL USAHA",
    "totalSales": "TOTAL ASSET",
    "shareholder": "PEMEGANG SAHAM",
    "bankName": "NAMA BANK",
    "bankAccountName": "NAMA PEMILIK REKENING",
    "bankAccountNo": "NOMOR REKENING",
    "typeOfServiceUsed": [
        "FLI INTEGRATED SERVICE",
        "FLI TRANSPORTATION",
        "FLI WAREHOUSING",
        "OTHERS"
    ]
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

`PUT /api/v1/identity/clients/contract`

### Header

`Authorization: Bearer [access_token]`

### Payload

Parameter | Description
--------- | -----------
clientId <br> <small>required</small>  | `long` 
startDate <br> <small>required</small>  | `string` 
endDate <br> <small>required</small>  | `string`
termOfPayment <br> <small>required</small>  | `string`
paymentMethod| `string`
paymentPIC| `string`
paymentPICNo| `string`
operationalPIC| `string`
operationalPICNo| `string`
insurance| `string` YES;NO
isAuditedByKAP| `string` YES;NO
averageValueShipment| `string`
totalAsset| `string`
ventureCapital| `string`
totalSales| `string`
shareholder| `string`
bankName| `string`
bankAccountName| `string` 
bankAccountNo| `string` 
typeOfServiceUsed| `string` 


## Get Client specific client detail

This endpoint used for get specific client detail

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:52:16.826+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "client": {
            "createdBy": "developer",
            "createdAt": 1562085005593,
            "id": 5,
            "name": "NAMA PERUSAHAAN",
            "code": "S1562085478146",
            "type": "SHIPPER",
            "status": "DRAFT",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/200"
        },
        "clientDetail": {
            "addressProvince": "PROVINSI",
            "insurance": "YES",
            "totalAsset": "TOTAL ASSET",
            "contractPeriodStart": "01-01-2019",
            "presidentDirector": "NAMA PIMPINAN",
            "contractNo": "CON1562085641287",
            "paymentPic": "NAMA PIC PEMBAYARAN",
            "bankAccountNo": "NOMOR REKENING",
            "bankName": "NAMA BANK",
            "billingDistrict": "KODYA/KAB PENAGIHAN",
            "phoneNo": "KANTOR TELEPON",
            "billingAddress2": "ALAMAT PENAGIHAN 2",
            "addressPostalCode": "KODE POS",
            "billingAddress1": "ALAMAT PENAGIHAN 1",
            "companyService": "PRODUK / JASA PERUSAHAAN",
            "billingProvince": "PROVINSI PENAGIHAN",
            "id": 5,
            "billingUrbanVillage": "KELURAHAAN PENAGIHAN",
            "addressCity": "KOTA",
            "termOfPayment": "TERM OF PAYMENT",
            "operationalPicMsisdn": "NO TELPON PIC OPERATIONAL",
            "bankAccountName": "NAMA PEMILIK REKENING",
            "isAuditedByKap": "YES",
            "address2": "ALAMAT PERUSAHAAN 2",
            "address1": "ALAMAT PERUSAHAAN 1",
            "contractPeriodEnd": "31-12-2019",
            "siupNo": "NO SIUP",
            "averageValuePerShipment": "AVERAGE VALUE PER SHIPMENT",
            "shareholder": "PEMEGANG SAHAM",
            "billingSubDistrict": "KECAMATAN PENAGIHAN",
            "pkpNo": "NO PKP",
            "totalSales": "TOTAL ASSET",
            "npwpNo": "NO NPWP",
            "addressSubDistrict": "KODYA/KAB",
            "establishDate": "01-05-2019",
            "tdpNo": "NO TDP",
            "ventureCapital": "MODAL USAHA",
            "faxNo": "KANTOR FAX",
            "typeOfServicesUsed": [
                "FLI INTEGRATED SERVICE",
                "FLI TRANSPORTATION",
                "FLI WAREHOUSING",
                "OTHERS"
            ],
            "billingPostalCode": "KODE POS PENAGIHAN",
            "operationalPic": "NAMA PIC OPERATIONAL",
            "paymentPicMsisdn": "NO TELPON PIC PEMBAYARAN",
            "paymentMethod": "TRANSFER",
            "addressDistrict": "KODYA/KAB",
            "addressUrbanVillage": "KELURAHAAN",
            "billingCity": "KOTA PENAGIHAN"
        }
    }
}
```

>  **<span style='color:#0489B1'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T16:52:28.513+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL tidak ditemukan",
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

`GET /api/v1/identity/clients/detail/<ID>`

### Header

`Authorization: Bearer [access_token]`

### URL Paramater

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  | `long` 


## Filter client by parameter

This endpoint used for retrieve all client info based on parameter

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:57:32.960+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "totalPages": 1,
        "totalElements": 2,
        "contents": [
            {
                "client": {
                    "createdBy": "developer",
                    "createdAt": 1562052502644,
                    "id": 3,
                    "name": "TRANSPORTER 1",
                    "code": "T1562052643552",
                    "type": "TRANSPORTER",
                    "status": "ACTIVE",
                    "averageRating": 3,
                    "imageUrl": "http://placehold.it/200"
                },
                "clientDetail": {
                    "addressProvince": "PROVINSI",
                    "insurance": null,
                    "totalAsset": null,
                    "contractPeriodStart": "01-01-2019",
                    "presidentDirector": "",
                    "contractNo": "CON1562052517871",
                    "paymentPic": null,
                    "bankAccountNo": null,
                    "bankName": null,
                    "billingDistrict": "KODYA/KAB",
                    "phoneNo": "",
                    "billingAddress2": "ALAMAT PERUSAHAAN",
                    "addressPostalCode": "KODE POS",
                    "billingAddress1": "ALAMAT PERUSAHAAN",
                    "companyService": "",
                    "billingProvince": "PROVINSI",
                    "id": 3,
                    "billingUrbanVillage": "KELURAHAAN",
                    "addressCity": "KOTA",
                    "termOfPayment": "30",
                    "operationalPicMsisdn": null,
                    "bankAccountName": null,
                    "isAuditedByKap": null,
                    "address2": "ALAMAT PERUSAHAAN",
                    "address1": "ALAMAT PERUSAHAAN",
                    "contractPeriodEnd": "31-12-2019",
                    "siupNo": "",
                    "averageValuePerShipment": null,
                    "shareholder": null,
                    "billingSubDistrict": "KECAMATAN",
                    "pkpNo": "",
                    "totalSales": null,
                    "npwpNo": "",
                    "addressSubDistrict": "KODYA/KAB",
                    "establishDate": "01-01-2019",
                    "tdpNo": "",
                    "ventureCapital": null,
                    "faxNo": "",
                    "typeOfServicesUsed": [
                        "",
                        "",
                        "",
                        ""
                    ],
                    "billingPostalCode": "KODE POS",
                    "operationalPic": null,
                    "paymentPicMsisdn": null,
                    "paymentMethod": null,
                    "addressDistrict": "KODYA/KAB",
                    "addressUrbanVillage": "KELURAHAAN",
                    "billingCity": "KOTA"
                }
            },
            {
                "client": {
                    "createdBy": "developer",
                    "createdAt": 1562052677860,
                    "id": 4,
                    "name": "TRANSPORTER 2",
                    "code": "T1562052677858",
                    "type": "TRANSPORTER",
                    "status": "ACTIVE",
                    "averageRating": 3,
                    "imageUrl": "http://placehold.it/200"
                },
                "clientDetail": {
                    "addressProvince": "PROVINSI",
                    "insurance": null,
                    "totalAsset": null,
                    "contractPeriodStart": "01-01-2019",
                    "presidentDirector": "",
                    "contractNo": "CON1562052694216",
                    "paymentPic": null,
                    "bankAccountNo": null,
                    "bankName": null,
                    "billingDistrict": "KODYA/KAB",
                    "phoneNo": "",
                    "billingAddress2": "ALAMAT PERUSAHAAN",
                    "addressPostalCode": "KODE POS",
                    "billingAddress1": "ALAMAT PERUSAHAAN",
                    "companyService": "",
                    "billingProvince": "PROVINSI",
                    "id": 4,
                    "billingUrbanVillage": "KELURAHAAN",
                    "addressCity": "KOTA",
                    "termOfPayment": "30",
                    "operationalPicMsisdn": null,
                    "bankAccountName": null,
                    "isAuditedByKap": null,
                    "address2": "ALAMAT PERUSAHAAN",
                    "address1": "ALAMAT PERUSAHAAN",
                    "contractPeriodEnd": "01-01-2020",
                    "siupNo": "",
                    "averageValuePerShipment": null,
                    "shareholder": null,
                    "billingSubDistrict": "KECAMATAN",
                    "pkpNo": "",
                    "totalSales": null,
                    "npwpNo": "",
                    "addressSubDistrict": "KODYA/KAB",
                    "establishDate": "01-01-2019",
                    "tdpNo": "",
                    "ventureCapital": null,
                    "faxNo": "",
                    "typeOfServicesUsed": [
                        "",
                        "",
                        "",
                        ""
                    ],
                    "billingPostalCode": "KODE POS",
                    "operationalPic": null,
                    "paymentPicMsisdn": null,
                    "paymentMethod": null,
                    "addressDistrict": "KODYA/KAB",
                    "addressUrbanVillage": "KELURAHAAN",
                    "billingCity": "KOTA"
                }
            }
        ]
    }
}
```

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T16:57:32.960+0000",
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

`GET /api/v1/identity/clients/filter`

### Header

`Authorization: Bearer [access_token]`

### Query Paramater

Parameter | Description
--------- | -----------
page <br> <small>required</small>  | `long` 
size <br> <small>required</small>  | `long` 
sort | `string` 
type | `string` 
name | `string` 



## Activate client

This endpoint used for flag active client

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:13:55.363+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "createdBy": "developer",
        "createdAt": 1562085005593,
        "id": 5,
        "name": "NAMA PERUSAHAAN",
        "code": "S1562085478146",
        "type": "SHIPPER",
        "status": "ACTIVE",
        "averageRating": 3,
        "imageUrl": "http://placehold.it/200"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:15:52.444+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL tidak ditemukan",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:16:11.228+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL sudah aktif",
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

`POST /api/v1/identity/clients/<ID>/active`

### Header

`Authorization: Bearer [access_token]`

### URL Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  | client id



## Deactivate client

This endpoint used for flag inactive client

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:19:12.936+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": {
        "createdBy": "developer",
        "createdAt": 1562085005593,
        "id": 5,
        "name": "NAMA PERUSAHAAN",
        "code": "S1562085478146",
        "type": "SHIPPER",
        "status": "INACTIVE",
        "averageRating": 3,
        "imageUrl": "http://placehold.it/200"
    }
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:15:52.444+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL tidak ditemukan",
    "data": null
}
```

>  **<span style='color:#DF7401'>*400 Bad Request*</span>**

```json
{
    "timestamp": "2019-07-02T17:16:11.228+0000",
    "status": "Bad Request",
    "statusCode": 400,
    "message": "Data customer/rekanan 3PL sudah tidak aktif",
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

`POST /api/v1/identity/clients/<ID>/deactive`

### Header

`Authorization: Bearer [access_token]`

### URL Parameter

Parameter | Description
--------- | -----------
ID <br> <small>required</small>  | client id



## Retrieve client list 

This endpoint used for retrieve client based parameter

>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:22:28.485+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": [
        {
            "createdBy": "developer",
            "createdAt": 1562052502644,
            "id": 3,
            "name": "TRANSPORTER 1",
            "code": "T1562052643552",
            "type": "TRANSPORTER",
            "status": "ACTIVE",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/200"
        },
        {
            "createdBy": "developer",
            "createdAt": 1562051992605,
            "id": 2,
            "name": "SHIPPER",
            "code": "S1562052367129",
            "type": "SHIPPER",
            "status": "ACTIVE",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/200"
        },
        {
            "createdBy": "admin",
            "createdAt": 1562052502000,
            "id": 1,
            "name": "Developer",
            "code": "Developer",
            "type": "DEVELOPER",
            "status": "ACTIVE",
            "averageRating": 3,
            "imageUrl": "http://placehold.it/100"
        }
    ]
}
```
>  **<span style='color:#04B404'>*200 OK*</span>**

```json
{
    "timestamp": "2019-07-02T17:23:55.208+0000",
    "status": "OK",
    "statusCode": 200,
    "message": "OK",
    "data": []
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

`GET /api/v1/identity/clients/list`

### Header

`Authorization: Bearer [access_token]`

### Query Parameter

Parameter | Description
--------- | -----------
id <br> <small>required</small>  | `string[]` client id

