# Trip

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Create Trip
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_author": "5933658b705c0a671c510acd",
            "_category": "test",
            "main_image": "https:///tes",
            "title": "tes",
            "description": "ttt",
            "additional_note": "this is additional note",
            "important_notice": "eh ini important notice",
            "is_public": false,
            "quota": 5,
            "price": 40000,
            "_id": "593e7da24d5c58aa6c349d3a",
            "activities": [
                {
                    "title": "tess",
                    "image": "ini gambar",
                    "_id": "593e7da24d5c58aa6c349d3b",
                    "hourly": [
                        {
                            "start": 7,
                            "end": 8,
                            "activity": "makan-makan",
                            "_id": "593e7da24d5c58aa6c349d3c"
                        },
                        .....
                        .....
                        .....
                    ]
                },
                .....
                .....
                .....
            ],
            "date": {
                "start": "1970-01-18T07:54:10.267Z",
                "end": "1970-01-18T07:54:10.267Z"
            },
            "meeting_point": {
                "name": "name destination",
                "lat": -6.9739024,
                "long": 107.627451
            }
        },
        .....
        .....
        .....
        .....
    ]
}
```

creating new trip.

### Endpoint

`POST /trip/create`

<aside class="notice">
Remember — User must be verified to make trip
</aside>

<aside class="notice">
Use JSON body request
</aside>

### Body request
name | Required | Description
--------- | ------- | -----------
category | true | trip category
main_image | true | main header image
title | true | trip title
description | true | trip description
destination | true | trip destination
meeting_point | true | where meeting point
date | true | time to trip,use unix timestamp
is_public | true | is trip public
quota | true | trip quota
min_quota | true | trip minimum quota
price | true | trip prize
price_included | true | price included
price_excluded | true | price excluded
activities | true | trip activities
requirement_equipment | true | price excluded
additional_note | false | additional note
important_notice | false | important notice


`see example request`


>Example Body Request

```json
{
	"category":"test",
	"main_image":"https:///tes",
	"title":"tes",
	"description":"ttt",
	"destination":"name of destination",
	"meeting_point":{
		"name":"name destination",
		"lat":-6.9739024,
		"long":107.627451
	},
	"date":[
		{
			"start":1497250267,
			"end":1497250267
		},
		{
			"start":1497250267,
			"end":1497250267
		}
	],
	"is_public":false,
	"quota":5,
	"price":40000,
	"price_included":"aaa,aaa,aa,",
	"price_excluded": "bbb,bbb,bbb,",
	"activities":[
		{
			"title":"tess",
			"image":"ini gambar",
			"hourly":[
				{
					"start":"07.00",
					"end": "08.00",
					"activity": "makan-makan"
				}
			]
		}
	],
	"requirement_equipment":"halah",
	"additional_note":"this is additional note",
	"important_notice":"eh ini important notice"
}
```


## Edit Trip
> Success Result

```json
{
    "error": false,
    "data": {
            "_author": "5933658b705c0a671c510acd",
            "_category": "test",
            "main_image": "https:///tes",
            "title": "tes",
            "description": "ttt",
            "additional_note": "this is additional note",
            "important_notice": "eh ini important notice",
            "is_public": false,
            "quota": 5,
            "price": 40000,
            "_id": "593e7da24d5c58aa6c349d3a",
            "activities": [
                {
                    "title": "tess",
                    "image": "ini gambar",
                    "_id": "593e7da24d5c58aa6c349d3b",
                    "hourly": [
                        {
                            "start": 7,
                            "end": 8,
                            "activity": "makan-makan",
                            "_id": "593e7da24d5c58aa6c349d3c"
                        },
                        .....
                        .....
                        .....
                    ]
                },
                .....
                .....
                .....
            ],
            "date": {
                "start": "1970-01-18T07:54:10.267Z",
                "end": "1970-01-18T07:54:10.267Z"
            },
            "meeting_point": {
                "name": "name destination",
                "lat": -6.9739024,
                "long": 107.627451
            }
        }
}
```
edit exiting trip

### Endpoint

`POST /trip/edit`

<aside class="notice">
Remember — User must be verified to make trip
</aside>

<aside class="notice">
Use JSON body request
</aside>

### Body request
name | Required | Description
--------- | ------- | -----------
trip_id  | true | trip `_id`
category | optional | trip category
main_image | optional | main header image
title | optional | trip title
description | optional | trip description
destination | optional | trip destination
meeting_point | optional | where meeting point
date | optional | time to trip,use unix timestamp
is_public | optional | is trip public
quota | optional | trip quota
min_quota | optional | trip minimum quota
price | optional | trip prize
price_included | optional | price included
price_excluded | optional | price excluded
activities | optional | trip activities
requirement_equipment | optional | price excluded
additional_note | optional | additional note
important_notice | optional | important notice



## Get Popular Trip
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "group": "Gunung Semeru",
            "trips": [
                {
                    "_id": "5974e32779595fbfaca877aa",
                    "_author": {
                        "_id": "5974d92957c5118a344f83e9",
                        "name": "arizal"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Semeru",
                    "quota": 5,
                    "price": 40000
                },
                {
                    "_id": "5974e40979595fbfaca877ae",
                    "_author": {
                        "_id": "5974da9257c5118a344f83ed",
                        "name": "paijo"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Semeru",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "Pahawang",
            "trips": [
                {
                    "_id": "5974e4c1564cc2a7d4a2deba",
                    "_author": {
                        "_id": "5974da3a57c5118a344f83eb",
                        "name": "tumpi"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Pahawang",
                    "quota": 5,
                    "price": 40000
                },
                {
                    "_id": "5974e4c1564cc2a7d4a2debd",
                    "_author": {
                        "_id": "5974da3a57c5118a344f83eb",
                        "name": "tumpi"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Pahawang",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "Gunung Bromo",
            "trips": [
                {
                    "_id": "5974e55f564cc2a7d4a2dec1",
                    "_author": {
                        "_id": "5974d92957c5118a344f83e9",
                        "name": "arizal"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Bromo",
                    "quota": 5,
                    "price": 40000
                },
                {
                    "_id": "5974e625135679b82c151c35",
                    "_author": {
                        "_id": "5974d92957c5118a344f83e9",
                        "name": "arizal"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Bromo",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "Gunung Merapi",
            "trips": [
                {
                    "_id": "5974e67564ca8ea84056f532",
                    "_author": {
                        "_id": "5974d92957c5118a344f83e9",
                        "name": "arizal"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Merapi",
                    "quota": 5,
                    "price": 40000
                },
                {
                    "_id": "5974e6ca64ca8ea84056f536",
                    "_author": {
                        "_id": "5974d92957c5118a344f83e9",
                        "name": "arizal"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Merapi",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "gunung merbabu",
            "trips": [
                {
                    "_id": "5974e8ca211facb5b46a50ab",
                    "_author": {
                        "_id": "5974da9257c5118a344f83ed",
                        "name": "paijo"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "gunung merbabu",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "Bali",
            "trips": [
                {
                    "_id": "5974e9347ee38d31dc2df4ee",
                    "_author": {
                        "_id": "5974da9257c5118a344f83ed",
                        "name": "paijo"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Bali",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "raja ampat",
            "trips": [
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
                    "price": 40000
                }
            ],
            "start_from": 40000
        },
        {
            "group": "Gunung Pratau",
            "trips": [
                {
                    "_id": "5974ea21432062c050bada5d",
                    "_author": {
                        "_id": "5974da3a57c5118a344f83eb",
                        "name": "tumpi"
                    },
                    "main_image": "https:///tes",
                    "title": "tes",
                    "destination": "Gunung Pratau",
                    "quota": 5,
                    "price": 40000
                }
            ],
            "start_from": 40000
        }
    ]
}
```

get popular trip.

### Endpoint

`GET /trip/by_popular`

### Query Parameters
Parameter | Required | Example
--------- | ------- | -----------
offset    | false   | `1` default offset is `0`
limit     | false   | `10` default limit is `10`
sort      | false   | `date.start` default is `date.start` `sort` could be anything



## Get Trip by Category
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "594a148eb28f952b64f87b9d",
            "_author": {
                "_id": "5933658b705c0a671c510acd",
                "name": "paijo",
                "profile_picture" : "http://alamat"
                "rating":{
                       "point":4.5,
                       "count":12
                 }
            },
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        {
            "_id": "594a14e8b28f952b64f87ba0",
            "_author": {
                "_id": "5933658b705c0a671c510acd",
                "name": "paijo",
                "profile_picture" : "http://alamat",
                "rating":{
                       "point":4.5,
                       "count":12
                 }
            },
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        ...
        ...
        ...
    ]
}
```

get trip by category.

### Endpoint

`GET /trip/by_category`

### Query Parameters
Parameter | Required | Example
--------- | ------- | -----------
category  | true    | `sport`
offset    | false   | `1` default offset is `0`
limit     | false   | `10` default limit is `10`
sort      | false   | `date.start` default is `date.start` `sort` could be anything


## Get Trip by Explore
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "594a148eb28f952b64f87b9d",
            "_author": {
                "_id": "5933658b705c0a671c510acd",
                "name": "paijo",
                "profile_picture" : "http://alamat"
                "rating":{
                       "point":4.5,
                       "count":12
                 }
            },
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        {
            "_id": "594a14e8b28f952b64f87ba0",
            "_author": {
                "_id": "5933658b705c0a671c510acd",
                "name": "paijo",
                "profile_picture" : "http://alamat",
                "rating":{
                       "point":4.5,
                       "count":12
                 }
            },
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        ...
        ...
        ...
    ]
}
```

get trip by explore.

### Endpoint

`GET /trip/by_explore`

### Query Parameters
Parameter | Required | Example
--------- | ------- | -----------
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `10`
sort      | false   | `createdAt` default is `createdAt` `sort` could be anything


## Get Trip by Author
> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "594a148eb28f952b64f87b9d",
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        {
            "_id": "594a14e8b28f952b64f87ba0",
            "main_image": "https:///tes",
            "title": "tes",
            "price": 40000
        },
        ...
        ...
        ...
    ]
}
```

get trip by author, or user who created the trip.

### Endpoint

`GET /trip/by_user`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | true    | user id
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `10`
sort      | false   | `-createdAt` default is `-createdAt` `sort` could be anything


## Get Detail Trip
> Success Result

```json
{
    "error": false,
    "data": {
        "_id": "594a148eb28f952b64f87b9d",
        "_author": {
            "_id": "5933658b705c0a671c510acd",
            "name": "paijo",
            "profile_picture" : "http://alamat"
            "rating":{
                   "point":4.5,
                   "count":12
             }
        },
        "_category": "sport",
        "main_image": "https:///tes",
        "title": "tes",
        "description": "ttt",
        "additional_note": "this is additional note",
        "important_notice": "eh ini important notice",
        "is_public": false,
        "quota": 5,
        "price": 40000,
        "__v": 0,
        "joined_user": 0,
        "activities": [
            {
                "title": "tess",
                "image": "ini gambar",
                "_id": "594a148eb28f952b64f87b9e",
                "hourly": [
                    {
                        "start": "07.00",
                        "end": "08.00",
                        "activity": "makan-makan",
                        "_id": "594a148eb28f952b64f87b9f"
                    }
                ]
            }
        ],
        "date": {
            "start": "2017-06-29T00:00:00.000Z",
            "end": "2017-07-01T00:00:00.000Z"
        },
        "meeting_point": {
            "name": "name destination",
            "lat": -6.9739024,
            "long": 107.627451
        },
        "destination": "name of destination"
    }
}
```

get detail data of trip

### Endpoint

`GET /trip/detail`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | true    | trip id


## Get User Trip
> Success Result

```json
{
    "error": false,
    "data": [{
            "_id": "59785ff7815aa05520472eac",
            "_author": {
                "_id": "5974d92957c5118a344f83e9",
                "name": "arizal"
            },
            "main_image": "https:///tes",
            "title": "tiga",
            "destination": "Gunung Sinabung",
            "quota": 5,
            "price": 40000,
            "date": [
                {
                    "start": "2017-09-04T00:00:00.000Z",
                    "end": "2017-09-04T00:00:00.000Z",
                    "count": 0,
                    "_joined_id": "59785ff7815aa05520472eaa"
                }
            ]
        },{
            "_id": "59785ff7815aa05520472eac",
            "_author": {
                "_id": "5974d92957c5118a344f83e9",
                "name": "arizal"
            },
            "main_image": "https:///tes",
            "title": "tiga",
            "destination": "Gunung Sinabung",
            "quota": 5,
            "price": 40000,
            "date": [
                {
                    "start": "2017-09-04T00:00:00.000Z",
                    "end": "2017-09-04T00:00:00.000Z",
                    "count": 0,
                    "_joined_id": "59785ff7815aa05520472eaa"
                }
            ]
        }
    ]
```

get user upcoming and past trip

### Endpoint

`GET /user/trip/get_user_trip`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
user_id        | true    | user id
type     | true | `upcoming` or `past`


## Get Joined User of Trip
> Success Result

```json
{
    "error": false,
    "data": [
      {
           "_id": "5923cfc450434044b836c3b8",
           "profile_picture": "image url profile picture",
           "name": "arizal"
         },
         {
           "_id": "592510f6f856d02284b2f44b",
           "profile_picture": "image url profile picture"
           "name": "bibibi testititititi"
         },
         {
           "_id": "59251006f856d02284b2f44a",
           "profile_picture": "image url profile picture"
           "name": "testititititi"
         }
    ]
}
```

getting joined user of the trip

### Endpoint

`GET /trip/detail/joined_user`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | true    | trip date `_joined_id`
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `15`


## Get Bookmark Trip
> Success Result

```json
{
    "error": false,
    "data": [
      {
           "_id": "5923cfc450434044b836c3b8",
           "profile_picture": "image url profile picture",
           "name": "arizal"
         },
         {
           "_id": "592510f6f856d02284b2f44b",
           "profile_picture": "image url profile picture"
           "name": "bibibi testititititi"
         },
         {
           "_id": "59251006f856d02284b2f44a",
           "profile_picture": "image url profile picture"
           "name": "testititititi"
         }
    ]
}
```

getting bookmark trip

### Endpoint

`GET /user/trip/bookmark`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | true    | trip id
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `15`


## Bookmark Trip
> Success Result

```json
{
    "error": false,
}
```

bookmark trip

### Endpoint

`POST /user/trip/bookmark`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id        | true    | trip id

## Remove Bookmark Trip
> Success Result

```json
{
    "error": false,
}
```

delete bookmark trip

### Endpoint

`DELETE /user/trip/bookmark/delete_single`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
trip_id        | true    | trip id

## Remove All Bookmark Trip
> Success Result

```json
{
    "error": false,
}
```

delete all bookmark trip

### Endpoint

`DELETE /user/trip/bookmark/delete_all`



