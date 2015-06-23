# Product and Variants

## GET All Products

> To request all products with all of it's variants and images, use this code:

```shell
curl -X GET https://{server_name}/api/v2/products"
```
> To request the a product with all of it's variants and images, use this code:

> ### Example

```json
{
  "results": [
    {
      "id": 1,
      "name": "fan",
      "type": "Bit",
      "bit_type": "output",
      "bit_variant_ids": [],
      "description": "The fan Bit is just what you'd think: a small electric fan tethered to a littleBits module. It's great for those hot summer nights. Use our little fan to create fluttering movement in your creations or just to keep yourself cool.\\\r\\\n\\\r\\\nCheck out our <b> <a href=\\\"http://littlebits.cc/tips-tricks-the-fan-bit\\\" target=\\\"_blank\\\">Tips + Tricks</a></b> for more ideas on using the fan.",
      "slug": "fan",
      "available_on": "2012-12-17T00:00:00.000Z",
      "updated_at": "2015-06-17T20:21:48.000Z",
      "short_description": "The fan Bit is just what you'd think: a small electric fan tethered to a littleBits module. It's great for those hot summer nights. Use our little fan ",
      "inactive": false,
      "variants": [
        {
          "id": 1,
          "type": "Bit",
          "bit_type": "output",
          "is_master": true,
          "images": [
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1353/product/IMG_8722RFLXLR.jpg?1423166165",
              "position": 1,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1439/product/fan.jpg?1423166254",
              "position": 2,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1648/product/Fan.gif?1423166521",
              "position": 3,
              "type": "image/gif"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2082/product/ProductImages_Fan.jpg?1423167715",
              "position": 4,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2220/product/Bit_Card_50_o13_Fan.jpg?1423168255",
              "position": 5,
              "type": "image/jpeg"
            }
          ],
          "kit_bits": []
        }
      ]
    },
    {
      "id": 198,
      "name": "Arduino Coding Kit",
      "type": "Kit",
      "bit_type": null,
      "bit_variant_ids": [
        137,
        136,
        138,
        83,
        25,
        26,
        42
      ],
      "description": "<strong>YOU BRING THE CODE. <br> \\\r\\\nWE'LL BRING THE ELECTRONICS. </strong><br>\\\r\\\n<br>\\\r\\\n<p>This kit contains 8 of our favorite prototyping modules. It’s everything you need to get started with electronics and programming. \\\r\\\n\\\r\\\nMake your own Etch-a-Sketch&#153;! Program a visual display! We’ll walk you through the basics using the Arduino programming environment, without the breadboarding, soldering or wiring normally required. Perfect for hackers, designers, makers and tinkerers of all levels. </p> \\\r\\\n<br>\\\r\\\n<li>Includes everything you need to get started (battery + power included!) right out of the box</li>\\\r\\\n<li>Build with 8 Getting Started sketches, including a DIY Etch-a-Sketch&#153;, Mouse Control and hundreds more from Arduino’s community!</li>\\\r\\\n<li>Communicate with software (Processing, MaxMSP, Flash etc…)</li>\\\r\\\n<li>Snap modules easily to 3 inputs and 3 outputs on the Arduino module, as well as additional I/O for advanced hardware interaction</li>\\\r\\\n<li>Access to community support from Arduino AND littleBits</li>\\\r\\\n<br>\\\r\\\n\\\r\\\nThe Arduino module is also available individually <strong><a href=\\\"http://littlebits.cc/bits/arduino/\\\">here</a> </strong>.\\\r\\\n\\\r\\\n<hr>\\\r\\\n<b>GETTING STARTED\\\r\\\n<li><a href=\\\"http://discuss.littlebits.cc/t/getting-started-with-arduino/109\\\"_blank\\\">Forums</a></li>\\\r\\\n<li><a href=\\\"http://littlebits.cc/tips-tricks-arduino-module\\\" target=\\\_blank\\\">Tips + Tricks</a></li></b>",
      "slug": "arduino-coding-kit",
      "available_on": "2014-11-09T00:00:00.000Z",
      "updated_at": "2015-06-17T20:26:37.000Z",
      "short_description": "Contains 8 modules to get you started with electronics and programming.",
      "inactive": false,
      "variants": [
        {
          "id": 213,
          "type": "Kit",
          "bit_type": null,
          "is_master": true,
          "images": [
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2484/product/ACK-kit-bits_LR.jpg?1423169038",
              "position": 0,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2492/product/jpeg.jpg?1423169057",
              "position": 1,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2507/product/arduinodiagram2.jpg?1423169092",
              "position": 2,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2488/product/Screenshot_2014-11-25_14.53.08.png?1423169042",
              "position": 3,
              "type": "image/png"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2491/product/Screenshot_2014-11-25_18.16.58.png?1423169053",
              "position": 4,
              "type": "image/png"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2509/product/diyetch.jpg?1423169095",
              "position": 5,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2506/product/arduino_screensaver.jpg?1423169089",
              "position": 6,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2510/product/pong.jpg?1423169098",
              "position": 7,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2402/product/ArduinoStarterKit_HR_Photoshopped-rgb.jpg?1423168694",
              "position": 8,
              "type": "image/jpeg"
            },
            {
              "url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2410/product/arduino-kit.png?1423168763",
              "position": 9,
              "type": "image/png"
            }
          ],
          "kit_bits": [
            {
              "variant_id": 152,
              "product_id": 139,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 101,
              "product_id": 101,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 40,
              "product_id": 40,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 38,
              "product_id": 38,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 29,
              "product_id": 29,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 24,
              "product_id": 24,
              "quantity": 2,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 23,
              "product_id": 23,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 22,
              "product_id": 22,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 21,
              "product_id": 21,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:32.000Z"
            },
            {
              "variant_id": 51,
              "product_id": 51,
              "quantity": 1,
              "updated_at": "2015-06-15T18:41:36.000Z"
            }
          ]
        }
      ]
    }
  ],
  "meta": {
    "version": 2,
    "criteria": {
      "method": "GET",
      "endpoint": "/api/v2/products",
      "params": [
        {}
      ]
    },
    "success": true,
    "errors": null
  }
}
```

### Return

This returns all active or retired product with all of their variants and their associated images.

Note:

* Kit products will have a `bit_variant_ids` node with all bit variant id's that are inside the kit within their JSON structure.

* Bit products have a `bit_type` node.

* All products have a `type` node


## GET Product

> To request the a product with all of it's variants and images, use this code:

```shell
curl -X GET https://{server_name}/api/v2/products/{:id}"
```
> The above command returns JSON.

> ### Example

```json
{
	"results": {
		"id": 4,
		"name": "slide dimmer",
         "type": "Bit",
        "bit_type": "input",
		"description": "You control the slide dimmer Bit by moving its lever from one end of the Bit to the other. It functions just like a light dimmer you might find at home, or a volume fader in a recording studio. Follow it with an LED for some adjustable mood lighting.\ \ \ \ Check out our <b> <a href=\"http://littlebits.cc/fridays-tips-tricks-the-slide-dimmer-and-dimmer-bits\" target=\"_blank\">Tips + Tricks</a></b> for more ideas on using the slide dimmer.",
		"slug": "slide-dimmer",
		"available_on": "2012-12-16T00:00:00.000Z",
		"updated_at": "2015-05-11T16:54:46.000Z",
		"short_description": "You control the slide dimmer Bit by moving its lever from one end of the Bit to the other. It functions just like a light dimmer you might find at home",
		"cost": 0,
		"inactive": false,
		"variants": [
			{
				"id": 4,
				"is_master": true,
                "type": "Bit",
                "bit_type": "input",
				"images": [
					{
					"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1349/product/IMG_8529RFLXLR.jpg?1423166155",
					"position": 1,
					"type": "image/jpeg"
					},
					{
					"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1458/product/slidedimmer.jpg?1423166301",
					"position": 2,
					"type": "image/jpeg"
					}
				]
			}
		]
	},
	"meta": {
	"version": 2,
	"criteria": {
		"method": "GET",
		"endpoint": "/api/v2/products/85",
		"params": [
			{
			"name": "product_id",
			"value": "85"
			}
		]
	},
	"success": true,
	"errors": null
	}
}
```

### Return

This returns a product with all of it's variants and their associated images.

## GET Variant

> To request the a variant of a product and all of its images, use this code:

```shell
curl -X GET https://{server_name}/api/v2/products/{:product_id}/variants/{:id}"
```
> The above command returns JSON.

> ### Example

```json
{
	"results": {
		"id": 4,
        "type": "Bit",
        "bit_type": "input",
		"is_master": true,
		"images": [
			{
			"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1349/product/IMG_8529RFLXLR.jpg?1423166155",
			"position": 1,
			"type": "image/jpeg"
			},
			{
			"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1458/product/slidedimmer.jpg?1423166301",
			"position": 2,
			"type": "image/jpeg"
			},
			{
			"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/1665/product/SlideDimmer.gif?1423166619",
			"position": 3,
			"type": "image/gif"
			},
			{
			"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2121/product/ProductImages_SlideDimmer.jpg?1423167844",
			"position": 4,
			"type": "image/jpeg"
			},
			{
			"url": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2176/product/Bit_Card_07_i5_SlideDimmer.jpg?1423168068",
			"position": 5,
			"type": "image/jpeg"
			}
		]
	},
	"meta": {
		"version": 2,
		"criteria": {
			"method": "GET",
			"endpoint": "/api/v2/products/4/variants/4",
			"params": [
				{
				"name": "variant_id",
				"value": "4"
				},
				{
				"name": "product_id",
				"value": "4"
				}
			]
		},
		"success": true,
		"errors": null
	}
}
```

### Return

This returns a product with all of it's variants and their associated images.
