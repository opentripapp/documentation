#Notification

## Add Device

> Success Result

```json
{
    "error": false
}
```

add user FCM Token

### Endpoint

`POST /notifications/add_device`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
device_token | true | device generated token for fcm


## Log Out

> Success Result

```json
{
    "error": false
}
```

User logOut

### Endpoint

`POST /notifications/logout`


## Get Unread Notifications

> Success Result

```json
{
    "error": false,
    "data":{
        "count":2
    }
}
```

get unread notifications

### Endpoint

`GET /notifications/unreads`

## Set Notification as Read

> Success Result

```json
{
    "error": false
}
```

set all notifications as read

### Endpoint

`PUT /notifications`

## Set A Notification as Read

> Success Result

```json
{
    "error": false
}
```

set single notifications as read

### Endpoint

`PUT /notifications/::notification_id`




## Get List of Notification
> Success Result

```json
{
    "error": false,
    "data":[
        {
            "type":"trip_full",
            "message":"your trip is full",
            "data":"trip id",
            "read":false
        },
         {
            "type":"join_trip",
            "message":"andika join your trip",
            "data":"trip id misalnya",
            "read":false
        },
        {
            "type":"join_trip",
            "message":"andika join your trip",
            "data":"user id misalnya",
            "read":false
        },
        {
            "type":"upcoming_trip",
            "message":"upcoming trip pada tanggal",
            "data":"user id misalnya",
            "read":false
        }
    ]
}
```

get list of all notifications

### Endpoint

`GET /notifications/list`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id        | true    | trip id
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `15`