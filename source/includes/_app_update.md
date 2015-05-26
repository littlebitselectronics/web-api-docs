# App Update

## GET Current App State

> To request the current status of the application, use this code:

```shell
curl -X GET https://{server_name}/api/v2/app_update"
```
> The above command returns JSON structured.

> ### Example

```json
{
	"results": {
		"version": 1,
		"viewforia": 1,
		"css": 1,
		"appData": {
			"projects": [
				{
				"id": 16,
				"updated_at": "2015-05-11T13:42:53.000Z"
				},
				{
				"id": 18,
				"updated_at": "2015-05-08T13:56:53.000Z"
				},
				{
				"id": 3299,
				"updated_at": "2015-05-11T13:40:27.000Z"
				}
			],
			"variants": [
				{
				"product_id": 1,
				"variant_id": 1,
				"updated_at": "2015-05-11T16:54:46Z"
				},
				{
				"product_id": 3,
				"variant_id": 3,
				"updated_at": "2015-05-11T13:42:49Z"
				},
				{
				"product_id": 4,
				"variant_id": 4,
				"updated_at": "2015-05-11T16:54:46Z"
				}
			],
		"keys": [
				{
				"key": "learn.lbbasics",
				"updated_at": "2015-05-11T16:54:46Z"
				},
				{
				"key": "learn.play",
				"updated_at": "2015-05-05T16:32:46Z"
				}
			]
		}
	},
	"meta": {
		"version": 2,
		"criteria": {
			"method": "GET",
			"endpoint": "/api/v2/app_update",
			"params": null
		},
		"success": true,
		"errors": null
	}
}
```


### Understanding the information

* `version` - Number, What the newest version of the app is. If there is a major increment, eg 1.2 to 2.0 then it represents a forced update - go to the app store and get the new version before you can use it again. Minor increments, 1.3 to 1.4 are optional updates.
* `viewforia` - Number, What the most recent version of the viewforia binary is. Any increment in version number requries an update.
* `css` - Number, What the most recent version of the css for html web view rendering is. Any increment in version number requries an update.
* `app_data` - Object, Contains the keys to look at for content caching. All keys are arrays of objects with and id/ids and an updated at property.
	* `projects` - Array of Objects, Each object contains `id` and `updated_at` keys that the current projects for the app and when they were last updated in our system.
	* `variants` - Array of Objects, Each object contains `product_id`, `variant_id`, and `updated_at` keys that represent the current products by variant for the app and when they were last updated in our system.
	* `keys` - Array of Objects, Each object contains `key` and `updated_at` keys that the current keys for the app and when they were last updated in our system.

### How to process the response

For each of the sections of app data, if you have an `id` that is no longer in the list, then you can delete it. If there is an `id` that you don't have, retrieve it. If there is an `id` you already have cached but the `updated_at` is more recent, then get the new version. If you have the key and the updated_at is the same, the just leave it.

