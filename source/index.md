---
title: littleBitsAPI Reference

language_tabs:
  - shell

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - status_codes

search: true
---

# Introduction

Welcome to the littleBits Mobile Application API reference docs. The littleBits.cc website itself has two existing API architecture's:

* One used and exposed primarily through the SpreeCommerce OpenSource framework
* another primarily used and exposed for littleBits CloudControl.

# Authentication

> To request a user's authorization token, use this code:

```shell
curl --data "mobile_app[email]=you@example.com&mobile_app[password]=savekittens"
https://{server_name}/api/mobile_app_sessions
```
> The above command returns JSON structured like this:

```json
  {
    "id": 54786,
    "first_name": null,
    "last_name": null,
    "avatar": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/blueModule.png",
    "username": "someperson001",
    "mobile_auth_token": "aaaaaaaaaaaaaaaaaaaaaaaaa"
  }
```

> To authorize, use this code:


```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "MobileAppAuth: {mobile_auth_token}"
```

### Testing on Staging Servers

While testing on Staging servers (stg1,stg2, pre-live, etc.) most requests are protected via HTTP Basic Auth. Therefore each HTTP Request must be prefaced with username/password like:

`username:password@stg1.littlebits.cc`

or

`username:password@pre-live.littlebits.cc`


### HTTP Request

`POST http://{server}/api/mobile_app_sessions`

### Form Data

Parameter | Description
--------- | -----------
mobile_app[email] | End user's email address
mobile_app[password] | End users' password


The API uses keys to grant access. A users mobile authentication token is returned in response to successful email and password authentication.

The API expects mobile authentication token to be included in subseqeunt API requests in a header that looks like the following:

`MobileAppAuth: meowmeowmeow`

<aside class="notice">
You must replace `meowmeowmeow` with the users mobile_auth_token.
</aside>

# My Library

## Get All Modules

```shell
curl "http://{server}/api/mylibrary/{:id}"
  -H "MobileAppAuth: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "version": "1.0",
    "href": "http://littlbits.cc/api/mylibrary/54786",
    "items": [
        {
            "id": 2,
            "name": "light trigger",
            "description": "The light trigger is a clever module: it senses how much light is around it, and sends an ON signal once the light reaches a certain brightness. Use th",
            "price": "18.0",
            "href": "http://littlebits/cc/some-product-url",
            "image": "http://aws.amazon.com/image_url",
            "category": "bits",
            "type": "power",
            "images": {
              "feature": "http://aws.amazon.com/image_url",
              "mini": "http://aws.amazon.com/image_url",
              "thumb": "http://aws.amazon.com/image_url"
            }
        }
    ]
}
```

This endpoint retrieves all modules in the users library.

### HTTP Request

`GET http://{server}/api/mylibrary/{:id}`

<aside class="success">
The :id can be obtained from the authentication response
</aside>

# Projects

## Get all projects

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
slug | string | Return only the project with this specific slug
user | integer | Return all projects of a given user
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
bits | integer | Return projects with this product ID. Can be a comma separated list.
tag | string | Return all projects with a given tag
q | string | Search projects by keyword
page | integer | Page number of returned results. Default is 1
per_page | integer | Number of results per page. Default is 10


## Get a specific project

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
        "params": null
      },
      "success": true,
      "errors": null
    }
  }

```

`GET http://{server}/api/v2/projects/{:id}`
