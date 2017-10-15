# Social

## Get User Following

> Result

```json
{
  "error": false,
  "data": [
    {
      "_id": "5923cfc450434044b836c3b8",
      "profile_picture": "image url profile picture",
      "name": "arizal"
    },
    {
      "_id": "592510f6f856d02284b2f44b",
      "profile_picture": "image url profile picture"
      "name": "bibibi testititititi"
    },
    {
      "_id": "59251006f856d02284b2f44a",
      "profile_picture": "image url profile picture"
      "name": "testititititi"
    }
  ]
}
```

Get user data following by id

### Endpoint

`GET /user/social/following`

### Query Parameters

Parameter | Required |  Type     | Description
--------- | ------- | -----------| --------
id | true | id | user id `_id`
limit | optional | number | how much data
offset | optional | number | from where

<aside class="notice">
default limit : <code>15</code> offset : <code>0</code>
</aside>


## Get User Followers

> Result

```json
{
  "error": false,
  "data": [
    {
      "_id": "5923cfc450434044b836c3b8",
      "profile_picture": "image url profile picture",
      "name": "arizal"
    },
    {
      "_id": "592510f6f856d02284b2f44b",
      "profile_picture": "image url profile picture"
      "name": "bibibi testititititi"
    },
    {
      "_id": "59251006f856d02284b2f44a",
      "profile_picture": "image url profile picture"
      "name": "testititititi"
    }
  ]
}
```

Get user data followers by id

### Endpoint

`GET /user/social/followers`

### Query Parameters

Parameter | Required |  Type     | Description
--------- | ------- | -----------| --------
id | true | id | user id `_id`
limit | optional | number | how much data
offset | optional | number | from where

<aside class="notice">
default `limit : <code>15</code> offset : <code>0</code>
</aside>


## Get User Blocked

> Result

```json
{
  "error": false,
  "data": [
    {
      "_id": "5923cfc450434044b836c3b8",
      "profile_picture": "image url profile picture",
      "name": "arizal"
    },
    {
      "_id": "592510f6f856d02284b2f44b",
      "profile_picture": "image url profile picture"
      "name": "bibibi testititititi"
    },
    {
      "_id": "59251006f856d02284b2f44a",
      "profile_picture": "image url profile picture"
      "name": "testititititi"
    }
  ]
}
```

Get user data following by id

### Endpoint

`GET /user/social/blocked`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>


### Query Parameters

Parameter | Required |  Type     | Description
--------- | ------- | -----------| --------
limit | optional | number | how much data
offset | optional | number | from where

<aside class="notice">
default limit : <code>15</code> offset : <code>0</code>
</aside>



## Action Follow

> Result

```json
{
  "error": false
}
```
You can follow another user profile using this endpoint.

### Endpoint

`POST /user/social/action/follow`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to follow

## Action Unfollow

> Result

```json
{
  "error": false
}
```
You can unfollow another user profile using this endpoint.

### Endpoint

`POST /user/social/action/unfollow`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to unfollow

## Action Block

> Result

```json
{
  "error": false
}
```
You can block another user profile using this endpoint.

### Endpoint

`POST /user/social/action/block`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to block

## Action Unblock

> Result

```json
{
  "error": false
}
```
You can block another user profile using this endpoint.

### Endpoint

`POST /user/social/action/unblock`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to unblock

## Action Report

> Result

```json
{
  "error": false
}
```
report user, when you report user, you automatically blocking that user.

### Endpoint

`POST /user/social/action/report`

### Header

Name | Required | Description | example
--------- | ---------| -----------| -------------
Authorization | true | access_token | `Authorization: Bearer <access_token>`

<aside class="notice">
You must replace <code>access_token</code> with access_token.
</aside>

### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to report
reason_code| true | reason why user report another user.

### reason_code

code | Description
---- | -----------
1    | it's spam
2    | it`s inappropriate
something else | why ?

## Action Review

> Result

```json
{
    "error": false,
    "data": {
        "point": 3,
        "from": "594b57fac0f7361678bbec5b",
        "to": "594b5978c0f7361678bbec60",
        "comment": "aa payah",
        "_id": "594b598ac0f7361678bbec61"
    }
}
```
review another user

### Endpoint

`POST /user/social/action/review`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | another user id to review
point | true | point rating `0` to `5`
comment | optional | review comment

## Get User Review

> Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "594b598ac0f7361678bbec61",
            "updatedAt": "2017-06-22T05:45:46.662Z",
            "createdAt": "2017-06-22T05:45:46.662Z",
            "point": 3,
            "from": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal",
                "profile_picture": "https://alamat"
            },
            "to": "594b5978c0f7361678bbec60",
            "comment": "aa payah",
            "__v": 0
        },
        {
            "_id": "594b598ac0f7361678bbec61",
            "updatedAt": "2017-06-22T05:45:46.662Z",
            "createdAt": "2017-06-22T05:45:46.662Z",
            "point": 3,
            "from": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal"
                "profile_picture": "https://alamat"
            },
            "to": "594b5978c0f7361678bbec60",
            "comment": "aa payah",
            "__v": 0
        }
        ...
        ...
        ...
    ]
}
```
get user review data

### Endpoint

`GET /user/social/review`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | id user untuk diambil reviewnya
sort | optional | `createdAt` is default sort
limit | optional | `10` is default limit
offset | optional | `0` is default offset

## Get My Review

> Result

```json
{
    "error": false,
    "data": {
        "_id": "594b598ac0f7361678bbec61",
        "updatedAt": "2017-06-22T05:45:46.662Z",
        "createdAt": "2017-06-22T05:45:46.662Z",
        "point": 3,
        "from": "594b57fac0f7361678bbec5b",
        "to": "594b5978c0f7361678bbec60",
        "comment": "aa payah",
        "__v": 0
    }
}
```
get user review to another user.

### Endpoint

`GET /user/social/my_review`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
id | true | id user untuk diambil reviewnya
