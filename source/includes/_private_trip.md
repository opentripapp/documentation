# Private Trip

## Create Request Private Trip


create private trip request

### Endpoint

`POST /trip/private_trip`

### Body Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
name  | true    | user name
phone_number | true    | phone number
email | true    | user email address
destination | true    | user email address
participants | true    | how many participants
day_of_trip | true    | length of trip
meeting_point_name | true    | name of meeting point
meeting_point | optional   | metting point location, use array [longitude,latitude]
additional_note | optional   | notes
trip_date | true    | date of trip (start date) format "yyyy-MM-dd" `2017-05-21`


## Get Request Private Trip

get private trip request

### Endpoint

`GET /trip/private_trip`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | optional   | `0` default offset is `0`
limit     | optional   | `10` default limit is `15`
sort    | optional   | sorting
how_many | optional | number
destination | optional | destination name

## Get My Request Private Trip


get private trip request

### Endpoint

`GET /trip/private_trip/me`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
offset    | optional   | `0` default offset is `0`
limit     | optional   | `10` default limit is `15`
sort    | optional   | sorting
how_many | optional | number
destination | optional | destination name

## Delete My Request Private Trip
> Success Result

```json
{
    "error": false
}
```

delete private trip request

### Endpoint

`DELETE /trip/private_trip`

### Query Parameters
Parameter | Required | Example/Description
--------- | ------- | -----------
id    | true   | request id


