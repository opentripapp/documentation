# Account

## Register

```shell
curl -X POST \
  https://api.opentripapp.com/user/register \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'postman-token: 60b98299-e595-bbc0-9ace-9f1276fa618c' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
  "name":"vita",
  "password":"123456",
  "email":"te2s@te2se3ed3e3d.coms",
  "referral_code":"muhammadarizals1@gmail.com",
  "referral_type":"email"
}'
```

> Result

```json
{
    "error": false,
    "data": {
        "email": {
            "data": "te2s@te2se3ed3e3d.coms",
            "verified": false
        },
        "rating": {
            "point": 0,
            "count": 0
        },
        "following": 0,
        "hide_post": [],
        "block": 0,
        "gender": 2,
        "interest": [],
        "point": 0,
        "is_leader": false,
        "verified": false,
        "_id": "5b1f72af78391d0005c82705",
        "name": "vita",
        "referral_code": "TE2S890F",
        "createdAt": "2018-06-12T07:13:51.843Z",
        "updatedAt": "2018-06-12T07:13:51.843Z",
        "__v": 0,
        "followers": 0,
        "access_token": "some access token"
    }
}
```

Register a new user using email and password

### Endpoint

`POST /user/register`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
name | true | Fullname for new user
email | true | Email for new user
password | true | Password for new user
referral_code | optional | referral link or code or email or phone
referral_type | optional | type of referral code `email` or `phone_number` default `code`

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Login

```shell
curl -X POST \
  https://api.opentripapp.com/user/login \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'postman-token: 7adbf8df-461e-3400-6993-ef974dd65437' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
  "password":"lala",
  "email":"lala@gmail.com"
}'
```

> Result

```json
{
    "error": false,
    "data": {
        "email": {
            "data": "myemail@email.com",
            "verified": true
        },
        "phone_number": {
            "data": "085722244745",
            "key": "4789",
            "verified": true
        },
        "identity_card": {
            "verified": false,
            "data": null
        },
        "notification": {
            "is_login": true
        },
        "rating": {
            "point": 0,
            "count": 0
        },
        "status": {
            "last_active": "2018-06-12T05:52:43.963Z",
            "online": false
        },
        "following": 19,
        "hide_post": [],
        "block": 0,
        "gender": 1,
        "interest": [],
        "point": 0,
        "is_leader": false,
        "verified": false,
        "_id": "59c5c89665a538001088798f",
        "updatedAt": "2018-06-12T05:52:43.963Z",
        "createdAt": "2017-09-23T02:36:06.225Z",
        "name": "arizal saputro",
        "__v": 0,
        "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media-20f95100/media/59c5c89665a538001088798f_103a61372d1a1561.jpg",
        "profile_cover": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_701c6df0bcb6a571.jpg",
        "birth_date": "2017-10-11T00:00:00.000Z",
        "bio": "",
        "address": "",
        "is_suspend": false,
        "referral_code": "1373K464M4FMF607K",
        "access_token": "some access token",
        "followers": 5
    }
}
```

User login application with email and password.

### Endpoint

`POST /user/login`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
email | true | Email for identifier
password | true | Password for identifier


## Forget Password

```shell
curl -X POST \
  https://api.opentripapp.com/user/forget_password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
	"email":"muhammadarizals1@gmail.com"
}'
```

> Result

```json
{
    "error": false,
}
```

User will receive email to reset password


### Endpoint

`POST /user/forget_password`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
email | true | Registered email address

## Reset Password

```shell
curl -X POST \
  https://api.opentripapp.com/user/reset_password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
      	"new_password":"pasiamo1",
      	"key":"ULOGOHeRf7gdjuztEHTMBCPo70tsbWMvoncVVvSj"
      }'
```

> Result

```json
{
    "error": false,
}
```

Reset password user if forget the password

### Endpoint

`POST /user/reset_password`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
key | true | unique key
new_password | true | new password


## Change Password

```shell
curl -X POST \
  https://api.opentripapp.com/user/update/password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
      	"old_password":"pasiamo5",
      	"new_password":"pasiamo1"
      }'
```

> Result

```json
{
  "error": false
}
```

Updating user password

### Endpoint

`PUT /user/update/password`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
old_password | true | user old password
new_password | true | user new password

## Change Email

> Result

```json
{
  "error": false
}
```

Updating user email address

### Endpoint

`PUT /user/update/email`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
email | true | new user email address



## Verify Email

```shell
curl -X POST \
  https://api.opentripapp.com/user/confirm_email \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
      	"key":"Dic673RTTS4InOqsQrTwRn1qBTfWLufRdVXa7cJz"
      }'
```


> Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-05-22T04:27:23.049Z",
    "_id": "5921e5246518bb29d8159771",
    "email": {
      "data": "tes@tes.com",
      "verified": true
    }
  }
}
```

To verify user email address


### Endpoint

`PUT /user/confirm_email`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
key | true | Unique key from to verify email address

## Add Phone Number

```shell
curl -X POST \
  https://api.opentripapp.com/user/update/password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
      	"phone_number":"0857222444444"
      }'
```

> Result

```json
{
  "error": false,
}
```

Adding phone number to user

### Endpoint

`PUT /user/add_phone_number`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
phone_number | true | phone number

## Resend OTP Code

```shell
curl -X POST \
  https://api.opentripapp.com/user/update/password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
```

> Result

```json
{
  "error": false,
}
```

Adding phone number to user

### Endpoint

`POST /user/resend_otp_code`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

## Resend Email Verification

> Result

```json
{
  "error": false,
}
```

Adding phone number to user

### Endpoint

`POST /user/resend_email_verification`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`



## Verify Phone Number

```shell
curl -X POST \
  https://api.opentripapp.com/user/update/password \
  -H 'accept-language: en' \
  -H 'api-client: android' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'device-id: 123' \
  -H 'Authorization: Bearer TOKEN'
  -H 'postman-token: 0404599d-358f-e444-0273-4979738b255e' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{
      	"code":"1234"
      }'
```
> Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-05-22T04:27:23.049Z",
    "_id": "5921e5246518bb29d8159771",
    "phone_number": {
      "data": "085641030148",
      "verified": true
    }
  }
}
```

To verify user phone number


### Endpoint

`PUT /user/verify/phone_number`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
code | true | phone number verification code
