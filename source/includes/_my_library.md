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
      "product_id": 201,
      "quantity": 2,
      "title": "cloudBit™",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything!",
      "type": "Bit",
      "bit_type": "wire",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2404/large/Cloud_2LR.jpg?1423168709",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2405/large/cloud_diagram2.png?1423168711"
      ]
    },
    {
      "variant_id": 13,
      "product_id": 13,
      "quantity": 1,
      "title": "usb power",
      "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
      "type": "Bit",
      "bit_type": "power",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1463/large/usbpower.jpg?1423166319",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1622/large/IMG_9861LR.jpg?1423166419",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2111/large/ProductImages_USBPower.jpg?1423167809"
      ]
    },
    {
      "variant_id": 179,
      "product_id": 166,
      "quantity": 5,
      "title": "USB Power Adapter + Cable",
      "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter to your",
      "type": "Accessory",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2251/large/WallAdapter_2LR.jpg?1423168341"
      ]
    },
    {
      "variant_id": 186,
      "product_id": 173,
      "quantity": 2,
      "title": "cloudBit module",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
      "type": "Bit",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2253/large/Cloud_2LR.jpg?1423168348"
      ]
    }
  ],
  "meta": {
    "version": 2,
    "criteria": {
      "method": "GET",
      "endpoint": "/api/v2/my_library",
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
 curl -X POST -d variant_id=216 http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
  "results": [
    {
      "variant_id": 13,
      "product_id": 13,
      "quantity": 1,
      "title": "usb power",
      "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
      "type": "Bit",
      "bit_type": "power",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1463/large/usbpower.jpg?1423166319",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1622/large/IMG_9861LR.jpg?1423166419",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2111/large/ProductImages_USBPower.jpg?1423167809"
      ]
    },
    {
      "variant_id": 179,
      "product_id": 166,
      "quantity": 4,
      "title": "USB Power Adapter + Cable",
      "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter  <a href",
      "type": "Accessory",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2251/large/WallAdapter_2LR.jpg?1423168341"
      ]
    },
    {
      "variant_id": 186,
      "product_id": 173,
      "quantity": 1,
      "title": "cloudBit module",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
      "type": "Bit",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2253/large/Cloud_2LR.jpg?1423168348"
      ]
    },
    {
      "variant_id": 216,
      "product_id": 201,
      "quantity": 1,
      "title": "cloudBit™",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything!",
      "type": "Bit",
      "bit_type": "wire",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2404/large/Cloud_2LR.jpg?1423168709",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2405/large/cloud_diagram2.png?1423168711"
      ]
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

**NOTE**: The following example is for incrementing the quantity of a kit Library Module (with variant_id=216) that already exists with a quantity of 2 in the user's library.
This will return more than one Library Module that represent the bits contained within the kit.

```shell
 curl -X PUT -d variant_id=216 -d operator="add" -d delta=1 http://<SERVER>/api/v2/my_library --user <HTTPUSER>:<HTTPPASSWORD> -H "MobileAppAuth: <USER_API_KEY>"
```

> JSON Response:

```json
{
  "results": [
    {
      "variant_id": 13,
      "product_id": 13,
      "quantity": 3,
      "title": "usb power",
      "description": "<strong>SHORT DESCRIPTION</strong><br>The USB power may be the smallest in the series, but it's big enough to send juice to all your creations. Connect",
      "type": "Bit",
      "bit_type": "power",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1333/large/IMG_8500RFLXLR.jpg?1423166105",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1463/large/usbpower.jpg?1423166319",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/1622/large/IMG_9861LR.jpg?1423166419",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2111/large/ProductImages_USBPower.jpg?1423167809"
      ]
    },
    {
      "variant_id": 179,
      "product_id": 166,
      "quantity": 5,
      "title": "USB Power Adapter + Cable",
      "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter to your",
      "type": "Accessory",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2251/large/WallAdapter_2LR.jpg?1423168341"
      ]
    },
    {
      "variant_id": 186,
      "product_id": 173,
      "quantity": 3,
      "title": "cloudBit module",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything! Retrofit your thermostat to control i",
      "type": "Bit",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2252/large/Cloud_1LR.jpg?1423168344",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2253/large/Cloud_2LR.jpg?1423168348"
      ]
    },
    {
      "variant_id": 216,
      "product_id": 201,
      "quantity": 3,
      "title": "cloudBit™",
      "description": "The cloudBit is the easiest way to create internet­-connected devices. You can now snap the internet to anything!",
      "type": "Bit",
      "bit_type": "wire",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2403/large/Cloud_1LR.jpg?1423168706",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2404/large/Cloud_2LR.jpg?1423168709",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2405/large/cloud_diagram2.png?1423168711"
      ]
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
  "results": [
    {
      "variant_id": 179,
      "product_id": 166,
      "quantity": 2,
      "title": "USB Power Adapter + Cable",
      "description": "This power adapter and USB cable combo is the perfect way to  power permanent creations! Simply connect the cable from the wall adapter to your",
      "type": "Accessory",
      "bit_type": null,
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2250/large/WallAdapter_1LR.jpg?1423168338",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2251/large/WallAdapter_2LR.jpg?1423168341"
      ]
    },
    {
      "variant_id": 201,
      "product_id": 185,
      "quantity": 3,
      "title": "MaKey MaKey",
      "description": "Visit the <a href=\\\"http://littlebits.cc/bitlab\\\">bitLab </a> to reserve your module!\\\r\\\n\\\r\\\nThe MaKey MaKey turns everyday objects into touchpads and combin",
      "type": "Bit",
      "bit_type": "wire",
      "images": [
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2328/large/MakeMakey_Module_6337LR.jpg?1423168548",
        "https://s3.amazonaws.com/lb-spree-staging/spree/products/2330/large/makeymakey4.JPG?1423168551"
      ]
    }
  ],
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

This endpoint deletes a Library Module from the user's library and returns all the remaining modules in the user's library.

**NOTE**: If the variant_id is for a kit, then all bit variants that belong to that kit will be deleted based on the quantity of the kit.

### HTTP Request

`DELETE http://<SERVER>/api/v2/my_library`

The following parameters should be passed as form data:

Parameter | Type  | Description
--------- | ----- | -----------
variant_id | integer | The ID of the product variant you are adding the user's library