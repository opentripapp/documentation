#Review and Rating

## Get Waiting List review

> Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "59da0cab2b48470010a8c865",
            "_leader": {
                "_id": "59c85563d6a8840010b91479",
                "name": "tryon lannister"
            },
            "date": {
                "end": "2017-10-13T17:00:00.000Z",
                "start": "2017-10-12T17:00:00.000Z"
            },
            "_trip": {
                "_id": "59da0cac2b48470010a8c866",
                "main_image": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c85563d6a8840010b91479_02dff637b986d163.jpg",
                "title": "Boyolali trip",
                "destination": "Boyolali"
            }
        },
        ...
        ...
        ...
    ]
}
```

get waiting list to review

### Endpoint

`GET /user/social/review/waiting`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
sort | optional | `date.end` is default sort
limit | optional | `50` is default limit
offset | optional | `0` is default offset



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
user_id | true | another user id to review or `_leader._id` from waiting list review
review_id | true | review id from `_id` waiting list review
point | true | point rating `0` to `5`
title | optional | review title
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
