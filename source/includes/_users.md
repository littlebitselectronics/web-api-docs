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
      "member_since": "Member since February 2015",
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

## Get a user's Likes

```shell
curl "http://{server}/api/v2/users/sch/likes"
```

> The above command returns JSON structured like this:

```json
{
  "results": [
    {
      "id": 1345,
      "name": "Real-Time Weather Dashboard",
      "slug": "real-time-weather-dashboard",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/4742/large_filled_weatherdashboard.jpg",
      "description": "<div>\r\n\t\t\t\t<div>\r\n\t\t\t\t\t<div>\r\n\t\t\t\t\t\t<p><b>Monitor current and forecasted weather data with littleBits and a little coding.</b> These customizable\r\nand modular weather boxes display current temperature, the forecasted high and low temperatures for the\r\nday, and the forecasted conditions for the day (i.e. sunny, cloudy, precipitation).\r\n</p>\r\n\t\t\t\t\t\t<p>Note: To complete this project, you will need to know how to work with APIs. The cloudBit’s API\r\ndocumentation can be found <a rel=\"nofollow\" target=\"_blank\" href=\"http://developer.littlebitscloud.cc/api-http\">here</a>. The Weather Underground's API documentation can be found <a rel=\"nofollow\" target=\"_blank\" href=\"http://www.wunderground.com/weather/api/d/docs?d=index\">here</a>.\r\n</p>\r\n\t\t\t\t\t\t<p><b>How they work:</b>\r\n</p>\r\n\t\t\t\t\t\t<p>We wrote a short program that gets information from Weather Underground and sends that data through the\r\nlittleBits cloud to a cloudBit. Every 30 minutes the program asks Weather Underground for the current\r\ntemperature and the forecasted high, low, and conditions for New York, NY. Then it converts this information\r\ninto a voltage* which is sent to each cloudBit, adjusting the angle of the servos (the servos must be set to\r\nturn mode for this to work). We've posted the code for our program here.\r\n</p>\r\n\t\t\t\t\t\t<p>*The program does not specify the volts, rather it sends a value from 0 to 100 which tells the cloudBit what\r\npercentage of the total power (5v) to output.&nbsp;</p>\r\n\t\t\t\t\t</div>\r\n\t\t\t\t</div>\r\n\t\t\t</div>",
      "comment_count": 8,
      "like_count": 23,
      "liked_by_user": null,
      "user": {
        "id": 1750,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/17/small_avatars_output-03.png",
        "slug": "littlebits",
        "username": "littleBits"
      }
    }
  ],
  "meta": {
    "version": 2,
    "criteria": {
      "method": "GET",
      "endpoint": "/api/v2/users/sch/likes",
      "params": [
        {
          "name": "id",
          "value": null
        },
        {
          "name": "slug",
          "value": "sch"
        }
      ]
    },
    "success": true,
    "errors": null
  }
}
```

`GET http://{server}/api/v2/users/{:id|:slug}/likes`

### Examples

`GET http://{server}/api/v2/users/25038/likes`

`GET http://{server}/api/v2/users/lev/likes`

## Create a user

`POST http://{server}/api/v2/users/new`

### Form Data

Parameter | Description
--------- | -----------
user[email] | New user's email address
user[username] | New user's username
user[password] | New user's password
user[password_confirmation] | New user's password

## Password Reset

`GET http://{server}/api/v2/users/password_reset?email=e@ma.il`
