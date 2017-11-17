#Booking

##Get Order ID
> Success Result

```json
{
    "error": false,
    "data":{
        "booking_code":"OPIJDNK"
        "amount":"10000"
    }
}
```
get order id to (this is for mobile sdk)

### Endpoint

`POST /booking/get_order_id`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id   | true    | trip `_id`
joined_id |true |  `_joined_id` of field in date trip
promo_code| false | voucher code

<aside class="notice">
The time to make the payment process is 1 day until the order will be canceled.
time to process payment : 5 minute
time to complete payment : 1 day
</aside>



##Get Payment Token
> Success Result

```json
{
    "error": false,
    "data":{
        "token":"easas-asdasd-asdasd",
        "booking_code":"OPIJDNK"
    }
}
```
get payament token to pay trip

### Endpoint

`POST /booking/get_payment_token`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id   | true    | trip `_id`
joined_id |true |  `_joined_id` of field in date trip
promo_code| false | voucher code

<aside class="notice">
The time to make the payment process is 60 minutes until the order will be canceled.
time to process payment : 15 minute
time to complete payment : 45 minute
</aside>


##Get Order ID (Multiple)
> Success Result

```json
{
    "error": false,
    "data": {
        "booking_code": "OP7N9YCYD5DI",
        "amount": 155000,
        "type": "multiple",
        "users_paid_count": 1,
        "promo_code": "59ef58d6a0306f909071fbf4",
        "original_price": 165000
    }
}
```

> Already Join Trip

```json
{
    "error": true,
    "code": "UNKNOWN_ERROR",
    "message": "Something went wrong, muhammadarizals1@gmail.com are already joining this trip"
}

```

> Contain Trip Leader

```json
{
    "error": true,
    "code": "UNKNOWN_ERROR",
    "message": "Something went wrong, smarthap@gmail.com are the leader of this trip"
}
```

> Trip Quota Insufficient

```json
{
    "error": true,
    "code": "QUOTA_INSUFFICIENT",
    "message": "The remaining quota is insufficient, only 2 left"
}
```

> Promo Code Error

```json
{
    "error": true,
    "code": "PROMO_CODE_EXPIRED",
    "message": "Promo code has expired"
}

{
    "error": true,
    "code": "INVALID_PROMO_CODE",
    "message": "Promo code does not work for this trip"
}

{
    "error": true,
    "code": "PROMO_CODE_EXPIRED",
    "message": "Promo period not valid yet"
}

```



get order id to (this is for mobile sdk) support multiple payment.

### Endpoint

`POST /booking/multiple/get_order_id`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id   | true    | trip `_id`
joined_id |true |  `_joined_id` of field in date trip
users | true | array of users email to be paid
promo_code| false | voucher code

<aside class="notice">
for once usage promo_code only work when user never use that promo_code before
</aside>


<aside class="notice">
The time to make the payment process is 1 day until the order will be canceled.
time to process payment : 5 minute
time to complete payment : 1 day
</aside>


##Get Payment Token (Multiple)
> Success Result

```json
{
    "error": false,
    "data": {
        "booking_code": "OP7N9YCYD5DI",
        "amount": 155000,
        "type": "multiple",
        "users_paid_count": 1,
        "promo_code": "59ef58d6a0306f909071fbf4",
        "original_price": 165000,
        "token": "6f611fa7-9149-4a42-83a6-897d63281bbe",
        "redirect_url": "https://app.midtrans.com/snap/v2/vtweb/6f611fa7-9149-4a42-83a6-897d63281bbe"
    }
}
```

> Already Join Trip

```json
{
    "error": true,
    "code": "UNKNOWN_ERROR",
    "message": "Something went wrong, muhammadarizals1@gmail.com are already joining this trip"
}

```

> Contain Trip Leader

```json
{
    "error": true,
    "code": "UNKNOWN_ERROR",
    "message": "Something went wrong, smarthap@gmail.com are the leader of this trip"
}
```

> Trip Quota Insufficient

```json
{
    "error": true,
    "code": "QUOTA_INSUFFICIENT",
    "message": "The remaining quota is insufficient, only 2 left"
}
```

> Promo Code Error

```json
{
    "error": true,
    "code": "PROMO_CODE_EXPIRED",
    "message": "Promo code has expired"
}

{
    "error": true,
    "code": "INVALID_PROMO_CODE",
    "message": "Promo code does not work for this trip"
}

{
    "error": true,
    "code": "PROMO_CODE_EXPIRED",
    "message": "Promo period not valid yet"
}

```



get payment token to (this is for web snap) support multiple payment.

### Endpoint

`POST /booking/multiple/get_payment_token`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id   | true    | trip `_id`
joined_id |true |  `_joined_id` of field in date trip
users | true | array of users email to be paid
promo_code| false | voucher code

<aside class="notice">
for once usage promo_code only work when user never use that promo_code before
</aside>


<aside class="notice">
The time to make the payment process is 1 day until the order will be canceled.
time to process payment : 5 minute
time to complete payment : 1 day
</aside>




##Cancel Booking
> Success Result

```json
{
    "error": false
}
```
to cancel booking, note this is cancel booking not cancel join trip
### Endpoint

`POST /booking/cancel`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
booking_code| false | voucher code

##Get Booked Trip
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "598adeaea907bd6aee3928b5",
            "_leader": {
                "_id": "5927f48c8553514047eee97c",
                "name": "tes"
            },
            "date": {
                "start": "2017-09-01T00:00:00.000Z",
                "end": "2017-09-01T00:00:00.000Z"
            },
            "_trip": {
                "_id": "598adeaea907bd6aee3928b6",
                "main_image": "https:///tes",
                "title": "tes",
                "destination": "Tangkuban Perahu"
            },
            "quota": 5,
            "count": 2,
            "trip_leader": true
        },
         {
            "_id": "598adeaea907bd6aee3928b5",
            "_leader": {
                "_id": "5927f48c8553514047eee97c",
                "name": "tes"
            },
            "date": {
                "start": "2017-09-01T00:00:00.000Z",
                "end": "2017-09-01T00:00:00.000Z"
            },
            "_trip": {
                "_id": "598adeaea907bd6aee3928b6",
                "main_image": "https:///tes",
                "title": "tes",
                "destination": "Tangkuban Perahu"
            },
            "quota": 5,
            "count": 2,
            "trip_leader": false
          }
    ]
}
```
get user booked trip

### Endpoint

`GET /user/trip/booked`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit     | optional | default '10'
offset    | optional | 0
sort      | optional | sort


##Get List Booking Request
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "5a0b1c03458a0f6130f6d03e",
            "updatedAt": "2017-11-14T16:39:27.954Z",
            "createdAt": "2017-11-14T16:38:27.621Z",
            "_author": "59c5c89665a538001088798f",
            "_trip": "59c87a84ed5d72000ffba17c",
            "_joined_id": "59c87a83ed5d72000ffba17b",
            "code": "OPBIQ1WD6YNQ",
            "amount": 330000,
            "original_price": 165000,
            "type": "multiple",
            "promo_code": {
                "_id": "5a027d96fae0bd21345becab",
                "updatedAt": "2017-11-14T16:33:28.808Z",
                "createdAt": "2017-11-08T03:44:22.112Z",
                "code": "AAAAA",
                "discount_type": "price",
                "start": "2017-11-12T17:00:00.000Z",
                "expiry": "2017-12-20T17:00:00.000Z",
                "discount": 1,
                "__v": 0,
                "once_promo": true
            },
            "users": [
                {
                    "data": {
                        "_id": "5a0a90f368d9ce60f872239d",
                        "name": "tumpistudio",
                        "email": {
                            "data": "tumpistudio@gmail.com"
                        }
                    },
                    "_id": "5a0b1c03458a0f6130f6d042",
                    "promo": false
                },
                {
                    "data": {
                        "_id": "5a0b172a8b8faf7d50bf7605",
                        "name": "vitayufita14",
                        "email": {
                            "data": "vitayufita14@gmail.com"
                        }
                    },
                    "_id": "5a0b1c03458a0f6130f6d041",
                    "promo": false
                }
            ],
            "status": "expired",
            "__v": 0,
            "snap": {
                "token": "6f611fa7-9149-4a42-83a6-897d63281bbe",
                "redirect_url": "https://app.midtrans.com/snap/v2/vtweb/6f611fa7-9149-4a42-83a6-897d63281bbe"
            }
        },
        {
            "_id": "5a0b1b4a458a0f6130f6d039",
            "updatedAt": "2017-11-14T16:36:22.860Z",
            "createdAt": "2017-11-14T16:35:22.835Z",
            "_author": "59c5c89665a538001088798f",
            "_trip": "59c87a84ed5d72000ffba17c",
            "_joined_id": "59c87a83ed5d72000ffba17b",
            "code": "OP5WGEE51JSI",
            "amount": 330000,
            "original_price": 165000,
            "type": "multiple",
            "promo_code": {
                "_id": "5a027d96fae0bd21345becab",
                "updatedAt": "2017-11-14T16:33:28.808Z",
                "createdAt": "2017-11-08T03:44:22.112Z",
                "code": "AAAAA",
                "discount_type": "price",
                "start": "2017-11-12T17:00:00.000Z",
                "expiry": "2017-12-20T17:00:00.000Z",
                "discount": 1,
                "__v": 0,
                "once_promo": true
            },
            "users": [
                {
                    "data": {
                        "_id": "5a0a90f368d9ce60f872239d",
                        "name": "tumpistudio",
                        "email": {
                            "data": "tumpistudio@gmail.com"
                        }
                    },
                    "_id": "5a0b1b4a458a0f6130f6d03d",
                    "promo": false
                },
                {
                    "data": {
                        "_id": "5a0b172a8b8faf7d50bf7605",
                        "name": "vitayufita14",
                        "email": {
                            "data": "vitayufita14@gmail.com"
                        }
                    },
                    "_id": "5a0b1b4a458a0f6130f6d03c",
                    "promo": false
                }
            ],
            "status": "expired",
            "__v": 0
        },
    ]
 }
```
get user booking request list

### Endpoint

`GET /booking/list`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit     | optional | default '10'
offset    | optional | 0
sort      | optional | sort
type      |optional | "multiple"
booking_code |optional | "OPIUHS89JH"
status |optional | "waiting" "pending" "success"
trip_id |optional | "id trip"
joined_id |optional | "id joined trip"
promo_code |optional | "PROMO10"

##Get Single Booking
> Success Result

```json
{
    "error": false,
    "data": {
        "_id": "5a0b1c03458a0f6130f6d03e",
        "updatedAt": "2017-11-14T16:39:27.954Z",
        "createdAt": "2017-11-14T16:38:27.621Z",
        "_author": "59c5c89665a538001088798f",
        "_trip": "59c87a84ed5d72000ffba17c",
        "_joined_id": "59c87a83ed5d72000ffba17b",
        "code": "OPBIQ1WD6YNQ",
        "amount": 330000,
        "original_price": 165000,
        "type": "multiple",
        "promo_code": {
            "_id": "5a027d96fae0bd21345becab",
            "updatedAt": "2017-11-14T16:33:28.808Z",
            "createdAt": "2017-11-08T03:44:22.112Z",
            "code": "AAAAA",
            "discount_type": "price",
            "start": "2017-11-12T17:00:00.000Z",
            "expiry": "2017-12-20T17:00:00.000Z",
            "discount": 1,
            "__v": 0,
            "once_promo": true
        },
        "users": [
            {
                "data": {
                    "_id": "5a0a90f368d9ce60f872239d",
                    "name": "tumpistudio",
                    "email": {
                        "data": "tumpistudio@gmail.com"
                    }
                },
                "_id": "5a0b1c03458a0f6130f6d042",
                "promo": false
            },
            {
                "data": {
                    "_id": "5a0b172a8b8faf7d50bf7605",
                    "name": "vitayufita14",
                    "email": {
                        "data": "vitayufita14@gmail.com"
                    }
                },
                "_id": "5a0b1c03458a0f6130f6d041",
                "promo": false
            }
        ],
        "status": "expired",
        "__v": 0,
        "snap": {
            "token": "6f611fa7-9149-4a42-83a6-897d63281bbe",
            "redirect_url": "https://app.midtrans.com/snap/v2/vtweb/6f611fa7-9149-4a42-83a6-897d63281bbe"
        }
    }
}
```
get single user booking request list

### Endpoint

`GET /booking/list`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | optional | 'id booking'
limit     | optional | default '10'
offset    | optional | 0
sort      | optional | sort
type      |optional | "multiple"
booking_code |optional | "OPIUHS89JH"
status |optional | "waiting" "pending" "success"
trip_id |optional | "id trip"
joined_id |optional | "id joined trip"
promo_code |optional | "PROMO10"