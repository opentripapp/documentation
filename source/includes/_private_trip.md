# Private Trip

## Create Request Private Trip
> Success Result

```json
{
    "error": false,
    "data": {
        "__v": 0,
        "updatedAt": "2018-01-30T05:30:38.569Z",
        "createdAt": "2018-01-30T05:30:38.569Z",
        "_author": "59c5c89665a538001088798f",
        "destination": "bali",
        "date": "2018-05-21T00:00:00.000Z",
        "phone_number": "12121212",
        "how_many": 1,
        "name": "njayen",
        "_id": "5a7002fe3b7b3117ac831e18"
    }
}
```

create private trip request

### Endpoint

`POST /trip/private_trip`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
destination  | true    | destination name
date    | true | date of trip `yyyy-mm-dd` format
phone_number | true | user phone number
how_many | true | how many private trip member
name        | optional    | user name or ??
location    | optional    | metting point location, use array  `[longitude,latitude]`

## Get Request Private Trip
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "5a7002fe3b7b3117ac831e18",
            "updatedAt": "2018-01-30T05:30:38.569Z",
            "createdAt": "2018-01-30T05:30:38.569Z",
            "_author": {
                "_id": "59c5c89665a538001088798f",
                "name": "arizal",
                "email": {
                    "data": "muhammadarizals1@gmail.com"
                },
                "phone_number": {
                    "data": "+6285722244744"
                },
                "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_dd4e289d20617520.jpg"
            },
            "destination": "bali",
            "date": "2018-05-21T00:00:00.000Z",
            "phone_number": "12121212",
            "how_many": 1,
            "name": "njayen",
            "__v": 0
        },
        {
            "_id": "5a70052170130c43e098b2be",
            "updatedAt": "2018-01-30T05:39:45.463Z",
            "createdAt": "2018-01-30T05:39:45.463Z",
            "_author": {
                "_id": "59c5c89665a538001088798f",
                "name": "arizal",
                "email": {
                    "data": "muhammadarizals1@gmail.com"
                },
                "phone_number": {
                    "data": "+6285722244744"
                },
                "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_dd4e289d20617520.jpg"
            },
            "destination": "jakarta",
            "date": "2018-05-21T00:00:00.000Z",
            "phone_number": "12121212",
            "how_many": 4,
            "name": "njayen",
            "__v": 0
        }
    ]
}
```

get private trip request

### Endpoint

`GET /trip/private_trip`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | optional   | `0` default offset is `0`
limit     | optional   | `10` default limit is `15`
sort    | optional   | sorting
how_many | optional | number
destination | optional | destination name

## Get My Request Private Trip
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "5a7002fe3b7b3117ac831e18",
            "updatedAt": "2018-01-30T05:30:38.569Z",
            "createdAt": "2018-01-30T05:30:38.569Z",
            "_author": {
                "_id": "59c5c89665a538001088798f",
                "name": "arizal",
                "email": {
                    "data": "muhammadarizals1@gmail.com"
                },
                "phone_number": {
                    "data": "+6285722244744"
                },
                "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_dd4e289d20617520.jpg"
            },
            "destination": "bali",
            "date": "2018-05-21T00:00:00.000Z",
            "phone_number": "12121212",
            "how_many": 1,
            "name": "njayen",
            "__v": 0
        },
        {
            "_id": "5a70052170130c43e098b2be",
            "updatedAt": "2018-01-30T05:39:45.463Z",
            "createdAt": "2018-01-30T05:39:45.463Z",
            "_author": {
                "_id": "59c5c89665a538001088798f",
                "name": "arizal",
                "email": {
                    "data": "muhammadarizals1@gmail.com"
                },
                "phone_number": {
                    "data": "+6285722244744"
                },
                "profile_picture": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/59c5c89665a538001088798f_dd4e289d20617520.jpg"
            },
            "destination": "jakarta",
            "date": "2018-05-21T00:00:00.000Z",
            "phone_number": "12121212",
            "how_many": 4,
            "name": "njayen",
            "__v": 0
        }
    ]
}
```

get private trip request

### Endpoint

`GET /trip/private_trip/me`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | optional   | `0` default offset is `0`
limit     | optional   | `10` default limit is `15`
sort    | optional   | sorting
how_many | optional | number
destination | optional | destination name

## Delete My Request Private Trip
> Success Result

```json
{
    "error": false
}
```

delete private trip request

### Endpoint

`DELETE /trip/private_trip`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id    | true   | request id


