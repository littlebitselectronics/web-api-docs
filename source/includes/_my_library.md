# My Library

## GET all modules

```shell
curl http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
    "results": [
        {
            "variant_id": 216,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit™",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
            "quantity": 1,
            "type": "Kit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706"
            }
        },
        {
            "variant_id": 13,
            "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
            "title": "usb power",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
            "quantity": 1,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105"
            }
        },
        {
            "variant_id": 186,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit module",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
            "quantity": 1,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344"
            }
        }
    ],
    "meta": {
        "version": 2,
        "criteria": {
            "method": "GET",
            "endpoint": "/api/v2/my_library.json",
            "params": null
        },
        "success": true,
        "errors": null
    }
}
```

This endpoint shows all modules in a user's library

### HTTP Request

`GET http://{server}/api/v2/my_library`

## CREATE new module

```shell
 curl -X POST -d variant_id=201 http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
    "results": [
        {
            "variant_id": 13,
            "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
            "title": "usb power",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
            "quantity": 1,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105"
            }
        },
        {
            "variant_id": 179,
            "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter to your,
            "title": "USB Power Adapter + Cable",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
            "quantity": 1,
            "type": "Accessory",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338"
            }
        },
        {
            "variant_id": 186,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit module",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
            "quantity": 1,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344"
            }
        },
        {
            "variant_id": 216,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit™",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
            "quantity": 1,
            "type": "Kit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706"
            }
        }
    ],
    "meta": {
        "version": 2,
        "criteria": {
            "method": "POST",
            "endpoint": "/api/v2/my_library",
            "params": [
                {
                    "name": "variant_id",
                    "value": "216"
                }
            ]
        },
        "success": true,
        "errors": null
    }
}
```

This endpoint creates a Library Module based on a product's variant_id, adds it the user's library with a quantity of 1, and returns the added Library Module(s).

**NOTE**: If the variant_id is for a kit, then all bit variants that belong to that kit will be added to the user's library and returned in the JSON structure as well.

### HTTP Request

`POST http://<SERVER>/api/v2/my_library`

The following parameters should be passed as form data:

Parameter | Type  | Description
--------- | ----- | -----------
variant_id | integer | The ID of the product variant you are adding the user's library

## UPDATE existing module

**NOTE**: The following example is for incrementing the quantity of a kit Library Module (with variant_id=201) that already exists with a quantity of 1 in the user's library.
This will return more than one Library Module that represent the bits contained within the kit.

```shell
 curl -X PUT -d variant_id=201 -d operator="add" -d delta=1 http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
    "results": [
        {
            "variant_id": 13,
            "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
            "title": "usb power",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
            "quantity": 2,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105"
            }
        },
        {
            "variant_id": 179,
            "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter to your,
            "title": "USB Power Adapter + Cable",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
            "quantity": 2,
            "type": "Accessory",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338"
            }
        },
        {
            "variant_id": 186,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit module",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
            "quantity": 2,
            "type": "Bit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344"
            }
        },
        {
            "variant_id": 216,
            "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
            "title": "cloudBit™",
            "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
            "quantity": 2,
            "type": "Kit",
            "images": {
                "feature": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "mini": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
                "thumb": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706"
            }
        }
    ],
    "meta": {
        "version": 2,
        "criteria": {
            "method": "PUT",
            "endpoint": "/api/v2/my_library",
            "params": [
                {
                    "name": "variant_id",
                    "value": "216"
                },
                {
                    "name": "delta",
                    "value": "1"
                },
                {
                    "name": "operator",
                    "value": "add"
                }
            ]
        },
        "success": true,
        "errors": null
    }
}
```

This endpoint updates a Library Module based on a product's variant_id. It will either add or subtract a Library Module from the user's library, based on the delta and operator parameters it is given.

**NOTE**: If the variant_id belongs to a kit, then all bit variants that belong to that kit will be added to or subtracted from the user's library and returned in a JSON structure as well.

### HTTP Request

`PUT http://<SERVER>/api/v2/my_library`

The following parameters should be passed as form data:

Parameter | Type  | Description
--------- | ----- | -----------
variant_id | integer | The ID of the product variant you are adding the user's library
operator | string | Either "add" or "subtract".
delta | integer | The quantity that you wish to add or subtract (must be positive)



## DELETE module

```shell
  curl -X DELETE -d variant_id=216 http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
    "results": [],
    "meta": {
        "version": 2,
        "criteria": {
            "method": "DELETE",
            "endpoint": "/api/v2/my_library",
            "params": [
                {
                    "name": "variant_id",
                    "value": "216"
                }
            ]
        },
        "success": true,
        "errors": null
    }
}
```

This endpoint deletes a Library Module from the user's library.

**NOTE**: If the variant_id is for a kit, then all bit variants that belong to that kit will be deleted based on the quantity of the kit.

### HTTP Request

`DELETE http://<SERVER>/api/v2/my_library`

The following parameters should be passed as form data:

Parameter | Type  | Description
--------- | ----- | -----------
variant_id | integer | The ID of the product variant you are adding the user's library