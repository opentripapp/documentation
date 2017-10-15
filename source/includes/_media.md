# Media

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Upload Image
> Success Result

```json
{
  "error": false,
  "data": {
    "location": "https://s3-ap-southeast-1.amazonaws.com/opentrip-media/5933658b705c0a671c510acd_b33c20a2b602ecf6.jpg"
  }
}
```

create/upload image.

### Endpoint

`POST /media/upload/image`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
file | true | file of the image

## Delete Image
> Success Result

```json
{
  "error": false
}
```

remove/delete image.

### Endpoint

`DELETE /media/upload/image`

### Query Parameters
Parameter | Required | Description
--------- | ------- | -----------
filename | true | url image

