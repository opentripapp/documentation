#Notification

## Add Device

```shell
curl -X POST \
  http://localhost:8000/add_token \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 0195ba7b-9f4a-bef6-2cdd-d324293dd165' \
  -H 'user-id: 59c5c89665a538001088798f' \
  -d '{
	"device_id":"123",
	"client_token":"12212121212121asdlaskm3",
	"client_agent":"etc"
}'
```

> Success Result

```json
{
    "error": false
}
```

add user player id (oneSignal)

### Endpoint

`POST /notifications/add_token`

### Body Parameters
Parameter | Required | Description
--------- | ------- | -----------
device_id | true | unique device id
client_token | true | players id from onesignal
client_agent | true | device type, android,ios,or web


## Log Out

```shell
curl -X DELETE \
  'http://localhost:8000/logout?device_id=123&client_agent=etc' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: ece90638-64e3-7e8c-2829-78b4a285af0e' \
  -H 'user-id: 59c5c89665a538001088798f'
```
> Success Result

```json
{
    "error": false
}
```

User logOut

### Endpoint

`DELETE /notifications/logout`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
device_id | true | unique device id
client_agent | true | device type, android,ios,or web


## Get Notifications Config

> Success Result

```json
{
    "data": {
        "unread_notification": 0
    },
    "error": false
}
```

get unread notifications

### Endpoint

`GET /notifications/config`


## Set Notification as Read

> Success Result

```json
{
    "error": false
}
```

set all notifications as read

### Endpoint

`POST /notifications/set_read`

## Set A Notification as Read

> Success Result

```json
{
    "error": false
}
```

set single notifications as read

### Endpoint

`POST /notifications/set_read/:notification_id`



## Get List of Notification


get list of all notifications

### Endpoint

`GET /notifications/list`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | false   | `0` default offset is `0`
limit     | false   | `10` default limit is `15`
is_read   | false   | `true` or `false`

## Delete A Notification

> Success Result

```json
{
    "error": false
}
```

delete single notifications

### Endpoint

`DELETE /notifications/delete/:notification_id`

## Delete Notification

> Success Result

```json
{
    "error": false
}
```

delete all notifications

### Endpoint

`DELETE /notifications/delete`