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
        "like_count": 1,
        "comment_count": 0,
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

### Query Parameters

Parameter | Type  | Description
--------- | ----- | -----------
q | string | Search projects by keyword
tag | string | Return projects with a given tag
bits | integer | Return projects with this product ID. Can be a comma separated list.
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
  "results": [
    {
      "id": 2055,
      "name": "Sounding Box #11",
      "description": "Sounding Box #11 is the first piece to go public in a series of acoustic sculptures that allow viewers...",
      "user": {
        "id": 47312,
        "image": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/small_Caselden_Studios_high_res.png",
        "slug": "caselden_studios",
        "username": "Caselden_Studios"
      },
      "credits": "God",
      "like_count": 10,
      "comment_count": 1,
      "images": [
        "https://lb-community-staging.s3.amazonaws.com/uploads/image/asset/7755/large_filled_IMG_6771.jpg"
      ],
      "tools": [
        "3D Printers"
      ],
      "products": [
        {
          "id": 139,
          "image": "https://s3.amazonaws.com/lb-spree-staging/spree/products/2046/small/arduino_withlogo.jpg?1423167635",
          "name": "Arduino",
          "quantity": 2
        }
      ],
      "materials": [
        {
          "name": "Assorted Paints and Finishing Oils",
          "quantity": 1
        }
      ],
      "steps": [
        {
          "number": 1,
          "description": "<b>Make a sound box:</b><br>Design a resonating wooden chamber. We took design influence from..."
        }
      ]
    }
  ],
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

### Examples

`GET http://{server}/api/v2/projects/16`

`GET http://{server}/api/v2/projects/robot`
