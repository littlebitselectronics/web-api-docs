# Introduction

Welcome to the littleBits Mobile Application API reference docs. The littleBits.cc website itself has two existing API architecture's:

* One used and exposed primarily through the SpreeCommerce OpenSource framework
* another primarily used and exposed for littleBits CloudControl.

## API Responses

> Standard Response format

```json
{
	"results": {
		"value": "{what you asked for here}"
	},
	"meta": {
		"version": 2,
		"criteria": {
			"method": "{method used}",
			"endpoint": "/api/v2/{endpoint}",
			"params": [
				{
				"name": "{param}",
				"value": "{value}"
				}
			]
		},
		"success": true,
		"errors": "{error message if success false}"
	}
}
```

### LB API Response Format

Every response will be an object with two keys, results and meta. Results will be an object or array of objects depending on the end point. Or empty if there was an error. Meta describes the request you made.

* `version` - Number, What API version you are using.
* `criteria` - Object, How we processed your request.
	* `method` - String, What HTTP method was used.
	* `endpoint` - String, What endpoint you hit.
	* `params` - Array of Objects, An array of key-value objects that represent what the values for your params were, including optional ones you might not have specified.
* `success` - Boolean, if the request was successfully processed.
* `errors` - String, the error message associated with a false success value.