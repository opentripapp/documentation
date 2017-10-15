#Chat

## Get Personal Chat
> Success Result

```json
{
    "error": false,
    "data":{
               "results": {
                   "meta": {
                       "current_page": 1,
                       "total_room": 7
                   },
                   "rooms_info": [
                       {
                           "last_comment_id": 661730,
                           "last_comment_message": "Yoi bos",
                           "last_comment_timestamp": "2017-08-24T12:01:05Z",
                           "participants": [
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "tumpistudio@gmail.com",
                                   "id": 134079,
                                   "last_comment_read_id": 661730,
                                   "last_comment_received_id": 0,
                                   "username": "John doe"
                               },
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "muhammadarizals1@gmail.com",
                                   "id": 134024,
                                   "last_comment_read_id": 661682,
                                   "last_comment_received_id": 0,
                                   "username": "Arizal"
                               }
                           ],
                           "room_avatar_url": "",
                           "room_id": 31387,
                           "room_name": "John doe",
                           "room_type": "single",
                           "unread_count": 1
                       },
                       {
                           "last_comment_id": 661714,
                           "last_comment_message": "Ohayo",
                           "last_comment_timestamp": "2017-08-24T12:00:18Z",
                           "participants": [
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "muhammadarizals1@gmail.com",
                                   "id": 134024,
                                   "last_comment_read_id": 661714,
                                   "last_comment_received_id": 0,
                                   "username": "Arizal"
                               }
                           ],
                           "room_avatar_url": "",
                           "room_id": 31384,
                           "room_name": "",
                           "room_type": "single",
                           "unread_count": 0
                       },
                       {
                           "last_comment_id": 0,
                           "last_comment_message": "",
                           "last_comment_timestamp": "2017-08-24T11:22:14Z",
                           "participants": [
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "muhammadarizals1@gmail.com",
                                   "id": 134024,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "Arizal"
                               },
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "tes5@tes.com",
                                   "id": 134042,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "pasijo"
                               }
                           ],
                           "room_avatar_url": "",
                           "room_id": 31375,
                           "room_name": "pasijo",
                           "room_type": "single",
                           "unread_count": 0
                       },
                       {
                           "last_comment_id": 0,
                           "last_comment_message": "",
                           "last_comment_timestamp": "2017-08-24T11:10:39Z",
                           "participants": [
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "tes@tes.com",
                                   "id": 134028,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "ssttuiui "
                               },
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "muhammadarizals1@gmail.com",
                                   "id": 134024,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "Arizal"
                               }
                           ],
                           "room_avatar_url": "",
                           "room_id": 31369,
                           "room_name": "ssttuiui ",
                           "room_type": "single",
                           "unread_count": 0
                       },
                       {
                           "last_comment_id": 0,
                           "last_comment_message": "",
                           "last_comment_timestamp": "2017-08-24T11:09:41Z",
                           "participants": [
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "test",
                                   "id": 133818,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "sssasdassdasd"
                               },
                               {
                                   "avatar_url": "https://qiscuss3.s3.amazonaws.com/uploads/55c0c6ee486be6b686d52e5b9bbedbbf/2.png",
                                   "email": "muhammadarizals1@gmail.com",
                                   "id": 134024,
                                   "last_comment_read_id": 0,
                                   "last_comment_received_id": 0,
                                   "username": "Arizal"
                               }
                           ],
                           "room_avatar_url": "",
                           "room_id": 31368,
                           "room_name": "sssasdassdasd",
                           "room_type": "single",
                           "unread_count": 0
                       }
                   ]
               },
               "status": 200
           }
}
```
get user personal chat

### Endpoint

`GET /chat/personal`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
page        | optional    | 1

## Get Group Chat
> Success Result

```json
{
    "error": false,
    "data":{
               "results": {
                   "meta": {
                       "current_page": 1,
                       "total_room": 7
                   },
                   "rooms_info": [
                        {
                                      "last_comment_id": 0,
                                      "last_comment_message": "",
                                      "last_comment_timestamp": "2017-09-03T07:20:37Z",
                                      "room_avatar_url": "",
                                      "room_id": 32898,
                                      "room_name": "trip name",
                                      "room_type": "group",
                                      "unread_count": 0
                                  },
                                  {
                                      "last_comment_id": 0,
                                      "last_comment_message": "",
                                      "last_comment_timestamp": "2017-09-03T07:13:34Z",
                                      "room_avatar_url": "",
                                      "room_id": 32896,
                                      "room_name": "trip name",
                                      "room_type": "group",
                                      "unread_count": 0
                                  },
                   ]
               },
               "status": 200
           }
}
```
get user group chat

### Endpoint

`GET /chat/group`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
page        | optional    | 1


## Leave Chat
> Success Result

```json
{
    "error": false
}
```
user leave chat
### Endpoint

`POST /chat/leave`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
room_id        | true    | "2324324"
