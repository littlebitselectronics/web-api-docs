# Users

## Get a user

```shell
curl "http://{server}/api/v2/users/7"
```

> The above command returns JSON structured like this:

```json
{
  "results": [
    {
      "id": 7,
      "username": "erin_littleBits",
      "twitter": "",
      "location": "boston, ma",
      "bio": "All the things!",
      "image": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/484/medium_DSC_4144_-_Version_2.JPG",
      "projects": [
        {
          "id": 176,
          "name": "Rudolph the Red-Nosed Reindeer",
          "slug": "rudolph-the-red-nosed-reindeer",
          "icon": "https://lb-community-staging.s3.amazonaws.com/uploads/lab/PurpleBit.jpg",
          "description": "Power + Pulse + RBG led = a littleBits powered blinking Rudolph nose!",
          "like_count": 1,
          "comment_count": 0,
          "user": {
            "id": 7,
            "image": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/484/small_DSC_4144_-_Version_2.JPG",
            "slug": "erin_littlebits",
            "username": "erin_littleBits"
          }
        },
      ]
    }
  ],
  "meta": {
    "version": 2,
    "criteria": {
      "method": "GET",
      "endpoint": "/api/v2/users/7",
      "params": [
        {
        "name": "id",
        "value": 7
        },
        {
        "name": "slug",
        "value": null
        }
      ]
    },
    "success": true,
    "errors": null
  }
}
```

`GET http://{server}/api/v2/users/{:id|:slug}`

### Examples

`GET http://{server}/api/v2/users/25038`

`GET http://{server}/api/v2/users/lev`
