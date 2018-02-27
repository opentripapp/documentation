#Promo

## Get List Promo

> Result

```json
{
    "error": false,
    "data": [
        {
            "expiry": "2017-10-15T05:30:48.063Z",
            "discount": 100000,
            "discount_type": "price",
            "code": "OPENTRIP100K"
        }
    ]
}
```

get list available promo

### Endpoint

`GET /promos`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
sort | optional | `expiry` is default sort
limit | optional | `25` is default limit
offset | optional | `0` is default offset

## Get Promo Code

> Result

```json
{
    "error": false,
    "data": {
        "expiry": "2017-10-15T05:30:48.063Z",
        "discount": 100000,
        "discount_type": "price",
        "code": "OPENTRIP100K"
    }
}
```

check promo code


### Endpoint

`GET /promos/check`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
code | true | promo code




## Check Promo Code

> Error Result

```json
{
    "error": true,
    "code": "NOT_FOUND",
    "message": "code not found"
}
```

> Success Result

```json
{
    "error": false,
    "data": {
        "code": "2D",
        "calculated_price": 98000
    }
}
```

check promo code and get calculated price


### Endpoint

`GET /promos/check_code`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
code | true | promo code
trip_id | true | id of trip
trip_price | true | price of trip


