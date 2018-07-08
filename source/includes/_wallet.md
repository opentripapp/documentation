# Wallet

## Wallet Balance
> Success Result

```json
{
    "error": false,
    "data":{
         "_author":"sadasdasda",
         "amount":0,
         "currency":"IDR"
    }
}
```
get user wallet balance

### Endpoint

`GET /wallet/balance`


## Wallet History

get user wallet history

### Endpoint

`GET /wallet/history`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
action | optional | "payment","refund","withdrawal","transfer","receive_transfer","topup"
service_type | optional | "invoice"
status | optional | status transaction



## Withdrawal Request

request withdrawal from wallet

### Endpoint

`POST /wallet/withdrawal`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
full_name  | true    | name of user
email     | true | email to receive notification
phone_number     | true | email to receive notification
amount    | true    | amount to transfer
bank_account_number | true | bank account number
bank_name   | true | name of bank
reference_number   | optional | reference number
password   | true | user password
notes   | optional | additional notes

<aside class="notice">
- minimum amount to transfer(Withdrawn) is : 25.000
- disbursement cost is : 5.000
- Withdrawal only once a day
</aside>


## Withdrawal History

get withdrawal history

### Endpoint

`GET /wallet/history/withdrawal`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
status         |false | status transaction

## Wallet History

get withdrawal history

### Endpoint

`GET /wallet/history`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
status         |false | status transaction

## Hold Transaction

get hold transaction

### Endpoint

`GET /wallet/hold`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
status         |false | status transaction

