# Projects Likes

## Like a Project

```shell
curl -X POST -H "MobileAppAuth: {api_key}" http://{server}/api/v2/projects/16/like
```

> The above command returns JSON structured like this:

```json
{
  "results": {
    "like_count":6
  },
  "meta":{
    "version":2.0,
    "criteria":
    {
      "method":"GET",
      "endpoint":"/api/v2/comments/project/16/like",
      "params": [
        {
          "name":"id",
          "value":16
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

`POST http://{server}/api/v2/projects/{:project_id}/like`

This request requires authentication.
