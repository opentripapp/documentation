# Category

## Get Trip Category

> Result

```json
{
  "error": false,
  "data": [
     {
        "_id":"5923cfc450434044b836c3b8",
        "name":"Sport"
    },
    {
        "_id":"5923cfc450434044b836c3b8",
        "name":"Sport"
    },
    {
        "_id":"5923cfc450434044b836c3b8",
        "name":"Culinare"
    }
  ]
}
```
Getting Trip Category

### Endpoint

`GET /category`

# Banner

## Get Banner

> Result

```json
{
  "error": false,
  "data": [
     {
          "image":"https://aws.imageurl",
          "type":"NEW_FEATURE",
          "data":"url info kalau ada"
    },
    {
         "image":"https://aws.imageurl",
         "type":"TRIP_PROMO",
         "data":"ini id trip yang dipromooin"
    },
    {
        "image":"https://aws.imageurl",
        "type":"INFO",
        "data":"url info mungkin kalau ada"
    }
  ]
}
```
Getting Home Banner

### Endpoint

`GET /banner`

### Query Parameters

Parameter | Required | Description
--------- | -------  | -----------
sort       | optional | default `createdAt`
limit | optional | default `4`
offset        | optional | default `0`
