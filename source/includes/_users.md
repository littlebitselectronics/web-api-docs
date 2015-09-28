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
curl "http://{server}/api/v2/users/lev/likes"
```

> The above command returns JSON structured like this:

```json
{
  "results": [
    {
      "id": 1399,
      "name": "Thermostat Hack",
      "slug": "thermostat-hack",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/5075/large_filled_servoarm.gif",
      "description": "<span><p><b>Control the temperature of your home remotely. </b>This thermostat add-on uses the littleBits cloudBit and a servo module to change the temperature of your home from anywhere. Heading home from work and want to cool your apartment down? Use the slider app on<a rel=\"nofollow\" target=\"_blank\" href=\"http://control.littlebitscloud.cc\"> littleBits Cloud Control</a> to wirelessly move the move the needle on the temperature scale. Want to make your thermostat smarter? Add a temperature sensor to get real time readings from your home.</p><p><i>*Note: temperature sensor is &nbsp;coming soon. Stay tuned!</i></p><br><p><b>How it works:</b></p><p><i>Control</i> - With this add-on, the littleBits servo is connected to adjuster arm on your thermostat. Use Cloud Control (on your phone or computer) to adjust the position of the servo arm, thus moving the little adjuster lever and changing the temperature.</p><br><p><i>Automate</i> - Use IFTTT to automatically adjust your thermostat in response to conditions that you set (i.e. time of day or forecasted weather conditions). <a rel=\"nofollow\" target=\"_blank\" href=\"https://ifttt.com/\">IFTTT (If This Then That)</a> is a service that lets you connect to different web apps through simple conditional statements. Use the <a rel=\"nofollow\" target=\"_blank\" href=\"https://ifttt.com/date_and_time\">Date &amp; Time channel</a> to turn your thermostat down at 1pm and up at 6pm. The littleBits trigger allows you to adjust the percentage of output voltage sent to the servo, giving you more control over the temperature of your home.</p><br><p><i>Monitor </i>- The temperature sensor transmits data through the cloudBit to Cloud Control, which can be viewed under the “receive signal” tab. This way, you can always know temperature in your apartment/house.</p><div><br></div></span>",
      "comment_count": 10,
      "like_count": 12,
      "liked_by_user": null,
      "user": {
        "id": 1750,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/17/small_avatars_output-03.png",
        "slug": "littlebits",
        "username": "littleBits"
      }
    },
    {
      "id": 1848,
      "name": "Lego Rail Crossing Arm and Counter",
      "slug": "lego-rail-crossing-arm",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/6454/large_filled_DMC_1474.jpg",
      "description": "Keep the lego mini figures safe at rail crossings with this lego rail crossing. &nbsp;It will also keep track of the number of trains which have passed over it as well.<br><br>",
      "comment_count": 2,
      "like_count": 2,
      "liked_by_user": null,
      "user": {
        "id": 36211,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_pinkModule.png",
        "slug": "david-mccormack",
        "username": "david.mccormack"
      }
    },
    {
      "id": 3197,
      "name": "Toilet Seat Alarm",
      "slug": "toilet-seat-alarm",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/7827/large_filled_toilet.png",
      "description": "I'm a horrible husband, and I think that littlebits can help me become a better spouse. Here's a project that does just that! This only works if you're thoughtful enough to turn off the bathroom light.&nbsp;",
      "comment_count": 1,
      "like_count": 5,
      "liked_by_user": null,
      "user": {
        "id": 45391,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_Tim_Cox.jpg",
        "slug": "timcox",
        "username": "timcox"
      }
    },
    {
      "id": 1553,
      "name": "Spinning Replicator",
      "slug": "spinning-replicator",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/5554/large_filled_SpinningReplicator_0001_wide.jpg",
      "description": "<p>The Spinning Replicator is a copy machine. It can scan an illustration and draw a copy of it without any kind of programming, just littleBits, LEGO elements and a marker. It moves like a gramophone, with two discs that rotates and a lever that travels from center to border. </p>\r\n<p>\r\nThe lever has two sides, one has a light sensor and the other has a marker attached to a servo. When the light sensor is over a dark area, the marker goes down, when the sensor finds a bright area, the marker goes up.\r\nWhen the copy is complete, the roller switch is released, the motors stops and the cloudBit send me a phone notification. </p>",
      "comment_count": 7,
      "like_count": 21,
      "liked_by_user": null,
      "user": {
        "id": 28385,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_arthur_sacek.png",
        "slug": "-4858bb87-204f-4cd8-a917-1292005c9315",
        "username": "arthursacek"
      }
    },
    {
      "id": 3383,
      "name": "LittleBits & Meccano",
      "slug": "crawler_01-ec7d9274-4a40-4206-97ff-21103cbe4d2b",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/8395/large_filled_Crawler_01.jpg",
      "description": "<p>A marriage of LittleBits and Meccano. This crawler is my first LittleBits project. The crawler is a fairly basic Meccano model that’s powered by a LittleBits DC Motor module. Eventually, as other modules are acquired, steering and remote control will be added.</p><p>I have some press-on brass sleeves on order that will adapt Meccano size (4.1 mm) pinions and spurs to be used with the DC Motor module. Since the LittleBits DC Motor module isn't powerful or fast enough to be of much use powering Meccano models, the plan is to use the Hardware Development Kit (HDK) to build a module that will allow LittleBits modules to control the larger more powerful Meccano motors.<br></p>",
      "comment_count": 3,
      "like_count": 1,
      "liked_by_user": null,
      "user": {
        "id": 55533,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_GWA120911.JPG",
        "slug": "georgea",
        "username": "GeorgeA"
      }
    },
    {
      "id": 4474,
      "name": "Lip Sync Minion",
      "slug": "lip-sync-minion",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/10982/large_filled_IMG_6886.JPG",
      "description": "I just came back from a trip around&nbsp;Asia. While I was there, I&nbsp;realized that the Minion toys from McDonalds there are different than the ones in New York. These Minions I found in Taiwan does more than just saying things and cursing,&nbsp;&nbsp;so awesome! <br><br>This particular one I found has a small slider&nbsp;in the back that opens and closes the&nbsp;Minion's mouth!! Hacker mode on!! BzZZzzzZZZzz!!<br><br>I have the following steps mapped out to my final&nbsp;goal:<br><br><b>Step1: </b>Can I control the mouth slider with a littlebits servo? <b>[checked!]</b><br><b>Step2: </b>Swap slider bit with Arduino bit&nbsp;<b>[checked!]</b><br><b>Step3: </b>Write a [Processing sketch 1] to communicate with the Arduino bit&nbsp;<b>[checked!]</b><br><b>Step4: </b>Write a separate [Processing sketch 2] to analyze sound&nbsp;<b>[checked!]</b><br><b>Step5:</b> Merge the code together!&nbsp;<b>[checked!]</b><br><br>I modified the SimpleWrite sketch in Processing to achieve this. I would like to change a few things in the future like make the mouth movement more analoguish than No and Off right now. Anyway, I had great fun with this side project, have a great day!",
      "comment_count": 1,
      "like_count": 3,
      "liked_by_user": null,
      "user": {
        "id": 34177,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_tumblr_nk0xjurrBP1qzyrh7o5_r1_540.jpg",
        "slug": "bfadt",
        "username": "PUSH"
      }
    },
    {
      "id": 4853,
      "name": "Automatic AC Thermostat",
      "slug": "automatic-ac-thermostat",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/12539/large_filled_17399379-5dd1-4c46-b044-70b711434283.png",
      "description": "<div><a rel=\"nofollow\" target=\"_blank\" href=\"http://youtu.be/FGvD5GybUBg\">http://youtu.be/FGvD5GybUBg</a> <br><br>My Second LittleBits project. My room gets pretty hot so I decided to have my fan automatically regulate the temperature. In this project I set my fan to turn on above 75 C and turn off below that.&nbsp;</div><div><br></div><div>PARTS</div><div>1 usb power</div><div>1 temperature sensor</div><div>1 threshold</div><div>1 IR Transmitter</div><div>1 AC Switch</div><div><br></div><div>OPTIONAL</div><div>1 split</div><div>1 number</div><div>1 cloudBit module</div>",
      "comment_count": 0,
      "like_count": 1,
      "liked_by_user": null,
      "user": {
        "id": 75479,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_dbe2f193-a627-4a2d-98c8-be106f93a9f9.png",
        "slug": "21920aa8-fa6b-4ee2-9511-7452f72e26c1",
        "username": "aaronify"
      }
    },
    {
      "id": 4512,
      "name": "Waste paper basketball cheering machine #BitOlympics",
      "slug": "waste-paper-basketball-cheering-machine-bitolympics",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/11099/large_filled_IMG_4436.JPG",
      "description": "The only thing more boring than producing tons of waste paper is having to throw it away the old-fashioned way. Without a basketball hoop, this is.<br>Therefore, for everyone's joy, here is the <b>waste paper basketball cheering machine</b>! Everytime your paper ball, Red Bull can, basketball or half eaten cup of ramen noodles passes the hoop, lights and the buzzer&nbsp;turn on for some enjoyable audio-visual effects aka blinking.<br>",
      "comment_count": 1,
      "like_count": 3,
      "liked_by_user": null,
      "user": {
        "id": 49620,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_Foto_Matthias_WOLF.png",
        "slug": "-2002d2ef-cd42-4141-bfcb-e0c587e58887",
        "username": "matthias.m.wolf"
      }
    },
    {
      "id": 4887,
      "name": "3G IoT Solar Rover",
      "slug": "3g-iot-solar-rover",
      "icon": "https://lb-community.s3.amazonaws.com/uploads/image/asset/12804/large_filled_04e6eb6c-63d5-4c52-8b6a-338887b3f1dc.jpg",
      "description": "<i>The 3G IoT Solar Rover w</i><i>e have built for the&nbsp;Holland Webweek Groningen,&nbsp;with the&nbsp;CloudBit, a solar panel,&nbsp;a wifi/3G connection and Lego (chassis).</i>",
      "comment_count": 0,
      "like_count": 1,
      "liked_by_user": null,
      "user": {
        "id": 67437,
        "image": "https://lb-community.s3.amazonaws.com/uploads/user/avatar/small_Profiel-foto.jpg",
        "slug": "andre-wolters",
        "username": "André Wolters"
      }
    }
  ],
  "meta": {
    "version": 2,
    "criteria": {
      "method": "GET",
      "endpoint": "/api/v2/users/lev/likes",
      "params": [
        {
          "name": "id",
          "value": null
        },
        {
          "name": "slug",
          "value": "lev"
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
