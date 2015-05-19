# My Library

## Get All Modules

```shell
curl "http://{server}/api/mylibrary/{:id}"
  -H "MobileAppAuth: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "version": "1.0",
    "href": "http://littlbits.cc/api/mylibrary/54786",
    "items": [
        {
            "id": 2,
            "name": "light trigger",
            "description": "The light trigger is a clever module: it senses how much light is around it, and sends an ON signal once the light reaches a certain brightness. Use th",
            "price": "18.0",
            "href": "http://littlebits/cc/some-product-url",
            "image": "http://aws.amazon.com/image_url",
            "category": "bits",
            "type": "power",
            "images": {
              "feature": "http://aws.amazon.com/image_url",
              "mini": "http://aws.amazon.com/image_url",
              "thumb": "http://aws.amazon.com/image_url"
            }
        }
    ]
}
```

This endpoint retrieves all modules in the users library.

### HTTP Request

`GET http://{server}/api/mylibrary/{:id}`

<aside class="success">
The :id can be obtained from the authentication response
</aside>
