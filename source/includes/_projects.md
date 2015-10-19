# Projects

## Get all published projects

```shell
curl "http://{server}/api/v2/projects?per_page=1"
```

> The above command returns JSON structured like this:

```json
{
  "results": [
      {
        "id": 16,
        "name": "littlePiggy Bank",
        "slug": "littlepiggy-bank--3",
        "icon": "https://lb-community-staging.s3.amazonaws.com/uploads/image/asset/776/small_pig3_interaction2_highRes.jpg",
        "description": "Interactive piggy bank that RINGS frantically to thank you for feeding it, BUZZES and LIGHTS up when you pet it’s ear, and SITS quietly when you want it to!<br>",
        "comment_count": 0,
        "like_count": 1,
        "liked_by_user": true,
        "user": {
          "id": 1750,
          "image": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/17/small_icon-green-ohhh.png",
          "slug": "littlebits",
          "username": "littleBits"
        }
      }
    ],
    "meta": {
      "criteria": {
        "method": "GET",
        "endpoint": "/api/v1/projects",
        "params": [
          {
            "name": "page",
            "value": 1
          },
          {
            "name": "per_page",
            "value": "1"
          }
        ]
      },
      "success": true,
      "errors": null
    }
}
```

`GET http://{server}/api/v2/projects/`

This request can be optionally authenticated to receive `liked_by_user`.

### Query Parameters

Parameter | Type  | Description
--------- | ----- | -----------
page | integer | Page number of returned results. Default is 1
per_page | integer | Number of results per page. Default is 10


## Search projects

```shell
curl "http://{server}/api/v2/projects/search?q=pig?per_page=1"
```

> The above command returns JSON structured like previously.


`GET http://{server}/api/v2/projects/search`

This request can be optionally authenticated to receive `liked_by_user`.

### Query Parameters

Parameter | Type  | Description
--------- | ----- | -----------
q | string | Search projects by keyword
sort | string | Sort projects by most recent or popular. Accepts either `recent` or `popular`
tags | string | Return projects with a given tag
type | string | Defaults to projects only. Use `lesson` for lessons only.
variants | integer | Return projects with these variant IDs and not any others. Should be a comma separated list.
qty | integer | Return projects with this quantity of a corresponding variant ID. Must be a comma separated list of the same size as the list of variants.
user | integer | Return projects of a given user ID
page | integer | Page number of returned results. Default is 1
per_page | integer | Number of results per page. Default is 10


## Get a project

```shell
curl "http://{server}/api/v2/projects/2055"
```

> The above command returns JSON structured like this:

```json
{
  "results":
  {
    "id": 2055,
    "name": "Sounding Box #11",
    "description": "Sounding Box #11 is the first piece to go public in a series of acoustic sculptures that allow viewers...",
    "comment_count": 1,
    "like_count": 10,
    "liked_by_user": false,
    "user": {
      "id": 47312,
      "image": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/small_Caselden_Studios_high_res.png",
      "slug": "caselden_studios",
      "username": "Caselden_Studios"
    },
    "credits": "God",
    "images": [
      {
        "id": 15,
        "url": "https://lb-community-staging.s3.amazonaws.com/uploads/image/asset/7755/large_filled_IMG_6771.jpg"
      }
    ],
    "embeds": [
      {
        "id": 5,
        "service": "youtube.com",
        "code": "<iframe width=\"560\" height=\"315\" src=\"//www.youtube.com/embed/IYJSEPD9T40\" frameborder=\"0\" allowfullscreen></iframe>"
      }
    ],
    "files": [],
    "tools": [
      {
        "id": 1,
        "name": "3D Printers"
      }
    ],
    "products": [
      {
        "product_id": 139,
        "variant_id": 133,
        "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2046/small/arduino_withlogo.jpg?1423167635",
        "name": "Arduino",
        "quantity": 2
      }
    ],
    "materials": [
      {
        "id": 4,
        "name": "Assorted Paints and Finishing Oils",
        "quantity": 1
      }
    ],
    "steps": [
      {
        "id": 2,
        "number": 1,
        "title": "i am a jolly step title",
        "description": "<b>Make a sound box:</b><br>Design a resonating wooden chamber. We took design influence from...",
        "images": [
          {
            "id": 9896,
            "url": "https://lb-community-staging.s3.amazonaws.com/uploads/image/asset/9896/large_filled_PurpleBit.jpg",
            "caption": "Picture 1"
          }
        ]
      }
    ]
  },
  "meta": {
    "criteria": {
        "method": "GET",
        "endpoint": "/api/v1/projects/2055",
        "params": [
          {
            "name": "id",
            "value": 2055
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

`GET http://{server}/api/v2/projects/{:id|:slug}`

This request can be optionally authenticated to receive `liked_by_user`.

### Examples

`GET http://{server}/api/v2/projects/16`

`GET http://{server}/api/v2/projects/robot`
