# Profile

## Upload Device Token
> Success Result

```json
{
  "error": false,
}
```
### Endpoint

to update user device fcm token, to send push notification.

`PUT /user/update/token`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
device_token | true | device generated token for fcm


## Get User Profile

> Result

```json
{
  "error": false,
  "data": {
    "_id": "59239a99feb15e3830fd8813",
    "updatedAt": "2017-05-23T02:15:21.075Z",
    "createdAt": "2017-05-23T02:12:41.283Z",
    "name": "njayen",
    "address": "jalan jalan",
    "bio": "Gas",
    "birth_date": "1970-01-18T07:24:20.306Z",
    "profile_cover": "url alamat cover",
    "profile_picture": "url alamat cover",
    "point": 0,
    "interest": [
      "apaya",
      "ehh"
    ],
    "gender": 0,
    "block": 0,
    "following": 0,
    "phone_number": {
      "data": "08783666786",
      "verified": false
    },
    "email": {
      "data": "muhammadarizals1@gmail.com",
      "verified": false
    },
    "followers": 0,
    "follow_you":false
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




## Update User Profile

> Result

```json
{
  "error": false,
  "data": {
    "_id": "59239a99feb15e3830fd8813",
    "updatedAt": "2017-05-23T02:47:28.727Z",
    "createdAt": "2017-05-23T02:12:41.283Z",
    "name": "njayen baru",
    "address": "jl sukarn hatta bandung",
    "bio": "Logi",
    "birth_date": "1970-01-18T07:24:20.306Z",
    "profile_cover": "cover bary",
    "profile_picture": "url alamat profile picture baru",
    "point": 0,
    "interest": [
      "apaya",
      "ehh"
    ],
    "gender": 1,
    "block": 0,
    "following": 0,
    "phone_number": {
      "data": "14045",
      "verified": false
    },
    "email": {
      "data": "muhammadarizals2@gmail.com",
      "verified": false
    },
    "followers": 0
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

### Query Parameters

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
