# Product and Variants

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
        "type": "Bit",
        "bit_type": "input"
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
