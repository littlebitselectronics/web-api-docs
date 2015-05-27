# Content

## GET Content

> To request CMS content, use this code:

```shell
curl -X GET https://{server_name}/api/v2/content?key="{your_content_key_here}"
```
> The above command returns JSON. We currently support two types of display responses: list and html.

> ### List

```json
{
	"results": {
		"display": "list",
		"content": [
			{
			"name": "power",
			"values": {
				"title": "It All Begins With Power",
				"value": "It's kind of important",
				"image": "https://lb-community.s3.amazonaws.com/uploads/image/asset/9531/card_feature_IMG_4778_-_Copy.JPG"
				}
			},
			{
			"name": "light",
			"values": {
				"title": "All Of The Lights",
				"value": "All of them!",
				"image": "https://lb-community.s3.amazonaws.com/uploads/image/asset/5953/large_filled_Sweater_IMG_7021LR.jpg"
				}
			}
		]
	},
	"meta": {
		"version": 2,
		"criteria": {
			"method": "GET",
			"endpoint": "/api/v2/content",
			"params": [
				{
				"name": "key",
				"value": "learn.lbbasics"
				}
			]
		},
		"success": true,
		"errors": null
	}
}
```

> ### HTML

```json
{
	"results": {
		"display": "html",
		"content": "<div class=\"container section-divider\">\ <h2 class=\"title-md section-title\">How it <strong class=\"purple\">Works</strong></h2>\ <div class=\"row\">\ <div class=\"\">\ <p class=\"section-sub-title\">The library has over 60 modules and growing. Every module works with every other in millions of combinations, you will never run out of things to make. Thousands of people are already inventing with littleBits. Join us!</p>\ </div></div></div>"
		},
	"meta": {
		"version": 2,
		"criteria": {
			"method": "GET",
			"endpoint": "/api/v2/content",
			"params": [
					{
					"name": "key",
					"value": "learn.play"
					}
				]
			},
		"success": true,
		"errors": null
	}
}
```

### Getting CMS Content

In order to retieve content from our server you will need a key. Keys are dot separated strings that allow for the creation of content that is simulateously structured and namespaced. An example is:

`content.landingpages.podcasts.android`

`.android` represents an instance of podcasts, while the key `.podcasts` respresents all of the podcast instances. 

### Responses

Every response object will have two keys: display and content. Currently, we support two types of display types: html and list. List is an array of json objects that respresent the items you requested. HTML is a block of HTML to display.

### Current Keys

Currently we only have to live keys as samples `learn.lbbasics` will return you a list of lbbasics objects. `learn.play` will return a blob of html to be rendered.
