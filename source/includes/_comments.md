# Projects Comments

## Get comments

```shell
curl "http://{server}/api/v2/projects/774/comments"
```

> The above command returns JSON structured like this:

```json
{
  "results": [
    {
      "id":2996,
      "owner_id":15157,
      "body":"AWESOME!!!!  :)",
      "created_at":"2015-04-06T12:48:36.000Z",
      "replies":[]
    }
  ],
  "meta":{
    "version":2.0,
    "criteria":
    {
      "method":"GET",
      "endpoint":"/api/v2/comments/project/the-pune-rudefood",
      "params": [
        {
          "name":"page",
          "value":1
        },
        {
          "name":"per_page",
          "value":10
        },
        {
          "name":"id",
          "value":null
        },
        {
          "name":"slug",
          "value":"the-pune-rudefood"
        },
        {
          "name":"type",
          "value":"project"
        }
      ]
    },
    "success":true,
    "errors":null
  }
}
```

`GET http://{server}/api/v2/projects/{:project_id}/comments`

### Examples

`GET http://{server}/api/v2/projects/16/comments`

### Query Parameters

Parameter | Type  | Description
--------- | ----- | -----------
page | integer | Page number of returned results. Default is 1
per_page | integer | Number of results per page. Default is 10

## Create comment

```shell
curl -X POST -H "MobileAppAuth: {api_key}" -F "comment=first!" http://{server}/api/v2/projects/16/comments
```

> The above command returns JSON structured like this:

```json
{
  "results": [
    {
      "id":2996,
      "owner_id":15157,
      "body":"first!",
      "created_at":"2015-04-06T12:48:36.000Z",
      "replies":[]
    }
  ],
  "meta":{
    "version":2.0,
    "criteria":
    {
      "method":"GET",
      "endpoint":"/api/v2/comments/project/the-pune-rudefood",
      "params": [
        {
          "name":"id",
          "value":16
        },
        {
          "name":"type",
          "value":"project"
        },
        {
          "name":"body",
          "value":"first!"
        }
      ]
    },
    "success":true,
    "errors":null
  }
}
```

`POST http://{server}/api/v2/projects/{:project_id}/comments`

### Reply

`POST http://{server}/api/v2/projects/{:project_id}/comments/{:comment_id}`

This request requires authentication.

Parameter | Type  | Description
--------- | ----- | -----------
comment | string | Body of the comment.
