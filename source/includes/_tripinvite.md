#Invite

##Invite user to join Trip
> Success Result

```json
{
    "error": false
}
```

invite another user to join trip

### Endpoint

`POST /user/trip/invite`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id        | true    | trip id
user_id         |true | user_id


## Get Trip Invites
> Success Result

```json
{
    "error": false,
    "data": [
      {
           "_from": {
                "name" : "",
                "profile_picture" : ""
           },
           "trip":{
            "main_image": "https:///tes",
                       "title": "tes",
                       "price": 40000
          }
         },
      {
                 "_from": {
                      "name" : "",
                      "profile_picture" : ""
                 },
                 "trip":{
                  "main_image": "https:///tes",
                             "title": "tes",
                             "price": 40000
                }
               },

    ]
}
```

getting joined user of the trip

### Endpoint

`GET /user/trip/invite`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `15`
