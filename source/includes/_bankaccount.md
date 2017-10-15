#Bank Account

##Get Bank Account
> Success Result

```json
{
    "error": false,
    "data":[
    {
         "_id":"sadasdasda",
         "_author":"asdasdsadas",
         "full_name":"Tsubasa",
         "account_number":"123123123",
         "bank_code":"MND",
         "bank_name":"MANDIRI"
    },
    {
        "_id":"sadasdasda",
         "_author":"asdasdsadas",
         "full_name":"Tsubasa",
         "account_number":"123123123",
         "bank_code":"MND",
         "bank_name":"MANDIRI"
    },
    ...
    ...
    ...
    ]
}
```
get user bank account

### Endpoint

`GET /wallet/bank_account`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
limit        | false    | limit get user data
offset         |false | start from offset
sort      |  false  | sorting

## New Bank Account
> Success Result

```json
{
    "error": false,
    "data":
    {
         "_id":"sadasdasda",
         "_author":"asdasdsadas",
         "full_name":"Tsubasa",
         "account_number":"123123123",
         "bank_code":"MND",
         "bank_name":"MANDIRI"
    }
}
```
create new user bank account

### Endpoint

`POST /wallet/bank_account`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
full_name | true    | full name
account_number | true    | account number
bank_code | true    | bank code
bank_name | true | bank name

<aside class="notice">
Here supported bank account : http://iris-docs.midtrans.com/#supported-banks
</aside>


## Update Bank Account
> Success Result

```json
{
    "error": false,
    "data":
    {
         "_id":"sadasdasda",
         "_author":"asdasdsadas",
         "full_name":"Tsubasa",
         "account_number":"123123123",
         "bank_code":"MND",
         "bank_name":"MANDIRI"
    }
}
```
updating user bank account

### Endpoint

`PUT /wallet/bank_account/:id/update`

<aside class="notice">
You must replace <code>:id</code> with bank account _id.
</aside>

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
full_name | optional    | full name
account_number | optional    | account number
bank_code | optional    | bank code
bank_name | optional | bank name

## Delete Bank Account
> Success Result

```json
{
    "error": false
}
```
updating user bank account

### Endpoint

`DELETE /wallet/bank_account/:id/delete`

<aside class="notice">
You must replace <code>:id</code> with bank account _id.
</aside>

## Delete All Bank Account
> Success Result

```json
{
    "error": false
}
```
updating user bank account

### Endpoint

`DELETE /wallet/bank_account`


