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

## Check Promo Code

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

### Discount Type

Parameter |  Description
--------- |  --------
price | price base discount
percent | percent base discount


### Endpoint

`GET /promos/check`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
code | true | promo code
