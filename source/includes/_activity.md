# Activity

## Create New Posting

> Result

```json
{
    "error": false,
    "data": {
        "__v": 0,
        "updatedAt": "2017-07-13T04:26:12.778Z",
        "createdAt": "2017-07-13T04:26:12.778Z",
        "_author": "594b57fac0f7361678bbec5b",
        "type": "STATUS",
        "text": "ahhh.. enaknya",
        "_id": "5966f6647abed889cc3eb349",
        "trip": [],
        "tag": [
            "5966e6c423c15b84140313ea",
            "5966e6c423c15b84140313ea",
            "5966e6c423c15b84140313ea"
        ],
        "photos": [
            "http://imageurl",
            "http://imageurl",
            "http://imageurl"
        ],
        "location": {
            "name": "Pahawang",
            "lat": -3434234,
            "long": 17000000
        },
        "share": 0,
        "comment": 0,
        "like": 0
    }
}
```

creating new posting/activity

### Endpoint

`POST /user/activity/posting`

### Parameters

Parameter | Required | Example     | Description
--------- | ------- | -----------| --------
type | true | "CHECK_IN","BOOK_TRIP","STATUS" | type of posting ,remember use that type
text | false | "i am happy at #pahawang" | user text status
photos| false | ["https:img./s/s","https:/ssss"] | user photo of status, user array
location | false | - | user location, see example request
tag | false | `array of user id` | user tag, see example request
trip | false | `array of trip id` | user trip, see example request

### Type Of Posting

Name | Description
-----| ------------
CHECK_IN | Check In location, location parameter required
BOOK_TRIP | Share booked Trip , trip parameter required
STATUS | User status (text,photos,etc)

`user json request`

>Example Body Request

```json
{
	"type":"STATUS",
	"text" : "ahhh.. enaknya",
	"photos": ["http://imageurl","http://imageurl","http://imageurl"],
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	},
	"tag":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"]

}

{
	"type":"CHECK_IN",
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	}
}

{
	"type":"BOOK_TRIP",
	"text" : "ahhh.. enaknya",
	"photos": ["http://imageurl","http://imageurl","http://imageurl"],
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	},
	"tag":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"],
	"trip":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"]

}

```

## Update Posting

> Result

```json
{
    "error": false,
    "data": {
        "_id": "5966f70d7abed889cc3eb34a",
        "updatedAt": "2017-07-14T02:07:34.159Z",
        "createdAt": "2017-07-13T04:29:01.238Z",
        "_author": "594b57fac0f7361678bbec5b",
        "type": "STATUS",
        "text": "baruuu test",
        "__v": 0,
        "trip": [
            "5966e6c423c15b84140313ea"
        ],
        "tag": [
            "5966e6c423c15b84140313ea",
            "5966e6c423c15b84140313ea"
        ],
        "photos": [
            "http://imageurl",
            "http://imageurl"
        ],
        "location": {
            "long": 17000000,
            "lat": -3434234,
            "name": "Pahawang"
        },
        "share": 0,
        "comment": 0,
        "like": 0
    }
}
```

updating posting/activity

### Endpoint

`PUT /user/activity/update_posting`

### Parameters

Parameter | Required | Example     | Description
--------- | ------- | -----------| --------
type | true | "CHECK_IN","BOOK_TRIP","STATUS" | type of posting ,remember use that type
text | false | "i am happy at #pahawang" | user text status
photos| false | ["https:img./s/s","https:/ssss"] | user photo of status, user array
location | false | - | user location, see example request
tag | false | `array of user id` | user tag, see example request
trip | false | `array of trip id` | user trip, see example request

### Type Of Posting

Name | Description
-----| ------------
CHECK_IN | Check In location, location parameter required
BOOK_TRIP | Share booked Trip , trip parameter required
STATUS | User status (text,photos,etc)

`user json request`

>Example Body Request

```json
{
	"type":"STATUS",
	"text" : "ahhh.. enaknya",
	"photos": ["http://imageurl","http://imageurl","http://imageurl"],
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	},
	"tag":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"]

}

{
	"type":"CHECK_IN",
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	},
}

{
	"type":"BOOK_TRIP",
	"text" : "ahhh.. enaknya",
	"photos": ["http://imageurl","http://imageurl","http://imageurl"],
	"location" : {
		"name": "Pahawang",
		"lat": "-3434234",
		"long":"17000000"
	},
	"tag":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"],
	"trip":["5966e6c423c15b84140313ea","5966e6c423c15b84140313ea"]
}

```


## Delete Posting

> Success Result

```json
{
  "error": false,
}
```

deleting user posting

### Endpoint

`DELETE /user/activity/delete_posting`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id  | true    | `_id` of post id



## Action Like

> Success Result

```json
{
  "error": false,
}
```

liking user posting

### Endpoint

`POST /user/activity/like`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id  | true    | `_id` of post id

## Action Cancel Like

> Success Result

```json
{
  "error": false,
}
```

canceling like on user posting

### Endpoint

`POST /user/activity/unlike`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id  | true    | `_id` of post id

## Action Share

> Success Result

```json
{
  "error": false,
}
```

sharing user posting

### Endpoint

`POST /user/activity/share`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id  | true    | `_id` of post id
text | false | "i am happy at #pahawang"
photos| false | ["https:img./s/s","https:/ssss"]
location | false |  see example request
tag | false | `array of user id`
trip | false | `array of trip id`


## Do Comment

> Success Result

```json
{
    "error": false,
    "data": {
        "__v": 0,
        "updatedAt": "2017-07-14T02:46:08.897Z",
        "createdAt": "2017-07-14T02:46:08.897Z",
        "text": "baguusss,suka deeh",
        "post_id": "5966f6647abed889cc3eb349",
        "user_id": "5966e6c423c15b84140313ea",
        "_id": "5968307081cced1504912f51"
    }
}
```

do comment on user posting

### Endpoint

`POST /user/activity/comment`

### Query Parameters
Parameter | Required | Example
--------- | ------- | -----------
post_id  | true    | `_id` of post id
text | true | comment text


## Update Comment

> Success Result

```json
{
    "error": false,
    "data": {
        "_id": "5968307081cced1504912f51",
        "updatedAt": "2017-07-14T02:50:34.038Z",
        "createdAt": "2017-07-14T02:46:08.897Z",
        "text": "baguusss,suka deeh,eh iya bagus",
        "post_id": "5966f6647abed889cc3eb349",
        "user_id": "5966e6c423c15b84140313ea",
        "__v": 0
    }
}
```

updating user comment

### Endpoint

`PUT /user/activity/update_comment`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
comment_id  | true    | `_id` of post id
text | true | comment text


## Delete Comment

> Success Result

```json
{
    "error": false
}
```

deleting user comment

### Endpoint

`DELETE /user/activity/delete_comment`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
comment_id  | true    | `_id` of post id


## Hide User Post

> Success Result

```json
{
    "error": false
}
```

hide user postings

### Endpoint

`POST /user/activity/hide_post`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
user_id  | true    | `_id` of another user

## Hide User Post

> Success Result

```json
{
    "error": false
}
```

hide user postings

### Endpoint

`POST /user/activity/hide_post`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
user_id  | true    | `_id` of another user

## Show User Post (Undo Hide)

> Success Result

```json
{
    "error": false
}
```

showing another user post or undo hiding user postings

### Endpoint

`POST /user/activity/show_post`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
user_id  | true    | `_id` of another user

## Action Report Posting

> Result

```json
{
  "error": false
}
```
report user posting

### Endpoint

`POST /user/activity/report_post`


### Query Parameters

Parameter | Required | Description
--------- | ------- | --------
post_id | true | post id to report
reason_code| true | reason why reported

### reason_code

code | Description
---- | -----------
1    | it's spam
2    | it`s inappropriate
something else | why ?



## Get Feed (Posting)

> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "596836590a345e30bc335c2f",
            "updatedAt": "2017-07-14T03:11:21.824Z",
            "createdAt": "2017-07-14T03:11:21.824Z",
            "_author": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal"
            },
            "posting": {
                "_id": "5966f6647abed889cc3eb349",
                "updatedAt": "2017-07-14T03:11:21.830Z",
                "createdAt": "2017-07-13T04:26:12.778Z",
                "_author": "594b57fac0f7361678bbec5b",
                "type": "STATUS",
                "text": "ahhh.. enaknya",
                "__v": 0,
                "trip": [],
                "tag": [
                    "5966e6c423c15b84140313ea",
                    "5966e6c423c15b84140313ea",
                    "5966e6c423c15b84140313ea"
                ],
                "photos": [
                    "http://imageurl",
                    "http://imageurl",
                    "http://imageurl"
                ],
                "location": {
                    "name": "Pahawang",
                    "lat": -3434234,
                    "long": 17000000
                },
                "share": 1,
                "comment": 0,
                "like": 1
            },
            "share_from": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal"
            },
            "type": "SHARE",
            "text": "baguusss,suka deeh",
            "__v": 0,
            "trip": [],
            "tag": [],
            "photos": [],
            "share": 0,
            "comment": 0,
            "like": 0,
            "is_like": false
        },
        {
            "_id": "5966f6647abed889cc3eb349",
            "updatedAt": "2017-07-14T03:11:21.830Z",
            "createdAt": "2017-07-13T04:26:12.778Z",
            "_author": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal"
            },
            "type": "STATUS",
            "text": "ahhh.. enaknya",
            "__v": 0,
            "trip": [],
            "tag": [
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                },
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                },
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                }
            ],
            "photos": [
                "http://imageurl",
                "http://imageurl",
                "http://imageurl"
            ],
            "location": {
                "name": "Pahawang",
                "lat": -3434234,
                "long": 17000000
            },
            "share": 1,
            "comment": 0,
            "like": 1,
            "is_like": true
        },
        {
                    "_id": "5966f6647abed889cc3eb349",
                    "updatedAt": "2017-07-14T03:11:21.830Z",
                    "createdAt": "2017-07-13T04:26:12.778Z",
                    "_author": {
                        "_id": "594b57fac0f7361678bbec5b",
                        "name": "arizal"
                    },
                    "type": "CHECK_IN",
                    "location": {
                        "name": "Pahawang",
                        "lat": -3434234,
                        "long": 17000000
                    },
                    "share": 1,
                    "comment": 0,
                    "like": 1,
                    "is_like": true
                },
                {
                            "_id": "5966f6647abed889cc3eb349",
                            "updatedAt": "2017-07-14T03:11:21.830Z",
                            "createdAt": "2017-07-13T04:26:12.778Z",
                            "_author": {
                                "_id": "594b57fac0f7361678bbec5b",
                                "name": "arizal"
                            },
                            "type": "BOOK_TRIP",
                            "text": "ahhh.. enaknya",
                            "__v": 0,
                            "trip": [],
                            "tag": [
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                },
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                },
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                }
                            ],
                            "photos": [
                                "http://imageurl",
                                "http://imageurl",
                                "http://imageurl"
                            ],
                            "location": {
                                "name": "Pahawang",
                                "lat": -3434234,
                                "long": 17000000
                            },
                            "share": 1,
                            "comment": 0,
                            "like": 1,
                            "is_like": true
                        }
    ]
}
```

getting another user feed who follow

### Endpoint

`GET /user/activity/get_posting`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
offset    | false   | `1` default offset is `0`
limit     | false   | `15` default limit is `15`
sort      | false   | `-createdAt` default is `-createdAt` `sort` could be anything


## Get Feed (Posting) By Author

> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "596836590a345e30bc335c2f",
            "updatedAt": "2017-07-14T03:11:21.824Z",
            "createdAt": "2017-07-14T03:11:21.824Z",
            "_author": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal"
            },
            "posting": {
                "_id": "5966f6647abed889cc3eb349",
                "updatedAt": "2017-07-14T03:11:21.830Z",
                "createdAt": "2017-07-13T04:26:12.778Z",
                "_author": "594b57fac0f7361678bbec5b",
                "type": "STATUS",
                "text": "ahhh.. enaknya",
                "__v": 0,
                "trip": [],
                "tag": [
                    "5966e6c423c15b84140313ea",
                    "5966e6c423c15b84140313ea",
                    "5966e6c423c15b84140313ea"
                ],
                "photos": [
                    "http://imageurl",
                    "http://imageurl",
                    "http://imageurl"
                ],
                "location": {
                    "name": "Pahawang",
                    "lat": -3434234,
                    "long": 17000000
                },
                "share": 1,
                "comment": 0,
                "like": 1
            },
            "share_from": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal"
            },
            "type": "SHARE",
            "text": "baguusss,suka deeh",
            "__v": 0,
            "trip": [],
            "tag": [],
            "photos": [],
            "share": 0,
            "comment": 0,
            "like": 0,
            "is_like": false
        },
        {
            "_id": "5966f6647abed889cc3eb349",
            "updatedAt": "2017-07-14T03:11:21.830Z",
            "createdAt": "2017-07-13T04:26:12.778Z",
            "_author": {
                "_id": "594b57fac0f7361678bbec5b",
                "name": "arizal"
            },
            "type": "STATUS",
            "text": "ahhh.. enaknya",
            "__v": 0,
            "trip": [],
            "tag": [
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                },
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                },
                {
                    "_id": "5966e6c423c15b84140313ea",
                    "name": "arizal"
                }
            ],
            "photos": [
                "http://imageurl",
                "http://imageurl",
                "http://imageurl"
            ],
            "location": {
                "name": "Pahawang",
                "lat": -3434234,
                "long": 17000000
            },
            "share": 1,
            "comment": 0,
            "like": 1,
            "is_like": true
        },
        {
                    "_id": "5966f6647abed889cc3eb349",
                    "updatedAt": "2017-07-14T03:11:21.830Z",
                    "createdAt": "2017-07-13T04:26:12.778Z",
                    "_author": {
                        "_id": "594b57fac0f7361678bbec5b",
                        "name": "arizal"
                    },
                    "type": "CHECK_IN",
                    "location": {
                        "name": "Pahawang",
                        "lat": -3434234,
                        "long": 17000000
                    },
                    "share": 1,
                    "comment": 0,
                    "like": 1,
                    "is_like": true
                },
                {
                            "_id": "5966f6647abed889cc3eb349",
                            "updatedAt": "2017-07-14T03:11:21.830Z",
                            "createdAt": "2017-07-13T04:26:12.778Z",
                            "_author": {
                                "_id": "594b57fac0f7361678bbec5b",
                                "name": "arizal"
                            },
                            "type": "BOOK_TRIP",
                            "text": "ahhh.. enaknya",
                            "__v": 0,
                            "trip": [],
                            "tag": [
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                },
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                },
                                {
                                    "_id": "5966e6c423c15b84140313ea",
                                    "name": "arizal"
                                }
                            ],
                            "photos": [
                                "http://imageurl",
                                "http://imageurl",
                                "http://imageurl"
                            ],
                            "location": {
                                "name": "Pahawang",
                                "lat": -3434234,
                                "long": 17000000
                            },
                            "share": 1,
                            "comment": 0,
                            "like": 1,
                            "is_like": true
                        }
    ]
}
```

getting another user feed by who created

### Endpoint

`GET /user/activity/get_by_author`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
user_id   | true    | `_id` of user
offset    | false   | `1` default offset is `0`
limit     | false   | `15` default limit is `15`
sort      | false   | `-createdAt` default is `-createdAt` `sort` could be anything



## Get Single Post

> Success Result

```json
{
    "error": false,
    "data": {
                        "_id": "5966f6647abed889cc3eb349",
                        "updatedAt": "2017-07-14T03:11:21.830Z",
                        "createdAt": "2017-07-13T04:26:12.778Z",
                        "_author": {
                            "_id": "594b57fac0f7361678bbec5b",
                            "name": "arizal"
                        },
                        "type": "STATUS",
                        "text": "ahhh.. enaknya",
                        "__v": 0,
                        "trip": [],
                        "tag": [
                            {
                                "_id": "5966e6c423c15b84140313ea",
                                "name": "arizal"
                            },
                            {
                                "_id": "5966e6c423c15b84140313ea",
                                "name": "arizal"
                            },
                            {
                                "_id": "5966e6c423c15b84140313ea",
                                "name": "arizal"
                            }
                        ],
                        "photos": [
                            "http://imageurl",
                            "http://imageurl",
                            "http://imageurl"
                        ],
                        "location": {
                            "name": "Pahawang",
                            "lat": -3434234,
                            "long": 17000000
                        },
                        "share": 1,
                        "comment": 0,
                        "like": 1,
                        "is_like": true
                    }
}
```

getting single user post

### Endpoint

`GET /user/activity/get_single_posting`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id   | true    | `_id` of posting



## Get Post Comment

> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "5968457ea2a4b32db8b3d12e",
            "updatedAt": "2017-07-14T04:15:58.299Z",
            "createdAt": "2017-07-14T04:15:58.299Z",
            "text": "yuhhuuu",
            "post_id": "5966f6647abed889cc3eb349",
            "user_id": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal"
            },
            "__v": 0
        },
        {
            "_id": "59684585a2a4b32db8b3d12f",
            "updatedAt": "2017-07-14T04:16:05.326Z",
            "createdAt": "2017-07-14T04:16:05.326Z",
            "text": "its great",
            "post_id": "5966f6647abed889cc3eb349",
            "user_id": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal"
            },
            "__v": 0
        }
    ]
}
```

getting user comment

### Endpoint

`GET /user/activity/get_comment`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id   | true    | `_id` of posting
offset    | false   | `1` default offset is `0`
limit     | false   | `15` default limit is `15`
sort      | false   | `createdAt` default is `createdAt` `sort` could be anything


## Get Who Likes

> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "59682e9781cced1504912f50",
            "updatedAt": "2017-07-14T02:41:01.208Z",
            "createdAt": "2017-07-14T02:38:15.412Z",
            "post_id": "5966f6647abed889cc3eb349",
            "user_id": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal",
                "picture": "sssss"
            },
            "__v": 0
        }
         {
                    "_id": "59682e9781cced1504912f50",
                    "updatedAt": "2017-07-14T02:41:01.208Z",
                    "createdAt": "2017-07-14T02:38:15.412Z",
                    "post_id": "5966f6647abed889cc3eb349",
                    "user_id": {
                        "_id": "5966e6c423c15b84140313ea",
                        "name": "paijo",
                        "picture" : "sssss"
                    },
                    "__v": 0
                }
    ]
}
```

getting who like post

### Endpoint

`GET /user/activity/get_who_likes`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id   | true    | `_id` of posting
offset    | false   | `1` default offset is `0`
limit     | false   | `15` default limit is `10`
sort      | false   | `createdAt` default is `createdAt` `sort` could be anything

## Get Who Share

> Success Result

```json
{
    "error": false,
    "data": [
        {
            "_id": "59682e9781cced1504912f50",
            "updatedAt": "2017-07-14T02:41:01.208Z",
            "createdAt": "2017-07-14T02:38:15.412Z",
            "post_id": "5966f6647abed889cc3eb349",
            "user_id": {
                "_id": "5966e6c423c15b84140313ea",
                "name": "arizal",
                "picture": "sssss"
            },
            "__v": 0
        }
         {
                    "_id": "59682e9781cced1504912f50",
                    "updatedAt": "2017-07-14T02:41:01.208Z",
                    "createdAt": "2017-07-14T02:38:15.412Z",
                    "post_id": "5966f6647abed889cc3eb349",
                    "user_id": {
                        "_id": "5966e6c423c15b84140313ea",
                        "name": "paijo",
                        "picture" : "sssss"
                    },
                    "__v": 0
                }
    ]
}
```

getting who share post

### Endpoint

`GET /user/activity/get_who_share`

### Query Parameters

Parameter | Required | Example
--------- | ------- | -----------
post_id   | true    | `_id` of posting
offset    | false   | `1` default offset is `0`
limit     | false   | `15` default limit is `10`
sort      | false   | `createdAt` default is `createdAt` `sort` could be anything