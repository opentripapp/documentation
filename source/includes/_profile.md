# Profile

## Get User Profile

```shell
curl -X GET \
  https://api.opentripapp.com/user/profile?id=59c63a5fe0bc2400117a87fc \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'x-api-key: YOUR_API_KEY' \
```

> Result

```json
{
    "error": false,
    "data": {
        "_id": "59c63a5fe0bc2400117a87fc",
        "updatedAt": "2018-02-20T15:03:44.705Z",
        "createdAt": "2017-09-23T10:41:35.643Z",
        "name": "Open Trip Official",
        "rating": {
            "point": 5,
            "count": 2
        },
        "point": 0,
        "interest": [
            "Traveling",
            " Networking",
            " Having Fun"
        ],
        "gender": 1,
        "block": 0,
        "hide_post": [],
        "following": 9,
        "email": {
            "data": "hello@opentripapp.com",
            "verified": false
        },
        "__v": 1,
        "phone_number": {
            "data": "08118808877",
            "verified": true
        },
        "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c63a5fe0bc2400117a87fc_81bba8be06307fce.jpg",
        "profile_cover": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c63a5fe0bc2400117a87fc_ae020d420134dcf2.jpg",
        "address": "Bandung",
        "birth_date": "2017-03-04T00:00:00.000Z",
        "bio": "Make Friends Along the Way",
        "verified": false,
        "status": {
            "last_active": "2018-02-20T15:03:44.704Z",
            "online": false
        },
        "follow_you": false,
        "is_follow": true,
        "followers": 5,
        "open_trips": 1
    }
}
```

Get user data profile by id

### Endpoint

`GET /user/profile`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
id | true | user id `_id`

## Get Other User Profile (Withour Auth)
```shell
curl -X GET \
  https://api.opentripapp.com/user/other_profile?id=59c63a5fe0bc2400117a87fc \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'x-api-key: YOUR_API_KEY' \
```


> Result

```json
{
    "error": false,
    "data": {
        "_id": "59c63a5fe0bc2400117a87fc",
        "updatedAt": "2018-02-20T15:03:44.705Z",
        "createdAt": "2017-09-23T10:41:35.643Z",
        "name": "Open Trip Official",
        "rating": {
            "point": 5,
            "count": 2
        },
        "point": 0,
        "interest": [
            "Traveling",
            " Networking",
            " Having Fun"
        ],
        "gender": 1,
        "block": 0,
        "hide_post": [],
        "following": 9,
        "email": {
            "data": "hello@opentripapp.com",
            "verified": false
        },
        "__v": 1,
        "phone_number": {
            "data": "08118808877",
            "verified": true
        },
        "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c63a5fe0bc2400117a87fc_81bba8be06307fce.jpg",
        "profile_cover": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c63a5fe0bc2400117a87fc_ae020d420134dcf2.jpg",
        "address": "Bandung",
        "birth_date": "2017-03-04T00:00:00.000Z",
        "bio": "Make Friends Along the Way",
        "verified": false,
        "status": {
            "last_active": "2018-02-20T15:03:44.704Z",
            "online": false
        },
        "follow_you": false,
        "is_follow": true,
        "followers": 5,
        "open_trips": 1
    }
}
```

Get user data profile by id without authentication

### Endpoint

`GET /user/other_profile`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
id | true | user id `_id`


## Update User Profile

```shell
curl -X PUT \
  https://api.opentripapp.com/user/update \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
    "name":"lala"
  }'
```


> Result

```json
{
    "error": false,
    "data": {
        "_id": "59c5c89665a538001088798f",
        "updatedAt": "2018-06-12T07:53:41.054Z",
        "createdAt": "2017-09-23T02:36:06.225Z",
        "name": "new arizal",
        "rating": {
            "point": 0,
            "count": 0
        },
        "point": 28,
        "interest": [],
        "gender": 2,
        "block": 0,
        "hide_post": [],
        "following": 7,
        "email": {
            "verified": true,
            "data": "muhammadarizals1@gmail.com"
        },
        "phone_number": {
            "verified": true,
            "data": "085722244744"
        },
        "__v": 0,
        "notification": {
            "is_login": true
        },
        "profile_picture": "https://d25b0guxzp2dqx.cloudfront.net/images/large/59c5c89665a538001088798f_2bb6e8d9c44bbded.jpg",
        "profile_cover": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_701c6df0bcb6a571.jpg",
        "identity_card": {
            "data": "https://images3.alphacoders.com/823/82317.jpg",
            "verified": false
        },
        "bio": "",
        "birth_date": null,
        "address": "",
        "is_suspend": false,
        "status": {
            "last_active": "2018-02-20T14:56:52.704Z",
            "online": false
        },
        "is_leader": true,
        "verified": false,
        "follow_you": false,
        "is_follow": false,
        "followers": 1,
        "open_trips": 8
    }
}
```

You can update user profile using this endpoint.

### Endpoint

`PUT /user/update`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Body Parameters

Parameter | Required | Description | Type
--------- | ------- | -----------| -----------
email | optional | new user email address | email
birth_date | optional | new user birth date | UNIX TIMESTAMP
interest | optional | new user interest on | Array of String `["a","b","c"]`
gender | optional | new user gender | 0/1/2
phone_number | optional | new user phone_number | phone numeber (62 ....)
name | optional | new user name | String
bio | optional | new user bio | String
address | optional | new user address | String
identity_card | optional | new user identity_card `ktp` | Url image adresss
profile_cover | optional | new user cover photo | Url image adresss
profile_picture | optional | new user profile photo | Url image adresss
device_token | optional | update user device token | to send post notification

<aside class="notice">
You can use `json` type on body request
</aside>

<aside class="notice">
example phone_number `6285722244744`
</aside>


<aside class="notice">
<code>gender</code> :
0 : <code>MALE</code>
1: <code>FEMALE</code>
2: <code>UNKNOWN</code>
</aside>

<aside class="notice">
When you updating phone number user will receive sms verification
</aside>

## Upload Photo Profile

```shell
curl -X POST \
  http://localhost:8005/media/upload/profile \
   -H 'accept-language: en' \
    -H 'api-client: android' \
    -H 'cache-control: no-cache' \
    -H 'content-type: application/json' \
    -H 'device-id: 123' \
    -H 'Authorization: Bearer TOKEN'
    -H 'x-api-key: YOUR_API_KEY' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 5d0a0e1d-3053-99d9-ca92-7a85d2e644db' \
  -F file=@1470.jpg
```

> Success Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-06-04T02:04:59.575Z",
    "_id": "5933658b705c0a671c510acd",
    "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/5933658b705c0a671c510acd4ab69878b7e6c88f.jpg"
  }
}
```
### Endpoint

`POST /media/upload/profile`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
file | true | file of the image

## Upload Photo Cover
```shell
curl -X POST \
  http://localhost:8005/media/upload/cover \
   -H 'accept-language: en' \
    -H 'api-client: android' \
    -H 'cache-control: no-cache' \
    -H 'content-type: application/json' \
    -H 'device-id: 123' \
    -H 'Authorization: Bearer TOKEN'
    -H 'x-api-key: YOUR_API_KEY' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 5d0a0e1d-3053-99d9-ca92-7a85d2e644db' \
  -F file=@1470.jpg
```

> Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-06-04T02:04:59.575Z",
    "_id": "5933658b705c0a671c510acd",
    "profile_cover": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/5933658b705c0a671c510acd4ab69878b7e6c88f.jpg"
  }
}
```
### Endpoint

``POST /media/upload/cover``

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
file | true | file of the image

## Upload Identity Card
> Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-06-04T02:04:59.575Z",
    "_id": "5933658b705c0a671c510acd",
    "identity_card":{
            "data":"https://url.image",
            "verified":false
     }
  }
}
```
### Endpoint

``POST /media/upload/identity_card``

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
file | true | file of the image



## Delete Photo Profile
> Success Result

```json
{
  "error": false,
  "data": {
    "_id": "5933658b705c0a671c510acd"
  }
}
```
### Endpoint

`DELETE /media/delete/profile`

## Delete Profile Cover
> Success Result

```json
{
  "error": false,
  "data": {
    "_id": "5933658b705c0a671c510acd"
  }
}
```
### Endpoint

`DELETE /media/delete/cover`


## Delete Identity Card
> Success Result

```json
{
  "error": false,
  "data": {
    "_id": "5933658b705c0a671c510acd"
  }
}
```
### Endpoint

`DELETE /media/delete/identity_card`
