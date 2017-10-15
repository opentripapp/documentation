#Wallet

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
> Success Result

```json
{
    "error": false,
    "data":[
    {
         "_author":"sadasdasda",
         "action":"payment",
         "amount":20
         "initial_balance":0,
         "final_balance":20,
         "note":"OPS3434"
    },
    {
             "_author":"sadasdasda",
             "action":"refund",
             "amount":20
             "initial_balance":20,
             "final_balance":0,
             "note":"OPS3434"
    },
    {
             "_author":"sadasdasda",
             "action":"withdrawal",
             "amount":3000
             "initial_balance":4000,
             "final_balance":1000,
             "note":"OPS3434"
    },
    {
             "_author":"sadasdasda",
             "action":"transfer",
             "amount":3000
             "initial_balance":4000,
             "final_balance":1000,
             "note":"OPS3434"
     },
     {
              "_author":"sadasdasda",
              "action":"receive_transfer",
              "amount":3000
              "initial_balance":4000,
              "final_balance":1000,
              "note":"OPS3434"
      },
       {
                 "_author":"sadasdasda",
                 "action":"topup",
                 "amount":3000
                 "initial_balance":4000,
                 "final_balance":7000,
                 "note":"OPS3434"
        },
    ]
}
```
get user wallet history

### Endpoint

`GET /wallet/history`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
sort      |  false  | sorting
action | optional | "payment","refund","withdrawal","transfer","receive_transfer","topup"
from_date | optional | "2017-05-21"
to_date | optional | "2017-06-1"


## Withdrawal Request
> Success Result

```json
{
    "error": false,
    "data":{
     "status": "queue",
     "reference_no":231231231
    }
}
```
request withdrawal from wallet

### Endpoint

`POST /wallet/withdrawal`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
amount    | true    | amount to transfer
bank_account_id | true | bank account `_id`
password  | true | user password
notes     | true  | notes withdrawal
email     | optional | email to receive notification

<aside class="notice">
- minimum amount to transfer(Withdrawn) is : 25.000
- disbursement cost is : 5.000
- Withdrawal only once a day
</aside>


## Withdrawal History
> Success Result

```json
{
    "error": false,
    "data":[
    {
     "status": "queue",
     "reference_no":231231231
    },
    {
     "status": "queue",
     "reference_no":231231231
    },
    {
      "status": "queue",
      "reference_no":231231231
    },
    {
       "status": "queue",
       "reference_no":231231231
    }
    ]
}
```
get withdrawal history

### Endpoint

`GET /wallet/history/withdrawals`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
sort      |  false  | sorting
from_date | optional | "2017-05-21"
to_date | optional | "2017-06-1"

## Get Detail Withdrawal
> Success Result

```json
{
    "error": false,
    "data":{
           "amount": 10000,
           "beneficiary_name": "any",
           "beneficiary_account": "1150006390175",
           "bank": "PT. Bank Mandiri (Persero) Tbk.",
           "reference_no": "11540d36312884",
           "notes": "testing",
           "beneficiary_email": "tumpistudio@gmail.com",
           "status": "queued",
           "created_by": "Muhammad Arizal",
           "created_at": "2017-08-21T10:54:44Z",
           "updated_at": "2017-08-21T10:54:44Z"
       }
}
```
get detail withdrawal

### Endpoint

`GET /wallet/history/withdrawals/:reference_no`

## Transfer
> Success Result

```json
{
    "error": false
}
```
transfer to another account

### Endpoint

`POST /wallet/transfer`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
amount        | true    | amount to transfer
password       |true | user password
email      |  true  |another user email to receive transfer
notes | true | notes of transfer

