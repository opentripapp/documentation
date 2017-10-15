# Account

## Register

> Result

```json
{
  "error": false,
  "data": {
    "updatedAt": "2017-05-23T02:12:41.283Z",
    "createdAt": "2017-05-23T02:12:41.283Z",
    "name": "arizal",
    "_id": "59239a99feb15e3830fd8813",
    "point": 0,
    "interest": [],
    "gender": 2,
    "block": 0,
    "following": 0,
    "email": {
      "data": "tes@tes.com",
      "verified": false
    },
    "followers": 0,
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjM5YTk5ZmViMTVlMzgzMGZkODgxMyIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJpYXQiOjE0OTU1MDU1NjEsImV4cCI6MTUwMDY4OTU2MX0.1ezJfr7oS525SZIk9cMAvIYcmypQiF9qHWvGWtQJsYk",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjM5YTk5ZmViMTVlMzgzMGZkODgxMyIsInR5cGUiOiJyZWZyZXNoX3Rva2VuIiwiaWF0IjoxNDk1NTA1NTYxLCJleHAiOjE1MjcwNjMxNjF9.jVyoVDUNEF6UFcKkDrsLcmyzQhHGMr717btMnxEteJ4"
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

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Login Manual

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
       "profile_cover": "api.arizalsaputro.net",
       "profile_picture": "www.arizalsaputro.net",
       "point": 0,
       "interest": [
         "apaya",
         "ehh"
       ],
       "gender": 1,
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
       "followers": 0
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNTI0NjUxOGJiMjlkODE1OTc3MSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJpYXQiOjE0OTU0MjUzODgsImV4cCI6MTUwMDYwOTM4OH0.8AP4seI3HOCiJqP-2QXzr46MzpNkPca80lm1crgdV7A",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNTI0NjUxOGJiMjlkODE1OTc3MSIsInR5cGUiOiJyZWZyZXNoX3Rva2VuIiwiaWF0IjoxNDk1NDI1Mzg4LCJleHAiOjE1MjY5ODI5ODh9.CE2cKlVzuyzfduwl7OGC1JzzkRJni-ctPNn4ZhsqzV0"
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

## Instagram Login

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
    "profile_cover": "api.arizalsaputro.net",
    "profile_picture": "www.arizalsaputro.net",
    "point": 0,
    "interest": [
      "apaya",
      "ehh"
    ],
    "gender": 1,
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
    "followers": 0
    "id_instagram": "1574083",
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNWM0YjlmZmIyMmFjNGI1OGUzYyIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJpYXQiOjE0OTU0MjU3MzQsImV4cCI6MTUwMDYwOTczNH0.PV5me3Ljcy4EYjVk4pkRx97jyvFGmHFpM502qk-6rGA",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNWM0YjlmZmIyMmFjNGI1OGUzYyIsInR5cGUiOiJyZWZyZXNoX3Rva2VuIiwiaWF0IjoxNDk1NDI1NzM0LCJleHAiOjE1MjY5ODMzMzR9.r9KeRQ4Gp9mhb1Fk-DCpqfzgI4LmwM0lqFyOuwxltBE"
  }
}
```

User login application with instagram account.


### Endpoint

`POST /user/login_instagram`

### Parameters

Parameter | Required | Description
--------- | ---------| -----------
access_token | true | user access_token by instagram account
id | true | user id instagram account
username | true | username instagram account
profile_picture | false | user profile picture
full_name | false | user full_name of instagram account


## Forget Password

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


## Verify Email

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



## Verify Phone Number

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

## RefreshToken

> Result

```json
{
  "error": false,
  "data": {
    "_id": "5921e5246518bb29d8159771",
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNTI0NjUxOGJiMjlkODE1OTc3MSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJpYXQiOjE0OTU0Mjc4NDQsImV4cCI6MTUwMDYxMTg0NH0.BkdPTO-H2NnB-kWxxPTDLpclc9L7pa-h7TRAuCGLtUc",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjU5MjFlNTI0NjUxOGJiMjlkODE1OTc3MSIsInR5cGUiOiJyZWZyZXNoX3Rva2VuIiwiaWF0IjoxNDk1NDI3ODQ0LCJleHAiOjE1MjY5ODU0NDR9.CRzb1_c2d536-bn-QG0JaDze5fAdyAHIwDcDT29R2eM"
  }
}
```

Get user access_token, use this then access_token was expired

### Endpoint

`GET /user/refresh_token`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | refresh_token | `Authorization: Bearer <refresh_token>`

<aside class="notice">
You must replace <code>refresh_token</code> with refresh_token.
Remember! header is <code>refresh_token</code> , NOT <code>access_token</code>
</aside>


## Delete Account

> Result

```json
{
  "error": false,
}
```

Deleting using account, password require for deleting account.account will deleted permanent.

### Endpoint

`DELETE /user/account`

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
password | true | user current password.
reason_code | true | why delete account ?.

### reason_code

code | Description
---- | -----------
1    | Trouble getting started
2    | Created a second account
3    | Privacy concerns
4    | Want to remove something
5    | Too busy/too distracting
6    | Can't find people to follow
7    | Too many ads
something else | why ?

