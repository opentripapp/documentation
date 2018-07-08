# Bank Account

## Get Bank Account

get user bank account

### Endpoint

`GET /wallet/bank_account`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset

## New Bank Account

create new user bank account

### Endpoint

`POST /wallet/bank_account`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
full_name | true    | full name
account_number | true    | account number
bank_code | true    | bank code
bank_name | true | bank name

<aside class="notice">
Here supported bank account : http://iris-docs.midtrans.com/#supported-banks
</aside>


