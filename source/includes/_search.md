# Search

## Search
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "5974e626135679b82c151c38",
            "name": "\"Gunung Bromo\""
        },
        {
            "_id": "5974e9347ee38d31dc2df4f1",
            "name": "Bali"
        },
        {
            "_id": "5974e67564ca8ea84056f535",
            "name": "Gunung Merapi"
        },
        {
            "_id": "5974ea21432062c050bada60",
            "name": "Gunung Pratau"
        },
        {
            "_id": "5974e32779595fbfaca877ad",
            "name": "Gunung Semeru"
        },
        {
            "_id": "5974e8ca211facb5b46a50ae",
            "name": "Gunung merbabu"
        },
        {
            "_id": "5974e4c1564cc2a7d4a2dec0",
            "name": "Pahawang"
        },
        {
            "_id": "5974e9427ee38d31dc2df4f5",
            "name": "Raja Ampat"
        }
    ]
}

{
    "error": false,
    "data": [
        {
            "_id": "5974d92957c5118a344f83e9",
            "name": "arizal",
            "profile_picture":"url"
        }
    ]
}

{
    "error": false,
    "data": [
        {
            "_id": "5974e9427ee38d31dc2df4f2",
            "_author": {
                "_id": "5974da9257c5118a344f83ed",
                "name": "paijo"
            },
            "main_image": "https:///tes",
            "title": "tes",
            "destination": "raja ampat",
            "quota": 5,
            "price": 40000,
            "date": {
                "start": "2017-08-17T00:00:00.000Z",
                "end": "2017-08-18T00:00:00.000Z"
            }
        }
    ]
}
```





get popular trip.

### Endpoint

`GET /search`

### Query Parameters
Parameter | Required | Example
--------- | ------- | -----------
q         | true    | `ya apaa yang dicari`
type      | true    | `trip` `trip_destination_suggestion` `user` `tag`
offset    | false   | `1` default offset is `0`
limit     | false   | `10` default limit is `10`
sort      | false   | `date.start` default is `date.start` `sort` could be anything

### Trip Type
Parameter | Required | Example
--------- | ------- | -----------
start         | false    | TIMESTAMP
end      | false    | TIMESTAMP
participant    | false   | `1`

<aside class="notice">
for `trip` search need "start","end","participant" parameter
</aside>
